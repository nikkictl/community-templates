# MongoDB Dashboard for InfluxDB v2

Provided by: Ignacio Van Droogenbroeck

This Dashboard offers you information about your MongoDB instance. Uptime, Connections, Open Connections, Query Operations, Document Operations, Flushes, Network I/O and Commands per Seconds.

![Dashboard Screenshot](screenshot.png)

### Quick Install

#### InfluxDB UI

In the InfluxDB UI, go to Settings->Templates and enter this URL: https://raw.githubusercontent.com/influxdata/community-templates/master/mongodb/mongodb.yml

#### Influx CLI
If you have your InfluxDB credentials [configured in the CLI](https://v2.docs.influxdata.com/v2.0/reference/cli/influx/config/), you can install this template with:

```
influx apply -u https://raw.githubusercontent.com/influxdata/community-templates/master/mongodb/mongodb.yml
```

## Included Resources

    - 1 Telegraf Configuration: 'mongodb-config'
    - 1 Dashboards: 'MongoDB'
    - 1 bucket: 'mongodb'
    - 1 label: 'mongodb'

## Setup Instructions

General instructions on using InfluxDB Templates can be found in the [use a template](../docs/use_a_template.md) document.

    Telegraf Configuration requires the following environment variables
    - `INFLUX_HOST` - Your InfluxDB host (ex:http://localhost:9999)
    - `INFLUX_TOKEN` - The token with the permissions to read Telegraf configs and write data to the `telegraf` bucket. You can just use your operator token to get started.
    - `INFLUX_ORG` - The name of your Organization.
    - `INFLUX_BUCKET` - The name of the bucket you will store the data.

In order to use this Dashboard, you need to specify the string connection to MongoDB instance as variable. Ex:

```$ export MONGO_STRING_CONNECTION=mongodb://user:auth_key@10.10.3.30:27017```

Also, if you want to use the bucket include in this template. please, define the name bucket as variable too.

```$ export INFLUX_BUCKET=mongodb```

## Contact

Author: Ignacio Van Droogenbroeck

Email: ignacio[at]vandroogenbroeck[dot]net

Github and Gitlab user: @xe-nvdk

Influx Slack: Ignacio Van Droogenbroeck
