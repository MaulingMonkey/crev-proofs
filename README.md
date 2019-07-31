<!-- CREV_README_MARKER_V0 - Please don't remove this first line, or `crev` might overwrite this file.  -->

# Proof Repository

This git repository is used a [Crev Proof
Repository](https://github.com/dpc/crev/wiki/Proof-Repository).

<!-- Feel free to customize this file below this line -->

# My use

I mostly care about malicious actors gaining access to data, or causing data loss.  So, any kind of RCE is a
concern (buffer overflows, SQL or shell injection attacks, network exposed commands, etc.) as is unsound code,
as it may be leveraged to create RCEs.  In code, this means paying special attention to:

* Test Coverage
* Fuzzing Coverage
* `unsafe` code
* FFI types and definitions
* `std::process::Command` use
* `std::fs::*`, `std::path::*`, or other filesystem use (possible data exfil, user controlled data)
* `std::net::*` or other network use (possible data exfil, user controlled data)
* `std::io::*` use (although these are usually mostly fine)
* `std::os::*` equivalents to the above.

I care less about "mere" Denial of Service attacks, even if those are still exploitable to ransom businesses,
although intentional vulnerabilities will still be grounds for completely distrusting their author.

# Personal Trust Criteria

Subject to change.

| trust     | criteria  |
| --------- | --------- |
| high      | Myself
| medium    | People I know offline
| low       | People I know online
| none      | People I don't know
| distrust  | People I believe have written malicious code, or have simply written far too much unsound code without good reason

# Personal Review Criteria

Subject to change.

| rating    | criteria |
| --------- | -------- |
| strong    | 100% safe code, good docs, good tests
| positive  | 100% sound code, good docs, good tests (FFI crates excepted on the docs/tests front.)
| neutral   | History of soundness issues, or possibly just rife enough with unsafe without having sufficient test coverage.
| negative  | Current soundness issues, or a history of poor responses to soundness issues
| dangerous | Current soundness issues, or a history of poor responses to soundness issues

# Official Trust Criteria

| trust     | criteria |
| --------- | -------- |
| high      | "for most practically purposes, I trust this ID as much or more than myself" eg. "my dayjob ID", "known and reputatable expert", "employee within my team"
| medium    | typical, normal level of trust
| low       | "I have some reservations about trusting this entity"
| none      | "I don't actually trust this entity"; use to revoke trust (or distrust) from a previously issued Trust Proof
| distrust  | "I distrust this person and so should you"

# Official Review Criteria

| rating    | criteria |
| --------- | -------- |
| strong    | secure and good in all respects, for all applications
| positive  | secure and ok to use; possibly minor issues
| neutral   | secure but with flaws
| negative  | severe flaws and not ok for production usage
| dangerous | unsafe to use; severe flaws and/or possibly malicious

| thoroughness | criteria |
| ------------ | -------- |
| high      | long, deep, focused review - possibly as a part of a formal security review; "hour or more per file"
| medium    | a standard, focused code review of a decent depth; "~15 minutes per file"
| low       | low intensity review: "~2 minutes per file"
| none      | no review, incomplete review, or just skimming; "seconds per file"

| understanding | criteria  |
| ------------- | --------- |
| high          | complete understanding
| medium        | good understanding
| low           | some parts are unclear
| none          | lack of understanding











## Unsafe Code

## FFI Code

## 
