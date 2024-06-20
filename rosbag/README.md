# rosbag

## File Organization

* Filenames correspond to trial number -- i.e., `01`-`22`

## Experimental Setup
* `acl-alpha`
    * Starting Position: `x+` relative to `acl-beta`
    * Altitude: `z = 0.50m`
    * UWB Nodes: `n6`-`n11`
* `acl-beta`
    * Starting Position: Center of mocap space
    * Altitude: `z = 1.75m`
    * UWB Nodes: `n0`-`n5`
* `acl-delta`
    * Starting Position: `x-` relative to `acl-beta`
    * Altitude: `z = 0.50m`
    * UWB Nodes: `n12`-`n17`

## rosbag topics
| ROS Topic          | rate [Hz] | message type                       |
| ------------------ | --------- | ---------------------------------- |
| `/acl_alpha/world` | `100`     | `geometry_msgs/PoseStamped`        |
| `/acl_beta/world`  | `100`     | `geometry_msgs/PoseStamped`        |
| `/acl_delta/world` | `100`     | `geometry_msgs/PoseStamped`        |
| `/n0/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n1/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n2/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n3/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n4/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n5/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n6/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n7/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n8/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n9/range`        | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n10/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n11/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n12/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n13/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n14/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n15/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n16/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |
| `/n17/range`       | `25`      | `nlink_parser/LinktrackNodeframe2` |

## rosbag info
| Filename | Duration [s] | Messages [count] | Size [MB] | acl-alpha          | acl-beta           | acl-delta          | Description                        |
| -------- | ------------ | ---------------- | --------- | ------------------ | ------------------ | ------------------ | ---------------------------------- |
| `01.bag` | `76`         | `57284`          | `16.2`    | Stationary         | Stationary         | Stationary         | Calibration, stationary            |
| `02.bag` | `126`        | `94647`          | `26.7`    | CW rot             | Stationary         | CW rot             | Calibration, in place rotation     |
| `03.bag` | `130`        | `97436`          | `27.5`    | CCW rot            | Stationary         | CCW rot            | Calibration, in place rotation     |
| `04.bag` | `84`         | `63301`          | `17.9`    | CW rot             | Stationary         | CCW rot            | Calibration, in place rotation     |
| `05.bag` | `77`         | `57702`          | `16.3`    | CCW rot            | Stationary         | CW rot             | Calibration, in place rotation     |
| `06.bag` | `77`         | `58105`          | `16.4`    | Stationary         | CW rot             | Stationary         | Calibration, in place rotation     |
| `07.bag` | `77`         | `58284`          | `16.5`    | Stationary         | CCW rot            | Stationary         | Calibration, in place rotation     |
| `08.bag` | `89`         | `66929`          | `18.9`    | Drive in/out       | Stationary         | Drive in/out       | Calibration, varying distance      |
| `09.bag` | `162`        | `121735`         | `34.3`    | CW circle          | Statinoary         | CW circle          | Calibration, fixed distance circle |
| `10.bag` | `153`        | `114914`         | `32.4`    | CCW circle         | Stationary         | CCW circle         | Calbiration, fixed distance circle |
| `11.bag` | `216`        | `162218`         | `45.7`    | CCW box            | Stationary         | CW spiral          | Calibration, patterns              |
| `12.bag` | `162`        | `121902`         | `34.4`    | CW box             | Stationary         | CCW spiral         | Calibration, patterns              |
| `13.bag` | `194`        | `140784`         | `40.4`    | Arbitrary movement | Stationary         | Arbitrary movement | Arbitrary movement                 |
| `14.bag` | `209`        | `156810`         | `44.2`    | Arbitrary movement | Stationary         | Arbitrary movement | Arbitrary movement                 |
| `15.bag` | `200`        | `150139`         | `42.3`    | Arbitrary movement | Stationary         | Arbitrary movement | Arbitrary movement                 |
| `16.bag` | `213`        | `159518`         | `44.9`    | Arbitrary movement | Arbitrary movement | Arbitrary movement | Trial #1, arbitrary movement       |
| `17.bag` | `221`        | `165792`         | `46.7`    | Arbitrary movement | Arbitrary movement | Arbitrary movement | Trial #2, arbitrary movement       |
| `18.bag` | `210`        | `157407`         | `44.3`    | Arbitrary movement | Arbitrary movement | Arbitrary movement | Trial #3, arbitrary movement       |
| `19.bag` | `243`        | `182418`         | `51.4`    | Arbitrary movement | Arbitrary movement | Arbitrary movement | Trial #4, arbitrary movement       |
| `20.bag` | `206`        | `154591`         | `43.6`    | Arbitrary movement | Arbitrary movement | Arbitrary movement | Trial #5, arbitrary movement       |
| `21.bag` | `248`        | `185571`         | `52.3`    | Patrol CW rot      | Patrol CW rot      | Patrol CW rot      | Pattern movement                   |
| `22.bag` | `226`        | `169258`         | `47.6`    | Patrol CCW rot     | Patrol CCW rot     | Patrol CCW rot     | Pattern movement                   |
