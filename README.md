# egeoffrey-service-csv

This is an eGeoffrey service package.

## Description

Retrieve values from a csv file.

## Install

To install this package, run the following command from within your eGeoffrey installation directory:
```
egeoffrey-cli install egeoffrey-service-csv
```
After the installation, remember to run also `egeoffrey-cli start` to ensure the Docker image of the package is effectively downloaded and started.
To validate the installation, go and visit the *'eGeoffrey Admin'* / *'Packages'* page of your eGeoffrey instance. All the modules, default configuration files and out-of-the-box contents if any will be automatically deployed and made available.
## Content

The following modules are included in this package.

For each module, if requiring a configuration file to start, its settings will be listed under *'Module configuration'*. Additionally, if the module is a service, the configuration expected to be provided by each registered sensor associated to the service is listed under *'Service configuration'*.

To configure each module included in this package, once started, click on the *'Edit Configuration'* button on the *'eGeoffrey Admin'* / *'Modules'* page of your eGeoffrey instance.
- **service/csv**: retrieve values from a csv file
  - Service configuration:
    - Mode 'pull':
      - *csv_file**: location or URL of the CSV file (e.g. https://www1.ncdc.noaa.gov/pub/data/cdo/samples/NORMAL_DLY_sample_csv.csv)
      - *value_position**: column number which contains the value to extract
      - *filter*: if defined, only the lines of the file with this value at this position will be evaluated
      - *filter_position*: the column you want to filter in the csv file
      - *date_position*: the column of the date (UTC) in the csv file
      - *date_format*: the format of the date in strftime format
      - *prefix*: an optional prefix of the value (that will be striped out) used as additional filter

## Contribute

If you are the author of this package, simply clone the repository, apply any change you would need and run the following command from within this package's directory to commit your changes and automatically push them to Github:
```
egeoffrey-cli commit "<comment>"
```
After taking this action, remember you still need to build (see below) the package (e.g. the Docker image) to make it available for installation.

If you are a user willing to contribute to somebody's else package, submit your PR (Pull Request); the author will take care of validating your contributation, merging the new content and building a new version.

## Build

Building is required only if you are the author of the package. To build a Docker image and automatically push it to [Docker Hub](https://hub.docker.com/r/egeoffrey/egeoffrey-service-csv), run the following command from within this package's directory:
```
egeoffrey-cli build egeoffrey-service-csv <amd64|arm>
```

## Uninstall

To uninstall this package, run the following command from within your eGeoffrey installation directory:
```
egeoffrey-cli uninstall egeoffrey-service-csv
```
Remember to run also `egeoffrey-cli start` to ensure the changes are correctly applied.
## Tags

The following tags are associated to this package:
```
service csv
```

## Version

The version of this egeoffrey-service-csv is 1.0-12 on the development branch.
