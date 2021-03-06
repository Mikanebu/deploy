Deployment automation for the DataHub.

## Installation

Git clone then install the requirements:

```
pip install -r requirements.txt
```

## Configuration

Set up your configuration variables in a file called `.env`. You can copy paste and `.env.template`.

Note: for multiline variable values you must replace newlines with `\n` and quote the variable e.g. a variable that looks like this originally:

```
----BEGIN PUBLIC KEY-----
...
...
```

Must be in the `.env` file like this:

```
PUBLIC_KEY="----BEGIN PUBLIC KEY-----\n...\n..."
```

## Using

Run the script and it will list the available commands:

```
python main.py
```

Main one right now is:

```
python main.py docker
```

Sometimes this times out on the redeploy as the update hasn't finished. In that case just run:

Note: Node cluster with tag name ${PROJECT}-${STAGE} should exist on docker-cloud

```
python main.py docker_deploy
```
