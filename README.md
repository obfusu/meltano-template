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

### Running target-rest-api (currently no-op implementation)

```
cd meltano-template
source .venv/bin/activate
./invoke-rest-target.sh # meltano elt tap-gitlab target-rest-api --job_id=gitlab-to-rest-api
```

### Target code

[Implement here](https://github.com/obfusu/meltano-template/blob/e0fe3f8866c1265f079b3f745a0ab3b2b11e31b8/extract/target-rest-api/target_rest_api/__init__.py#L50)
