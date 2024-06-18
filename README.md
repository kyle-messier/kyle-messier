# Welcome to my personal GitHub profile.

Hello! I'm [Kyle P Messier, PhD](https://niehs.github.io/SET/people.html#KPM), Stadtman Tenure Track Investigator at the National Institute of Environmental Health Sciences.  

## {SET}group

The Spatiotemporal Exposures and Toxicology group, {SET} group, at NIEHS has a broad interest in geospatial [exposomics](https://factor.niehs.nih.gov/2022/9/feature/2-feature-exposomics-research) and risk mapping. 

Please check out our [gh-pages](https://niehs.github.io/SET/) website for details on the people, papers, and software. 


## Software 

Our code and software is hosted at the [NIEHS GitHub](https://github.com/NIEHS/) Enterprise.

Here is a current list of our software in development:

| No. | Package Name                                                                          | Description | Status |
|--------|-------------------------------------------------------------------|----------|----------------------------|
| 1.  | [amadeus](https://niehs.github.io/amadeus/)                  | **A** **Ma**chine for **D**ata, **E**nvironments, and **U**ser **S**etup for common environmental and climate health datasets is an R package developed to improve and expedite users’ access to large, publicly available geospatial datasets. | [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) |
| 2.  | [beethoven](https://niehs.github.io/beethoven/)                                                                     | **B**uilding an **E**xtensible, R**e**producible, **T**est-driven, **H**armonized, **O**pen-source, **V**ersioned, **En**semble model for air quality is an R package developed to facilitate the development of ensemble models for air quality. | [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) |
| 3.  | [chopin](https://niehs.github.io/chopin/)                    | Computation for **C**limate and **H**ealth research **O**n **P**arallelized **In**frastructure automates parallelization in spatial operations with chopin functions as well as sf/terra functions. | [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) |
| 4.  | [GeoTox](https://niehs.github.io/GeoTox)                 | GeoTox, or source-to-outcome, modeling framework with an S3 object-oriented approach. Facilitates the calculation and visualization of single and multiple chemical risk at individual and group levels. | [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) |
| 5.  | [RGCA](https://niehs.github.io/RGCA)                    | Implements Reflected Generalized Concentration Addition: A geometric, piecewise inverse function for 3+ parameter sigmoidal models used in chemical mixture concentration-response modeling. | [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) |
| 6.  | [PrestoGP](https://niehs.github.io/PrestoGP/)                 | Scalable **p**enalized **re**gression on **s**patio-**t**emporal **o**utcomes using **G**aussian **p**rocesses. Designed for big data, large-scale geospatial exposure assessment, and geophysical modeling. | [![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](https://www.repostatus.org/badges/latest/wip.svg)](https://www.repostatus.org/#wip) |

## Software Development Practices

We are focused on developing and promoting software and computational best-practices such as test-driven-development ([TDD](https://en.wikipedia.org/wiki/Test-driven_development)) and open-source code for the environmental health sciences. To this end, we have protocols in place
to ensure that our code is well-documented, tested, and reproducible. Below are some of the key practices we follow:

###  Unit and Integration Testing 

We will utilize various testing approaches to ensure functionality and quality of code.

### Git + GitHub 

Version control of software is essential for reproducibility and collaboration. We use Git and the [NIEHS Enterprise GitHub](https://github.com/NIEHS) for version control and collaboration.

#### CI/CD Workflows

Within GitHub, we will utilize continuous integration and continuous deployment workflows to ensure that our code is always functional and up-to-date. Multiple ** branch protection rules** within GitHub aresetup and enforced for our GitHub repositories:

1. Require pull request and 1 review before merging to `main`
2. Test pass: [Linting](https://lintr.r-lib.org/index.html): Code shall adhere to the style/linting rules defined in the repository.
3. Test pass: [Tets Coverage](https://testthat.r-lib.org/): A given push should not decrease overall test coverage of the repository.
4. Test pass: [Build Checks](https://github.com/r-lib/actions/blob/v2-branch/examples/check-standard.yaml): The code should build without errors or warnings.

The CI/CD workflows in GitHub are setup to run on every push to the main branch and on every pull request. The workflows are setup using yaml files in the `.github/workflows` directory of the repository.


### Processes to test or check 
1) data type
2) data name
3) data size
4) relative paths
5) output of one module is the expectation of the input of the next module

### Test Drive Development
Starting from the end product, we work backwards while articulating the tests needed at each stage.

#### Key Points of Unit and Integration Testing
##### File Type
1. NetCDF
2. Numeric, double precision
3. NA
4. Variable Names Exist
5. Naming Convention

##### Stats 
1. Non-negative variance ($\sigma^2$)
2. Mean is reasonable ($\mu$)
3. SI Units

##### Domain 
1. In the geographic domain (eg. US + buffer)
2. In Time range (e.g. 2018-2022)

##### Geographic 
1. Projections
2. Coordinate names (e.g. lat/lon)
3. Time in acceptable format 

### Test Driven Development (TDD)- Key Steps

1. **Write a Test**: Before you start writing any code, you write a test case for the functionality you want to implement. This test should fail initially because you haven't written the code to make it pass yet. The test defines the expected behavior of your code.

2. **Run the Test**: Run the test to ensure it fails. This step confirms that your test is correctly assessing the functionality you want to implement.

3. **Write the Minimum Code**: Write the minimum amount of code required to make the test pass. Don't worry about writing perfect or complete code at this stage; the goal is just to make the test pass.

4. **Run the Test Again**: After writing the code, run the test again. If it passes, it means your code now meets the specified requirements.

5. **Refactor (if necessary)**: If your code is working and the test passes, you can refactor your code to improve its quality, readability, or performance. The key here is that you should have test coverage to ensure you don't introduce new bugs while refactoring.

6. **Repeat**: Continue this cycle of writing a test, making it fail, writing the code to make it pass, and refactoring as needed. Each cycle should be very short and focused on a small piece of functionality.

7. **Complete the Feature**: Keep repeating the process until your code meets all the requirements for the feature you're working on.

TDD helps ensure that your code is reliable and that it remains functional as you make changes and updates. It also encourages a clear understanding of the requirements and promotes better code design.

### _targets and/or snakemake pipelines

We will utilize the `targets` and/or `snakemake` packages in R and Python respectively to create reproducible workflows for our data analysis. These packages allow us to define the dependencies between the steps in our analysis and ensure that our analysis is reproducible. Additionally, they keep track of pipeline objects and skip steps that have already been run, saving time and resources.

#### Some Benefits of _targets and/or snakemake pipelines

1. **Reproducibility**: By defining the dependencies between the steps in our analysis, we ensure that our analysis is reproducible. This is essential for scientific research and data analysis.

2. **High-Level Abstract**: _targets and snakemake allow us to define our analysis at a high level of abstraction, making it easier to understand and maintain.

3. **Testing**: Creating pipelines and unit/integration testing go hand-in-hand together. As we write the pipeline, the tests to write become obvious. 


