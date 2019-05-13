# Changelog

## [2.4.5] - 2019-03-29

### Added

- Added debrief feature to make sure data has synced to nas

## [2.4.4] - 2019-03-25

### Added

- Added get_log_path() API in process_monitor plugin for remote debugger

## [2.4.3] - 2019-03-21

### Fixed

- Fixed debrief merge issue
- Disabled node_status topic at debrief mode (2019-03-11)

## [2.4.2] - 2019-03-18

### Added

- Adaptive GPU Device ID

## [2.4.1] - 2018-01-24

### Added

- Added get_node_out_topics() API

## [2.4.0] - 2018-01-24

### Removed

- Removed support for OctopusApp

## [2.3.1] - 2018-01-21

### Fixed

- Fix a deadlock condition in process monitor

## [2.3.0] - 2018-01-15

### Added

- `replay_speed` support during regen mode

## [2.2.10] - 2018-01-26

### Changed

- Changed use IMAGE_TAG when writing to datasets.

## [2.2.9] - 2018-01-25

### Changed

- Changed use IMAGE_VERSION when writing to datasets.

## [2.2.8] - 2018-01-09

### Fixed

- Fix a bug that errors in `generate_app` will skip module cleanup that causes incorrect apps module.

## [2.2.7] - 2018-01-09

### Changed

- Change behavior of `recording_path` in regen mode

## [2.2.6] - 2018-01-09

### Added

- Support for both old vehicle_config and new vehicle_name

## [2.2.5] - 2018-01-08

### Fixed

- Fixed module import issue.

## [2.2.4] - 2019-01-04

### Added

- Alias for `/diagnostics` topic
- Hardcoded `console_backend` topics

## [2.2.3] - 2019-01-03

### Added

- Alias for recorded `/octopus/node_status` topic

### Changed

- Use `rosmaster --core` instead of `roscore`

## [2.2.2] - 2018-12-27

### Changed

- Skip machine assignment if node_assignment is not present.

## [2.2.1] - 2018-12-27

### Changed

- Use hostname instead of IP for ROSMaster in vehicle mode
- Support delayed start in auto_start config

## [2.2.0] - 2018-12-20

### Changed

- Remove 'Octopus-' from `vehicle_name`
- Use NodeHandler in debrief mode

## [2.1.9] - 2018-12-20

### Changed

- Change ds-play timeout to 60s (0.05s * 1200)

## [2.1.8] - 2018-12-13

### Added

- Add `trip_id` to `landing_cfg`

## [2.1.7] - 2018-12-12

### Fixed

- add IMAGE_BUILD_ID in docker

## [2.1.6] - 2018-12-10

### Added

- API for downloading full log

## [2.1.5] - 2018-12-06

### Changed

- Store manually added tags into `event` when adding tag in Debrief mode

## [2.1.4] - 2018-12-05

### Changed

- Use IP address instead of hostname in ROSMaster to allow cross site communication

## [2.1.3] - 2018-12-04

### Changed

- Skip non-present node during regeneration

## [2.1.2] - 2018-12-03

### Changed

- Do not raise exception if cannot obtain current vehicle config

## [2.1.1] - 2018-11-30

### Changed

- Store vehicle info in config dir of dataset

## [2.1.0] - 2018-11-29

### Added

- Support for OctopusAPI
- Support for OctopusApp2

## [2.0.7] - 2018-11-29

### Changed

- "auto_start" will ignore nonexisting nodes

## [2.0.6] - 2018-11-27

### Changed

- Allow to use new config thru roslaunch
- Allow more time for rosmaster to start

## [2.0.5] - 2018-11-20

### Changed

- Allow console to be stopped multiple times
- Update debrief handler to support custom tag data

### Fixed

- Debrief tag range precision issue when committing

## [2.0.4] - 2018-11-19

### Changed

- Add docker version to recorded dataset

## [2.0.3] - 2018-11-19

### Changed

- Increased timeout value for recorder termination.

## [2.0.2] - 2018-11-08

### Added

- Add `get_node_status` API

## [2.0.1] - 2018-11-08

### Fixed

- `recording_path` will default to `~/octopus_bags` in vehicle mode.

## [2.0.0] - 2018-11-08

### Changed

- Fully rewritten from scratch.

## [1.3.16] - 2018-10-29

### Changed

- remove camera trigger from system and move it to camera repo 

## [1.3.15] - 2018-10-05

### Changed

- `add_tag` now will use server time instead of client time to prevent incorrect time on client

## [1.3.15] - 2018-10-05
### Added
- Save octopus nodes in top.json to support replay when some nodes' src code is not present.

## [1.3.14] - 2018-10-07

### Added

- IMAGE_BUILD_ID to recorded docker name

