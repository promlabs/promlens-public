## 0.9.0 / 2020-09-07

* [FEATURE]: The Monaco-based PromQL text editor has been completely replaced with a CodeMirror-Next-based one. This introduces a full parser system that allows for **contextual autocompletion of metric names, label names/values, function names, operators, and other keywords**. It also introduces an **offline linter, showing many common PromQL errors** directly in the text input field.
* [FEATURE]: Show query time for each tree node.
* [FEATURE]: Add global settings menu to customize the per-node information display (query evaluation time, number of results, and labels).
* [FEATURE]: Show metric `HELP` and `TYPE` metadata in the "Explain" tab for vector selectors.
* [FEATURE]: Add support for the new human-friendly duration syntax (e.g. `1h30m`) introduced in Prometheus 2.21.0 (see https://github.com/prometheus/prometheus/pull/7713 and https://github.com/prometheus/prometheus/pull/7833).
* [FEATURE]: Add support for the new `group()` aggregator introduced in Prometheus 2.20.0 (see https://github.com/prometheus/prometheus/pull/7480).
* [ENHANCEMENT]: Don't show a quick action button to add `sum()` around nodes that only return one time series.
* [ENHANCEMENT]: Update function documentations from upstream Prometheus project.
* [ENHANCEMENT]: Improve alignment and rendering of quick action buttons.
* [BUGFIX]: Use correct back/forward skip duration for the instant query timestamp selector.
* [BUGFIX]: Fix bug in applying URL-supplied Prometheus server settings when there is also a default Grafana datasource.
* [BUGFIX]: Don't display a license error when the page configuration cannot be loaded.
* [MISC]: Updated PromLens logo, dropped the "Preview" text.
