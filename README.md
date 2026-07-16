<p align="center">
  <img src="logo.svg" width="96" alt="IIS Log Viewer logo">
</p>

<h1 align="center">IIS Log Viewer</h1>

<p align="center">
  A single-file, fully client-side viewer for W3C IIS log files —
  built for fast IP and user-agent triage.
</p>

---

## What it does

Drop one or more IIS log files (W3C extended format) into the page and explore them without anything leaving your browser. No server, no upload, no dependencies — just open `index.html`.

**Features**

- Filter, sort, and full-text search across requests
- Client IP and user-agent analysis views
- Timeline histogram with drag-to-select time window
- IIS substatus and Win32 status code decoding (e.g. `500.19`, `401.3`)
- Endpoint aggregation tab for spotting hot or failing routes

## Usage

**Online:** open the [GitHub Pages site](https://vansh-shah.github.io/iis-log-viewer/).

**Offline:** clone or download the repo and open `index.html` in any modern browser. Works from a file share or a locked-down support workstation — no network access required.

```
git clone https://github.com/Vansh-Shah/iis-log-viewer.git
cd iis-log-viewer
start index.html    # Windows
open index.html     # macOS
```

## Log format

Expects W3C extended log files as produced by IIS (`#Fields:` directive present). Typical location on a server:

```
%SystemDrive%\inetpub\logs\LogFiles\W3SVC<siteId>\u_ex*.log
```

## Privacy

All parsing happens in your browser. Log files are never transmitted anywhere, which makes this safe to use with production logs containing client IPs.

## License

[MIT](LICENSE)
