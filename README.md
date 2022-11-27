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
docker run jonzeolla/hacks_automation:2022.11.01 --help
```

## Manual setup

### Whoop

Configure the following Journal questions and answer them daily to map to questions in the HACKS spreadsheet:

| Whoop Journal                         | HACKS sheet                |
| ------------------------------------- | -------------------------- |
| Feel energized throughout the day?    | Energy levels              |
| Feel emotionally and mentally stable? | Ability to focus           |
| Experience any stress?                | Mental or emotional stress |
| Do you feel recovered today?          | Muscle soreness            |
| Sick?                                 | Signs of illness           |
| Notes                                 | Session performed          |
| Spend time outdoors?                  | Daylight time estimate     |

## Troubleshooting

If you're troubleshooting the results of any of the invoke tasks, you can add `--debug` to enable debug logging, for instance:

```bash
pipenv run invoke build --debug
```
