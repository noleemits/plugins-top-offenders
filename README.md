# WordPress Memory Usage Logger

This lightweight debug utility logs memory usage, peak usage, and the active plugins during each WordPress admin request. It's designed to help identify plugins or requests that consume excessive memory, which may slow down or crash your site.

---

## 🚀 Features

- Logs final memory usage and peak memory usage on each admin request.
- Logs the currently active plugins for correlation.
- Logs the request URI and current user for context.
- Saves all data to a custom log file (`wp-content/debug-memory.log`).
- Only runs for users with `manage_options` capability (admins).
- Runs on the `shutdown` hook for accurate profiling at the end of each request.

---

## 📂 Installation

1. Drop the code into your `functions.php`, a custom plugin, or your personal debugging mu-plugin.
2. Make sure `WP_CONTENT_DIR` is writable — the log file will be saved at:
