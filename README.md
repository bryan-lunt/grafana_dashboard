# ksp_grafana_dashboard

This project uses Docker Compose to build a start a pre-configured Grafana server and a telemetry database.

The server will serve appropriate Mission Control type dashboards, customized for KSP.

Later versions may also include the code to actually get telemetry into the database, and a web interface to start/stop kRPC connections.
https://github.com/uiuc-cs-ksp/krpc_telemetry_server

If we decide later that we need custom plugins or extensions to Grafana, they should also be stored in this project if possible.

### Goals

- Nice dashboards that are useful for playing KSP (especially as a group.)
- Ease of use
- Straightforward configuration. (All non-default config files stored in this repo and easy to access/alter.)

#### 0.1.0 goals

- Basic KSP dashboard(s) using only default widgets.
	- Current mission/game/next-node time.
	- Resources
	- Thrust/Force
	- Current ISP
	- Engine temperatures
	- Atmospheric stuff. (drag, pressure, etc.)
- Preconfigured datasource.
- No login needed.
- Land on a KSP dashboard as the "Home" dashboard.

#### 0.1.1 goals

- Include the telemetry getters in this project.
- A flask or other UI for starting/stopping getters, finding the ip/port/etc of a kRPC server (running KSP game.)
	(It could be a Grafana widget/plugin/something, but only if that is easy to do, if it takes much effort, put that off to later.)

#### 0.1.2 goals

- Basic security configuration. (Bearing in mind that this is still for private/entertainment use. It will usually be run locally.)

#### other goals

- Can we have dashboards get their clock time from KSP, using the KSP game date instead of UTC or unix time?
- Can we alter the sense of time somehow to know that KSP days are 6hrs?
- Can we have multiple timeframes? A kerbol is different on each body.

#### potential plugins, etc.

- Solar-system view? (Maybe from astropy or something.)
	- With ship orbits and manouver nodes?
	- 3D? (Three.js)
- Navball?
- etc?
