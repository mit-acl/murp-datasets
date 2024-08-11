# parsed

## File Organization

* Folder names corresponds to trial number -- i.e., `01`-`22`
* Filenames are of the form `TRIAL_base-A_targ-B_win-W_step-S.csv` where:
    * `TRIAL` corresponds to trial number -- i.e., `01`-`22`
    * `A` corresponds to base's agent number -- i.e., `1`-`3`
    * `B` corresponds to target's agent number -- i.e., `1`-`3` and `A != B`
    * `W` is moving average filter window size [s] -- i.e., here either `0` (raw) or `1` second window length
    * `S` is window step size [s] -- i.e., here either `0` (raw) or `1` second window step
* Agent numbers are assigned as:
    * `1`: `acl-beta`
    * `2`: `acl-alpha`
    * `3`: `acl-delta`


## CSV Data
| Field      | Description | 
| ---------- | ----------- |
| `t`        | time [s] since the beginning of the data collect |
| `x`        | rel x [m] from base to target |
| `y`        | rel y [m] from base to target |
| `z`        | rel z [m] from base to target |
| `roll`     | rel roll [deg] from base to target |
| `pitch`    | rel pitch [deg] from base to target |
| `yaw`      | rel yaw [deg] from base to target |
| `A_x`      | abs x [m] of base in mocap |
| `A_y`      | abs y [m] of base in mocap |
| `A_z`      | abs z [m] of base in mocap |
| `A_roll`   | abs roll [deg] of base in mocap |
| `A_pitch`  | abs pitch [deg] of base in mocap |
| `A_yaw`    | abs yaw [deg] of base in mocap |
| `B_x`      | abs x [m] of target in mocap |
| `B_y`      | abs y [m] of target in mocap |
| `B_z`      | abs z [m] of target in mocap |
| `B_roll`   | abs roll [deg] of target in mocap |
| `B_pitch`  | abs pitch [deg] of target in mocap |
| `B_yaw`    | abs yaw [deg] of target in mocap |
| `I_J`      | raw measurement [m] between base's `I`th and target's `J`th antenna |
| `I_J_t`    | true distance [m] between base's `I`th antenna and target's `J`th antenna |
| `I_J_err`  | error in measurement [m], `I_J_err` = `I_J` - `I_J_t` |
| `r`        | mean of raw measurements [m] |
| `r_t`      | mean of true distances [m] between base and target |
| `r_err`    | error in `r` [m], `r_err` = `r` - `r_t` |
| `rho`      | radius [m] of `x`,`y`,`z` in spherical coordinates |
| `az`       | azimuth [deg] of `x`,`y`,`z` in spherical coordinates |
| `el`       | elevation [deg] of `x`,`y`,`z` in spherical coordinates |

where:
* `I` is a number from 1-6 corresponding to base's `I`th antenna
* `J` is a number from 1-6 corresponding to target's `J`th antenna
