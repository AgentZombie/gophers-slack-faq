# Gophers Slack FAQ

This is an _unofficial_ FAQ for the gophers slack.

## Getting Help

### Be specific

"A problem well-stated is half-solved" - Charles Kettering

Others in the slack will always know less about your problem than you do. Do your best to help them understand the problem. It's fine that you don't know what information others need to answer your question. It's fine when you can't provide all the information up front. Others can ask you clarifying questions once they have a foothold.

A great approach is to form your question like a bug report:

> I do _X_, I expect _Y_, but I'm observing _Z_ instead.

For example:

> I'm trying to assert `soi []interface{}` to `sos []string` with `sos := soi.([]string)` but the compiler tells me `invalid type assertion: soi.([]string) (non-interface type []interface {} on left)`

A specific error message is much more helpful than "When I try _x_ I get an error".

It's not uncommon that as you start to describe the problem you realize the cause. This is called [Rubber Ducking](https://en.wikipedia.org/wiki/Rubber_duck_debugging) and it's welcome.

Finally, a short demonstration of the problem on [The Go Playground](https://play.golang.org/) or [The Go Play Space](https://goplay.space/) is extremely valuable in helping others understand.

### Be concise

Details aid others in understanding your problem which helps lead to a solution. However, details that aren't contributing to the problem are distracting and make it more difficult to understand. Do your best to remove details from the question and from the example that aren't part of the question.

### Do your homework

Try to find answers to basic questions by searching before asking for help from others. We're happy to help, but responding to questions with well-documented answers is a source of fatigue for helpful gophers.

Google and other search engines should be your first stop for answers. The language is called "Go" but that's not a helpful search term so use `golang` instead. For example: `golang yaml`, `golang sort`, or `golang linter`.

Most basic questions about the language are answered in [A Tour of Go](https://tour.golang.org/) and [Effective Go](https://golang.org/doc/effective_go.html).

### Don't ask "census" questions

* Does anyone here use `x`?
* Can someone help me with `y`?
* Can I ask a question here?

Don't ask to ask or try to determine if asking your question will pay off. Just ask! If someone with the answer is watching they'll answer. You may get directed to ask in a better channel.

### Be patient

We're all volunteers and we don't have an SLA on answers. It's possible no one has the answer to your question. It may be that a few hours later someone happens to look at the channel and will respond. Be patient.

### Don't broadcast questions

Don't pose the same question in multiple channels at the same time. Try to pick the best channel for the question and post it there. If you're unsure, #general or #newbies are great choices.

## Language/Learning

### How do I get started?

[Start here](https://golang.org/doc/).

### How do I build a REST service?

There's no magic here. There are routers/frameworks to streamline some aspects of this but they make it harder to understand what's happening. See: _Which HTTP router should I use?_

## Tools

### Which editor/IDE should I use?

Editors are tools and no tool is perfect for everyone. You'll have to try different editors to decide which feels best to you. The major editors have their own channels.

## Packages

### Which HTTP router should I use?

Don't (at first). HTTP routers add complexity to your service at the very beginning, when it should be simple.

Start by doing everything with the standard library (`net/http`). Building a web service this way will help you understand what problems the routers are trying to solve, which apply to your use case, and how those tools are attempting to solve those problems. Without that kind of understanding it's very difficult to troubleshoot issues you encounter with those tools.
