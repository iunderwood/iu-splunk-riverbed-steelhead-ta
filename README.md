iu-splunk-riverbed-steelhead-fwd
================================

Splunk for Riverbed Steelhead - Forwarding Transform

This is a self-contained Splunk application which parses log information for the interesting fields returned by the Riverbed Steelhead equipment.  Specifically, it looks for log lines which roughly match the following:

[component.LOGLEVEL} (- | a digit)

Log lines that match this expression are assigned a sourcetype of "riverbed_steelhead".

The forwarding component is a separate entity which needs to be installed on every Splunk instance that is taking input from a Riverbed device.  This is designed to be lightweight and simple for those folks who have deployed heavy forwarders.

Install the rb_steelhead_fwd directory on your input instances:

$SPLUNK_HOME\etc\apps

If you are using a Deployment server, place it here:

$SPLUNK_HOME\etc\deployment_apps