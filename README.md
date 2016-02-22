# Cloud Vision API with Golang

## Prerequisites

### Enable Cloud Vision API

You need to turn it on manually to be available. Let’s see and enable on your [developer console](https://console.cloud.google.com/apis/library?q=Cloud%20Vision%20API).

### Setting Up a Service Account

Set up a service account on [credentials page](https://console.cloud.google.com/apis/credentials) and get a service account credentials json file.

### Export credentials environment variable

Export export a service account json file into `GOOGLE_APPLICATION_CREDENTIALS` env variable:

```
$ export GOOGLE_APPLICATION_CREDENTIALS=/path/to/service_account.json
```

### Dependencies

To run this sample, you need to install these packages:

- golang.org/x/net/context
- golang.org/x/oauth2/google
- google.golang.org/api/vision/...

To install all of them at once, type:

```
go get github.com/hermanschaaf/go-cloud-vision-api/...
```

## Installation

Type the below command to install if you use this application on your device.

```shell
go get github.com/hermanschaaf/go-cloud-vision-api
```

Make sure that `go-cloud-vision-api` was installed correctly:

```shell
go-cloud-vision-api -h
```

## Usage

```shell
go run main.go lenna.jpg
```

or if you already installed as a command.

```shell
go-cloud-vision-api lenna.jpg
```

## Example

### input

![lenna.jpg](https://raw.githubusercontent.com/kaneshin/go-cloud-vision-api/master/lenna.jpg)

### output

[more detail](https://github.com/kaneshin/go-cloud-vision-api/blob/master/result.json)

```
[
  {
    "faceAnnotations": [
      {
        "angerLikelihood": "VERY_UNLIKELY",
        "blurredLikelihood": "VERY_UNLIKELY",
        "boundingPoly": {
          "vertices": [
            {
              "x": 143,
              "y": 43
            },
            {
              "x": 245,
              "y": 43
            },
            {
              "x": 245,
              "y": 163
            },
            {
              "x": 143,
              "y": 163
            }
          ]
        },
        "detectionConfidence": 0.99805844,
        "fdBoundingPoly": {
          "vertices": [
            {
              "x": 172,
              "y": 82
            },
            {
              "x": 241,
              "y": 82
            },
            {
              "x": 241,
              "y": 151
            },
            {
              "x": 172,
              "y": 151
            }
          ]
        },
        "headwearLikelihood": "UNLIKELY",
        "joyLikelihood": "VERY_UNLIKELY",
        "landmarkingConfidence": 0.5350582,
        "landmarks": [
          {
            "position": {
              "x": 197.90556,
              "y": 102.932,
              "z": 0.00083794753
            },
            "type": "LEFT_EYE"
          },
          {
            "position": {
              "x": 223.43489,
              "y": 102.72927,
              "z": 17.352478
            },
            "type": "RIGHT_EYE"
          },
          {
            "position": {
              "x": 189.50327,
              "y": 96.40799,
              "z": -4.1362653
            },
            "type": "LEFT_OF_LEFT_EYEBROW"
          },
          ...
```


## License

[The MIT License (MIT)](http://kaneshin.mit-license.org/)


## Author

Shintaro Kaneko <kaneshin0120@gmail.com>
