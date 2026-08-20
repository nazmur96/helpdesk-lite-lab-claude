# HelpDesk Lite

A minimal support-ticket CLI, used as a training ground for Git and GitHub Actions.

## Requirements

Python 3.10 or newer. That's it — there are no third-party dependencies and
nothing to install. Every command below runs from the repository root.

## Running the tests

```bash
python -m unittest discover -s tests
```

## Running the CLI

```bash
python -m helpdesk list
```

```
INC-101  LOW  Update company logo on internal wiki
INC-102  MEDIUM  Laptop keyboard intermittently unresponsive
INC-103  MEDIUM  VPN disconnects during video calls
INC-104  HIGH  Payment page returns an error
INC-109  HIGH  Customer cannot reset password
```

## Project structure

```
helpdesk-lite-lab/
├── helpdesk/           # Application package
│   ├── __main__.py     # Enables `python -m helpdesk`
│   ├── cli.py          # Argument parsing and output formatting
│   ├── models.py       # The Ticket dataclass
│   └── service.py      # Loading tickets from JSON
├── tests/              # Unit tests (stdlib unittest)
├── data/tickets.json   # Sample ticket data
└── pyproject.toml      # Project metadata
```

## Development

This project follows test-driven development: a failing test comes first, then
the smallest implementation that makes it pass.
