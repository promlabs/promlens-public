## 0.10.0 / 2020-10-19

* [FEATURE]: In autocomplete, show the metric type and docstring for every metric (provided the datasource can provide them).
* [FEATURE]: In autocomplete, show help strings for functions, keywords, aggregators, etc..
* [FEATURE]: Add new metrics explorer, which allows showing and filtering all metric names, showing their type and docstring, and inserting/copying metric names.
* [FEATURE]: Add new `q` URL query parameter which allows supplying an initial query, e.g. `?q=up`. This can be used to generate direct links to queries without having to persist a shared page link.
* [FEATURE]: Show an alert to first-time visitors with an option to view an example query page. Dismissal of the alert is saved in local storage.
* [FEATURE]: Allow enabling/disabling the text editor's syntax highlighting, autocompletion, and linting features, from the global settings menu.
* [ENHANCEMENT]: Speed up autocompleting of label names and values on metrics with many series.
* [ENHANCEMENT]: Clean up the textual PromQL representation of nodes in the tree view to omit child indicators rather than rendering them as an ellipsis (…).
* [ENHANCEMENT]: Make the tree node edit buttons clearer by adding textual labels.
* [ENHANCEMENT]: Always display tree node edit buttons on placeholder nodes, not just when hovering over the node.
* [ENHANCEMENT]: Improve styling minorly throughout the app.
* [ENHANCEMENT]: Include correct monospace font in app, so that monospace code looks the same everywhere.
* [ENHANCEMENT]: Autocomplete more PromQL grammatical cases and do so more correctly.
* [ENHANCEMENT]: Generally improved editor and autocomplete styling consistency across browsers.
* [ENHANCEMENT]: Autocomplete dropdowns now don't get cut off at the bottom when the height of the current query view is too short to contain the full dropdown.

## 0.9.1 / 2020-09-08

* [BUGFIX]: Pull in changes from latest `codemirror-promql` package that make snippet placeholder texts syntactically problematic for PromQL (by not including `<` and `>` around the placeholder text). Besides avoiding extraneous linter errors, this avoids a JavaScript error in the CodeMirror Next linter which could happen during autocomplete in a broken expression, and which still needs to be tracked down upstream.

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
