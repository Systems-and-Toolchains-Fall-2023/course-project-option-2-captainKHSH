<p align="center">
<img src="https://github.com/Systems-and-Toolchains-Fall-2023/course-project-option-2-captainKHSH/assets/74871590/867eb86c-ff80-4062-84f3-acc69975bb33" width="500">
<br/>
</p>

![GitHub repo size](https://img.shields.io/github/repo-size/Systems-and-Toolchains-Fall-2023/course-project-option-2-captainKHSH)
![GitLab last commit](https://img.shields.io/gitlab/last-commit/Systems-and-Toolchains-Fall-2023/course-project-option-2-captainKHSH)

# MQTT Dataset

This dataset contains information related to MQTT (Message Queuing Telemetry Transport) protocol.

## Latest Development Changes
```bash
python -m pip install git+https://github.com/Systems-and-Toolchains-Fall-2023/course-project-option-2-captainKHSH
```

## Install
- [pgAdmin4](https://www.postgresql.org/)
- ```bash
  python -m pip install pyspark
  ```


## Features

| Feature                 | Description                                                  | Type                              |Nullable|
|-------------------------|--------------------------------------------------------------|-----------------------------------|---------|
| tcp.flags               | Flags associated with TCP (Transmission Control Protocol) communication. |text|not null|
| tcp.time_delta          | Time difference between TCP packets.                        |double precision||
| tcp.len                 | Length of the TCP packet.                                    |integer||
| mqtt.conack.flags       | MQTT connection acknowledgment flags.                        |text||
| mqtt.conack.flags.reserved | Reserved flags for MQTT connection acknowledgment.         |double precision||
| mqtt.conack.flags.sp   | MQTT connection acknowledgment flag - SP.                    |double precision||
| mqtt.conack.val         | Value associated with MQTT connection acknowledgment.        |double precision||
| mqtt.conflag.cleansess  | MQTT connection flag indicating clean session.               |double precision||
| mqtt.conflag.passwd    | MQTT connection flag indicating password usage.             |double precision||
| mqtt.conflag.qos       | MQTT connection flag indicating QoS (Quality of Service).   |double precision||
| mqtt.conflag.reserved  | Reserved flag for MQTT connection.                           |double precision||
| mqtt.conflag.retain    | MQTT connection flag indicating message retention.           |double precision||
| mqtt.conflag.uname     | MQTT connection flag indicating username usage.              |double precision||
| mqtt.conflag.willflag  | MQTT connection flag indicating will flag.                   |double precision||
| mqtt.conflags           | Combined MQTT connection flags.                              |text||
| mqtt.dupflag            | MQTT duplicate message flag.                                 |double precision||
| mqtt.hdrflags           | MQTT header flags.                                           |text||
| mqtt.kalive             | MQTT keep-alive interval.                                    |double precision||
| mqtt.len                | Length of the MQTT packet.                                   |double precision||
| mqtt.msg                | MQTT message.                                                |text||
| mqtt.msgid              | MQTT message identifier.                                     |double precision||
| mqtt.msgtype            | MQTT message type.                                           |double precision||
| mqtt.proto_len          | Length of the MQTT protocol.                                 |double precision||
| mqtt.protoname          | MQTT protocol name.                                          |text||
| mqtt.qos                | MQTT quality of service.                                     |double precision||
| mqtt.retain             | MQTT retain flag.                                            |double precision||
| mqtt.sub.qos            | MQTT subscribe quality of service.                            |double precision||
| mqtt.suback.qos         | MQTT subscribe acknowledgment quality of service.            |double precision||
| mqtt.ver                | MQTT protocol version.                                       |double precision||
| mqtt.willmsg            | MQTT will message.                                           |double precision||
| mqtt.willmsg_len        | Length of the MQTT will message.                              |double precision||
| mqtt.willtopic          | MQTT will topic.                                             |double precision||
| mqtt.willtopic_len      | Length of the MQTT will topic.                                |double precision||
| target                  | Target variable indicating a specific target.                |text|not null|
|dataset                  |Diffrentiate between "train" or "test"                        |text|not null|
|id                       |"matt_pkey" PRIMARY KEY, btree                                |integer|not null|

Please refer to the dataset documentation for more details on each feature and its representation.


## Constraints

Here are the constraints for columns in the dataset:

| Feature                 | Constraint                                                |
|-------------------------|-----------------------------------------------------------|
|tcp.len|Must be non-negative (>= 0).|
| mqtt.len                | Must be non-negative (>= 0).|
| tcp.time_delta               | Must be non-negative (>= 0).|
|mqtt.protoname         | Length must not exceed a specified maximum length.        |
|dataset|Check if the data is "train" or "test"|

Please refer to the dataset documentation for more details on the constraints and the dataset structure.


## Usage

To use this dataset, follow the instructions below:
1. [In this project, you will use MQTT Dataset available on Kaggle](https://www.kaggle.com/datasets/cnrieiit/mqttset)
2. Download the dataset.
3. Load both train and test dataset into one Postgres Database table.
5. Apply the constraints as needed for your analysis or machine learning tasks.



