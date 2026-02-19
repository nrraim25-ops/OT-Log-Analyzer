# OT-Log-Analyzer
A Python-based log parser and analyzer for OT/SCADA systems. 

Parses structured log files from industrial devices — PLCs, RTUs, Firewalls, and HMIs — extracts severity levels, detects anomalies based on hourly activity spikes, and generates a summary report.

What It Does
Parses log entries in SCADA format (timestamp device severity message) using precompiled regex. Falls back to generic key=value parsing for non-standard lines. Extracts IP addresses, timestamps, and severity levels (DEBUG, INFO, WARNING, ERROR, CRITICAL). Tracks error rate, warning rate, and per-device event counts. Detects anomalous hours where activity exceeds mean + 2 standard deviations. Outputs a text or JSON report and an optional activity plot.
