# RFC

This is a collection of Request For Comments for Static Tap.  Please open
issues via GitHub's Issues system.  Changes that are accepted will move
forward as Pull Requests, which will update this RFC.  Once the RFC
reaches `v1.0.0`, it will be finalized and engineering work will
commence, mapping to this RFC.  Any updates to this RFC which do not
constitute significant rewrites will be released as `v1.0.x`, while
specifications which are fundamentally new will be released as `v1.x.y`.

Latest RFC: RFC 012

Next RFC: RFC 013

# Static Tap?

Static Tap is the Working Name for a project which aims to provide
a common interaction language for network devices.  The name is up for
debate--see [#1][1].

## Goals

Taken largely from a [blog post I recently wrote][2]:

> My goal is to create an API which, at its core, simply queries a
> database and returns the results of the query in JSON, XML, or the
> next format of the future. There must be a component to populate
> that database, and this component should operate independently of the
> API. It should be event-driven or have strong multi-threading.
> The component that updates the database must be entirely language
> agnostic.  A specification for each data structure must be defined
> that all database-updating components should conform to.  None of this
> should be taken to indicate that this system should reinvent the
> wheel.  There are many systems that already exist to collect and/or
> graph historical data of varying types.  Static Tap (working name)
> does not aim to maintain historical data of any sort at this stage.

## Versioning

For `vx.y.z`:

- x: major
- y: minor
- z: bug/hotfix

Taking `v1.2.3` as an example, `1` is the major version, `2` is the
minor version, and `3` is the bugfix or hotfix version.

## Technology

Selecting the appropriate technology stack is imperative.  It's
a decision that Static Tap (working name) will have to live with for, at
the least, `v1.x.y`, the lifetime of which is currently undetermined
(see [#2][3]).

There are multiple areas of the system to consider:

- Database: See [#3][4]
- API Backend Language: See [#4][5]
- Front End: See [#5][6]
- Backend Updater Language: See [#6][7]

## Administrative

The technology tells half of the story of success.  The other half is
how people work.  Here are some items to consider:

- Workflow Management: See [#7][8]
- Collaboration: See [#8][9]
- Ticket Management: See [#9][10]
- Life Cycle: See [#2][3]
- Release Cycle: See [#10][11]

## API Route Structure

We also need to consider the structure of the API.  There is a [working
document][12] for the API route structure.  Also see [#11][13].

## Database Tables

Each of the database tables will require careful planning and
consideration.  RFCs for database tables are on hold until [#3][4] is
resolved.

# How You Can Help

At this stage, there are many issues related to the technology stack
that will be used.  Your input is invaluable if you have any practical
experience in any programming language or database administration.  Even
if you don't, there are several RFCs that you can comment on to improve
this project and shape its future.  I've broken them down below.  All
you have to do is comment on the relevant issues!

### How to Help if You Aren't a Programmer

- [RFC 001][1] - Project Name: The current working name is awful.  Help
  influence the future name of the project!
- [RFC 002][2] - Life Cycle: How long should a release be supported?
- [RFC 005][6] - Frontend System: Should I (or we?) spend time on
  a frontend application that consumes the API, or should I (we?) focus
  solely on the API itself?
- [RFC 010][11] - Release Cycle: How frequently should we
  (realistically) release?

Open a new RFC!  I can't think of everything.  If you have an idea, open
a new GitHub Issue with a title of `RFC xyz: Summary`, where `xyz` is
the next sequential RFC number.  The current and next RFC numbers are at
the top of this document.

As the other RFCs are finalized, there will be _many_ more opportunities
for those who are not programmers to help.

### How to Help if You Are a Programmer

Right now, almost every RFC is an architecture/technology stack
decision.  Pick one (or many!) and start giving your input.

# About Me

I've wanted to do this for a long time.  I previously lacked the
technical skill to make it happen.  Honestly, I still lack that ability.
It seems that no one else is going to make this tool for me, though, and
the best way that I can think of to bring it to fruition is by
open-sourcing it.

I'm a network engineer and sometimes I write code.  I automate networks
and I do network integrations (and sometimes I get really scary and
automate network integrations).  My two strongest passions are
automation and analytics/insight.

You can reach me via e-mail at tyler@oss-stack.io.

[1]: ../../issues/1 "RFC 001: Project Name"
[2]: https://oss-stack.io/blog/network-status-api-part-2/ "Network Status API Part 2"
[3]: ../../issues/2 "RFC 002: Life Cycle"
[4]: ../../issues/3 "RFC 003: Database Selection"
[5]: ../../issues/4 "RFC 004: API Backend Language Selection"
[6]: ../../issues/5 "RFC 005: Front End System"
[7]: ../../issues/6 "RFC 006: Backend Updater Language Selection"
[8]: ../../issues/7 "RFC 007: Workflow Management"
[9]: ../../issues/8 "RFC 008: Collaboration"
[10]: ../../issues/9 "RFC 009: Ticket Management"
[11]: ../../issues/10 "RFC 010: Release Cycle"
[12]: api.md "API Reference Document"
[13]: ../../issues/11 "RFC 011: API Route Structure"

