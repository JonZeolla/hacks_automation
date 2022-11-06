# HACKS Automation

Welcome to hacks-automation

## Getting Started

First, you need to ensure you have `docker`, `git`, `pipenv`, and `python3` installed locally, and the `docker` daemon is running.

Then, you can setup your local environment via:

```bash
# Install the dependencies
pipenv install --deploy --ignore-pipfile --dev

# Build the image
pipenv run invoke build

# Run the image
docker run jonzeolla/hacks_automation:2022.11.00 --help
```

## Troubleshooting

If you're troubleshooting the results of any of the invoke tasks, you can add `--debug` to enable debug logging, for instance:

```bash
pipenv run invoke build --debug
```
