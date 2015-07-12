Test-Driven Development: My Way!
################################
:date: 2013-10-12 14:13
:author: curlyreggie
:category: Uncategorized
:tags: Code, Development, Software, Testing
:slug: test-driven-development-my-way
:status: published

It was a fun day. My tech lead just freaked out with the way I started
to think - repetitive, narrowed and complicated. When you have a simple
requirement to turn to code, I sat there generating data using code!
When the `use-case <http://en.wikipedia.org/wiki/Use_case>`__ is to be
tested, is it worth to sit and generalize code rather than taking sample
data-sets directly? And what if, after hours of coding such a case, you
find that it was fundamentally wrong?

After pissing out people, I crashed into `test-driven
development <http://en.wikipedia.org/wiki/Test-driven_development>`__. I
have no idea with it's literal intent is, but it might be to see if you
write according to use-cases and not in a general fashion all the time.
The approach simply rocks, as you narrow down to your need and not to
any dependencies. No chains. Not to external factors. Just plain,
functional development.

Always break the need to direct samples, not code for them
----------------------------------------------------------

I totally irritated my senior here. He kept on insisting to use hard
values but there I was, using the general data-set code. And then it
boomed him off. Unnecessary complications of writing lines and lines of
code can lead to a basic leak in achieving the purpose. Just take a
simple set to begin with. It can be a
`HashMap <http://en.wikipedia.org/wiki/Hash_table>`__, a Dictionary, an
array or a list. Just that. And fill in random, hard-coded data.

Never code for random data! You may be handling a lot of data but not
the intended data. And, you lose most of the use-cases.

Develop functions for samples. Generalize them later.
-----------------------------------------------------

Instead of worrying about sample-generating code which won't be used at
all later, why not focus on what objective you're intending to? The
input set, operation(s) and the net result? There are implications in
these. The use-case handling gets freakier. Change the samples, and the
module behaves strangely. Add more lines inside, function crashes.
Dependencies, external and internal blow up. And you thought input
handling can do all of it. It was just the beginning.

Test, Test and er.. Test.
-------------------------

Module development isn't easy. You've to address all of the various
issues. And the solution? Testing. Test your functions. Change inputs.
Change behavior. Comment code in between, see the difference. TEST ALL
OF IT MANUALLY!! Automate these only if you've time. Use asserts to
crash. Check how your code can be integrated into the main system after
achieving success and drinking beer.

And yes, test the main system after integration. The same old dependency
problem, you see. And drink more to that.

Ask for help, even if you're a geek
-----------------------------------

Internet was never this friendlier before. Are you looking up the
correct sources for help? Are you using too much of unnecessary
thinking? Can a single line solve your problem? Direct documentation
look up is waste. Nobody has the time to sit, understand and then use
their brains to get the problem solved, \ *unless *\ there's no direct
help. You might not be searching properly either. Helpers blame
questioners for this sole reason.

The above should do your objective. Trust me, it cut down my working
time to a quarter.

TDD, my style. Bye.

 
