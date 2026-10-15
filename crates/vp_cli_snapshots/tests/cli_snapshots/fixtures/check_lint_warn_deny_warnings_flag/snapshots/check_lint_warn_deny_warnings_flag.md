# check_lint_warn_deny_warnings_flag

## `vp check --deny-warnings`

warnings fail the check

**Exit code:** 1

```
pass: All 3 files are correctly formatted (<duration>, <n> threads)
warn: Lint warnings found
⚠ eslint(no-console): Unexpected console statement.
   ╭─[src/index.js:2:3]
 1 │ function hello() {
 2 │   console.log("hello");
   ·   ───────────
 3 │ }
   ╰────
  help: Delete this console statement.

Found 0 errors and 1 warning in 2 files (<duration>, <n> threads)
```

## `vp check --deny-warnings --quiet`

warnings stay hidden but --deny-warnings still fails

**Exit code:** 1

```
pass: All 3 files are correctly formatted (<duration>, <n> threads)
warn: Lint warnings found

Found 0 errors and 1 warning in 2 files (<duration>, <n> threads)
```

## `vp check --deny-warnings --no-lint`

lint is skipped so there is nothing to deny

```
pass: All 3 files are correctly formatted (<duration>, <n> threads)
```