## [1.3.13] - 2018-10-04

### Changed
- Prevent removal of bags only based on its import status (only remove when older than 1 day)

## [1.3.12] - 2018-09-07
### Added
- store topics in top.json
- use regen cleaner to handle file moving 

## [1.3.11] - 2018-08-24

### Added
- regen: run nodes sequentially
- SIGKILL to kill a node if not responding for 30s

### Fixed
- Node sorted by name in node graph

## [1.3.10] - 2018-08-24

### Added
- regen: let user choose check or not

## [1.3.9] - 2018-08-22

### Fixed
- Plugin dependencies.
- regeneration & replay offset problem

## [1.3.8] - 2018-08-22

### Fixed
- moved node generation to vehicle config parser.

## [1.3.7] - 2018-08-22

### Added
- out topics


## [1.3.6] - 2018-08-21

### Fixed
- support `.tsmap` in node handler


## [1.3.5] - 2018-08-20

### Fixed
- typo env while recording dataset

## [1.3.4] - 2018-08-16

### Removed
- rospy

### Changed
- code structure
- start/exit logic

## [1.3.3] - 2018-08-16

### Changed

- Support for old vehicle name.

## [1.3.2] - 2018-08-14

### Added

- Octopus App support

## [1.3.1] - 2018-08-13

### Added
- More metadata in regeneration

## [1.3.0] - 2018-08-09

### Removed
- 8080 front-end and its backend components

### Changed
- Plugin structure

### Fixed
- Regeneration Recorder bugs

## [1.2.19] - 2018-08-09

### Changed

- regeneration data write to /tmp before move to dataset-addon

### Added

- publish sns message for regeneration

## [1.2.18] - 2018-08-08

### Fixed

- support ttyUSB* auto find feature

## [1.2.17] - 2018-08-07

### Fixed 

- handled subprocess exception in parameter center 

## [1.2.16] - 2018-08-07

### Changed

- add docker version in top.json

## [1.2.15] - 2018-08-01

### Changed

- Fix "no enough space" error in replay mode

## [1.2.14] - 2018-07-30

### Added

- support play audio in replay mode

## [1.2.13] - 2018-07-27

### Added

- delete the dataset on truck which is already imported

## [1.2.12] - 2018-07-17

### Added

- UNBUFFEREDPYTHON

## [1.2.11] - 2018-07-15

### Removed

- Alert plugin

### Changed

- Heartbeat logic and audio API

## [1.2.10] - 2018-07-11

### Removed

- USB Cam util

## [1.2.9] - 2018-07-11

### Added 

- Slow and extremely slow audio

## [1.2.8] - 2018-07-09

### Fixed 

- Fix usb cam starting logic 

## [1.2.7] - 2018-07-03

### Changed

- Sort nodes in topological order
- Publish `node_status` topic when status changed

### Fixed

- Use list instead of queue for py2 compatibility

### Removed

- MapHandler from plugins

## [1.2.7] - 2018-07-01

### Changed

- Move `hmi_server` to launch file

## [1.2.6] - 2018-06-26

### Added
- parse new middleware `hardware_id`
- Support for HMI tag viewer

## [1.2.6] - 2018-06-20

### Added
- Tag creator
- Audio alert

## [1.2.5] - 2018-06-11

### Changed
- Change heartbeat timeout to 1.5s
- Do not quit when USB cam fails because some system path does not exist

## [1.2.4] - 2018-06-06

### Changed
- Move Octopus node's logs to `ROS_LOG`

## [1.2.3] - 2018-06-05

### Fixed
- Fix gTTS version

## [1.2.2] - 2018-06-04

### Changed
- some enhancement in audio recording for debrief

## [1.2.1] - 2018-06-04

### Changed
- Better handling audio warning on newly launched nodes
- Fix missing vehicle name in recording

## [1.2.0] - 2018-06-03

### Changed
- automatically generate audio if not previously generated
- `/vehicle/dbw_enabled` is published by DatasetPlayer. Because this topic is a latched topic and we should rely on `dbw_enabled` tag to identify the period of autonomous driving


## [1.1.1] - 2018-06-02

### Changed
- by default do not use `enable_viz` in vehicle mode, because currently only fusion works


## [1.1.0] - 2018-05-31

### Added
- ds-play style API for replay control
- publish a topic named `/octopus/node_status` to update node status
- tests for `dbw_enabled` tagging and recording

### Fixed
- Bug in creating a tag through topics


## [1.0.0] - 2018-05-29

### Added
- `ts_rpc` wrapper for front-end requests
- tuyaco ci

### Changed
- Locks in each OctopusNode rather than NodeHandler
- Replace play/recording wrapper with ds-play and ds-record

### Removed
- Monitor Center. Now using diagnostic directly
