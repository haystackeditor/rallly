<!-- haystack:begin -->
## Haystack

After you change this app's code, or when the user asks you to check a change, run `haystack verify` before you
call the work done. It runs the app with and without the change, explores it, and reports where the change shows up
and what broke. It changes nothing, so run it without asking.

- It often takes 10 to 15 minutes: give it your longest timeout or run it in the background, and do not pipe it
  through `tail` or `head`, which hide its progress. If your command times out, run it again: it picks up the same crawl.
- Fix each bug it reports that your change caused, then run `haystack verify` again.
- If it says onboarding needs an answer, ask the user that question and file their choice with
  `haystack verify answer <question-id> <choice>`.
- Read its short report. `--json` prints the full result, often hundreds of kilobytes, for scripts;
  `haystack verify --help` explains the output and exit codes.
- If `haystack` is not installed, run each command as `npx -y @haystackeditor/cli@latest <command>`.
<!-- haystack:end -->
