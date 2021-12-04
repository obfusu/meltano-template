# Quick Start

```
git clone https://github.com/obfusu/meltano-template
cd meltano-template
python3 -m venv .venv
source .venv/bin/activate
pip3 install meltano
meltano install
```
Create `.env` file and add your gitlab token
```
TAP_GITLAB_PRIVATE_TOKEN="glpat-xxxx"
```

### Running target-rest-api

```
cd meltano-template
source .venv/bin/activate
./invoke-rest-target.sh # meltano elt tap-gitlab target-rest-api --job_id=gitlab-to-rest-api
```

Note: This target makes POST request to http://localhost:8080/echo for each jsonl line. Doesn't handle state nor throws error if api is down.

### Target code

[Implement here](https://github.com/obfusu/meltano-template/blob/53508c1176c6124ce9bcaccdb31fdafd8861e40a/extract/target-rest-api/target_rest_api/__init__.py#L54)
