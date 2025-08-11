# 1ES Landscape

This repository contains a landscape visualization for the 1 Engineering System (1ES). It organizes projects, categories, and related data to provide an overview of the 1ES ecosystem.

## Structure

- `data.yml` — Main data source for categories, subcategories, and items.
- `settings.yml` — Configuration for appearance and grouping.
- `guide.yml` — Content for the landscape guide.
- `games.yml` — Data for interactive games and quizzes.
- `build/` — Generated assets and static site output.

## Usage

1. Edit the YAML files (`data.yml`, `settings.yml`, etc.) to update the landscape.
2. Build or serve the site using your preferred static site generator or build process.

## Installing

* Currently, using the `homebrew`install (`brew install cncf/landscape2/landscape2`). 
* Probably have to look into using the container setup for production.

## Commands

### Seeding a new landscape (Not needed for 1ES)

```bash
$ landscape2 new --output-dir .
```

### Building

```bash
$ landscape2 build 
  --data-file data.yml \
  --settings-file settings.yml \
  --guide-file guide.yml \
  --logos-path logos \
  --output-dir build
```

### Serving

```bash
$ landscape2 serve --landscape-dir build
``` 

### Validating

```bash
$ landscape2 validate settings --settings-file settings.yml
$ landscape2 validate games --settings-file games.yml
$ landscape2 validate data --settings-file data.yml
$ landscape2 validate guide --settings-file guide.yml
```


## Resources

- [Landscape documentation](https://github.com/cncf/landscape2?tab=readme-ov-file)