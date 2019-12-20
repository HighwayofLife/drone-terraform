# drone-terraform

[![Build Status](http://beta.drone.io/api/badges/highwayoflife/drone-terraform/status.svg)](http://beta.drone.io/highwayoflife/drone-terraform)

Drone plugin to execute Terraform plan and apply. For the usage information and
a listing of the available options please take a look at [the docs](https://github.com/highwayoflife/drone-terraform/blob/master/DOCS.md).

## Build

Build the binary with the following commands:

```
export GO111MODULE=on
go mod download
go test
go build
```

## Docker

Build the docker image with the following commands:

```
docker build --rm=true \
  -t highwayoflife/drone-terraform \
  --build-arg terraform_version=0.12.0 .
```

## Usage

Execute from the working directory:

```
docker run --rm \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  highwayoflife/drone-terraform:latest --plan
```

