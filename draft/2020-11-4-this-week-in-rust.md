Title: This Week in Rust 363
Number: 363
Date: 2020-11-04
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta: safety, concurrency, and speed.
This is a weekly summary of its progress and community.
Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us a pull request](https://github.com/emberian/this-week-in-rust).
Want to get involved? [We love contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/emberian/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/emberian/this-week-in-rust/pulls).

# Updates from Rust Community

### Official

### Tooling

### Observations/Thoughts

### Learn Rust

### Project Updates

### Miscellaneous

# Crate of the Week

This week's crate is [rust-gpu](https://github.com/EmbarkStudios/rust-gpu) from Embark Studios, a system to compile Rust code into Vulkan graphics shaders (with other shader types to follow).

Thanks to [Vlad Frolov](https://users.rust-lang.org/t/crate-of-the-week/2704/831) for the suggestion!

[Submit your suggestions and votes for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

400 pull requests were [merged in the last week][merged]

[merged]: https://github.com/search?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2020-10-19..2020-10-26

* [tweak `if let` suggestion to be more liberal with suggestion and to not ICE](https://github.com/rust-lang/rust/pull/77283)
* [reduce diagram mess in 'match arms have incompatible types' error](https://github.com/rust-lang/rust/pull/78255)
* [tweak match arm semicolon removal suggestion to account for futures](https://github.com/rust-lang/rust/pull/78214)
* [explain where the closure return type was inferred](https://github.com/rust-lang/rust/pull/78235)
* [rewrite `collect_tokens` implementations to use a flattened buffer](https://github.com/rust-lang/rust/pull/77250)
* [fix trait solving ICEs](https://github.com/rust-lang/rust/pull/77720)
* [stop promoting union field accesses in 'const'](https://github.com/rust-lang/rust/pull/77526)
* [ensure that statics are inhabited](https://github.com/rust-lang/rust/pull/78324)
* [rustc_mir: track inlined callees in `SourceScopeData`](https://github.com/rust-lang/rust/pull/68965)
* [optimize const value interning for ZST types](https://github.com/rust-lang/rust/pull/78061)
* [calculate visibilities once in resolve](https://github.com/rust-lang/rust/pull/78077)
* [mir-opt: disable MatchBranchSimplification](https://github.com/rust-lang/rust/pull/78151)
* [implement `TryFrom` between `NonZero` types](https://github.com/rust-lang/rust/pull/77339)
* [add `Pin::static_ref`, `static_mut`](https://github.com/rust-lang/rust/pull/77726)
* [support custom allocators in `Box`](https://github.com/rust-lang/rust/pull/77187)
* [hashbrown: parametrize RawTable, HashSet and HashMap over an allocator](https://github.com/rust-lang/hashbrown/pull/133)
* [rustdoc: greatly improve display for small mobile devices screens](https://github.com/rust-lang/rust/pull/78084)
* [clippy: add linter for a single element for loop](https://github.com/rust-lang/rust-clippy/pull/6109)
* [clippy: add lint for `&mut Mutex::lock`](https://github.com/rust-lang/rust-clippy/pull/6103)
* [clippy: add new lint for undropped `ManuallyDrop` values](https://github.com/rust-lang/rust-clippy/pull/6181)
* [clippy: lint unnecessary int-to-int and float-to-float casts](https://github.com/rust-lang/rust-clippy/pull/6187)

## Rust Compiler Performance Triage

* [2020-10-27](https://github.com/rust-lang/rustc-perf/blob/master/triage/2020-10-27.md):
0 Regressions, 2 Improvements, 3 Mixed

See the [full report](https://github.com/rust-lang/rustc-perf/blob/master/triage/2020-10-27.md) for more.

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments) process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

* [Destructuring assignment](https://github.com/rust-lang/rfcs/pull/2909)
* [RFC: Reading into uninitialized buffers](https://github.com/rust-lang/rfcs/pull/2930)
* [RFC: Promote aarch64-unknown-linux-gnu to a Tier-1 Rust target](https://github.com/rust-lang/rfcs/pull/2959)

## Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now.

### [RFCs](https://github.com/rust-lang/rfcs/labels/final-comment-period)
* [YieldSafe auto trait](https://github.com/rust-lang/rfcs/pull/2890)
* [Variadic tuples](https://github.com/rust-lang/rfcs/pull/2775)
* [RFC for a match based surface syntax to get pointer-to-field](https://github.com/rust-lang/rfcs/pull/2666)

### [Tracking Issues & PRs](https://github.com/rust-lang/rust/labels/final-comment-period)
* [disposition: merge] [Allow making `RUSTC_BOOTSTRAP` conditional on the crate name](https://github.com/rust-lang/rust/pull/77802)
* [disposition: merge] [consider assignments of union field of ManuallyDrop type safe](https://github.com/rust-lang/rust/pull/78068)
* [disposition: merge] [Define `fs::hard_link` to not follow symlinks.](https://github.com/rust-lang/rust/pull/78026)
* [disposition: merge] [repr(transparent) on generic type skips "exactly one non-zero-sized field" check](https://github.com/rust-lang/rust/issues/77841)
* [disposition: merge] [Rename/Deprecate LayoutErr in favor of LayoutError](https://github.com/rust-lang/rust/pull/77691)
* [disposition: merge] [Tracking Issue for raw_ref_macros](https://github.com/rust-lang/rust/issues/73394)

## New RFCs
* [RFC: Plan to make core and std's panic identical.](https://github.com/rust-lang/rfcs/pull/3007)

# Upcoming Events

### Online
* [October 29. Berlin, DE - Rust Hack and Learn - Berline.rs](https://www.meetup.com/opentechschool-berlin/events/txcprrybcnbmc/)
* [November 4. Johannesburg, ZA - Monthly Joburg Rust Chat! - Johannesburg Rust Meetup](https://www.meetup.com/Johannesburg-Rust-Meetup/events/274142374/)
* [November 4. Dublin, IE - Rust Dublin November - Rust Dublin](https://www.meetup.com/Rust-Dublin/events/274202454/)
* [November 4. Indianapolis, IN, US - Indy.rs - with Social Distancing - Indy.rs](https://www.meetup.com/indyrs/events/jhfstrybcpbgb/)
* [November 7 & 8, Global, RustFest Global](https://rustfest.global/)
* [November 10, Seattle, WA, US - Seattle Rust Meetup](https://www.meetup.com/Seattle-Rust-Meetup/events/gskksrybcpbnb/)

## Asia Pacific
* [November 1. Auckland, NZ - Rust meetup - Introduction to Rust - Rust AKL](https://www.meetup.com/rust-akl/events/266876718/)

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Please remember to add a link to the event too.
Email the [Rust Community Team][community] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[community]: mailto:community-team@rust-lang.org

# Rust Jobs

* [Senior Software Engineer - Rust at Immunant (Remote within United States)](https://immunant.com/jobs)

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

> what many devs often miss initially when talking about Rust is that it isn't just about the design & details of the language (which is great), Rust's super power is that in combination with its fantastic community & ecosystem, and the amazing friendly people that create & form it

– [Johann Andersson on twitter](https://mobile.twitter.com/repi)

llogiq is pretty pleased with his own suggestion and unanimously voted for it.

[Please submit quotes and vote for next week!](https://users.rust-lang.org/t/twir-quote-of-the-week/328)

*This Week in Rust is edited by: [nellshamrell](https://github.com/nellshamrell), [llogiq](https://github.com/llogiq), and [cdmistman](https://github.com/cdmistman).*

<small>[Discuss on r/rust](https://www.reddit.com/r/rust/comments/jk35ha/this_week_in_rust_362/)</small>
