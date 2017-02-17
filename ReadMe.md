# Rust for the fun of it!

It's fun to learn Rust by porting stuff to Rust.  This is my project to port a
bunch of Apple's BSD utilities so I can have fun and learn.  And have fun.  And
learn while I have fun.  Maybe it's fun for you too.  If you think it might be
fun, tell me and I'll grant you commit access.  To contact me, either make a
dang issue, or join me on my
[RustProgramming Discord Channel](https://discord.gg/pR7hBBe)

# Fun Guidelines

- I'm targeting [shell_cmds version 198](https://opensource.apple.com/source/shell_cmds/shell_cmds-198/), because it's the shiniest at the moment.
- Lets keep the command names and flag named exactly the same.
- I don't give a flip about exact *behavior* compatibility or completeness.
- The rust code should be as *idiomatic* as possible (aka do it the Rust ), which means line-by-line
  porting is not really an option, because Rust sorta flipped C's nasty unsafe
  paradigm on its head.  So put some thought into it!
- No pull requests.  Just push to master.  You might have to pull first ;-)

# FAQ

Q. Why are you doing this?  A. For fun.  I like learning Rust this way.
Q. Why don't you just use this other existing project...? A. See last question.
Q. Will this make you rich? A. Absolutely. As soon as a wealthy patron decides
   to dump money on me because I made a pass at re-implementing ancient BSD
   utilities in Rust, I'll totally be rich.
Q. Can I play too? A. Yes. I'll even give you commit access. Hurry the heck up, it's lonely over here.

# Organization...maybe

It might work nicely to make a `src/bin/command.rs` for each `command` you want to implement.  Put a `fn main()` in it.

To run your new command: `cargo run --bin command`

If there's some *actually* duplicated or reusable code somewhere, lets put it
in a properly named library module.  Like `src/awesome.rs` or something relevant.

If there's a better way to do it, tell me about it.  Lets give it a shot.

# Status of Stuff

| Command | Status |
|---------|--------|
| true | It works flawlessly.  100% compatible.  I'm AMAZING. |
| yes | Gonna do it next. |
| Everything else | Who cares? Oh, you do? Then update this file, dangit! I'm a doctor, not a technical writer, Jim. |
