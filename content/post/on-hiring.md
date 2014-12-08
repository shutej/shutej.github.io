+++
date = "2014-12-08"
author = "Jeremy Shute"
title = "On Hiring"
+++

I learned how to hire while I worked for Google, a company that has an enviable
number of great engineers.  They frequently rank in the [top places to
work](http://www.greatplacetowork.com/best-companies/100-best-companies-to-work-for),
but when I left the thing I missed the most was not the free food or the
generous vacation.  I missed the people.

How did Google get so many great engineers?  I've heard it said that great
problems attract great people.  I've also heard it said that great people
attract great people.  I actually think they just hire great people.

So, if you want to emulate their success, what should you do?

Whenever you measure a population, the [bell
curve](http://en.wikipedia.org/wiki/Normal_distribution) is bound to come up.
The bell curve is used to measure underlying processes that have an outcome
that's the sum of many small random events.  You can probably safely assume
that your measure of "employee quality" will look like a bell curve.  You can
also probably safely assume your applicant's interview scores will also look
like a bell curve.

By changing policies and processes, you can increase the accuracy of the hiring
decision.  The name of the game here is increasing the correlation between
"employee quality" and applicant interview score.  They'll both still look like
a bell curve when viewed independently, but when plotted against one another
the relationship becomes obvious.

{{% imgresponsive "/images/correlation.png" %}}

By changing the number of applicants you reject, you bias the result toward the
ones that are of "employee quality."  Notice that in the *p=0* graph above, the
right side of the graph looks like it has the same mean on the *y* axis as the
left side of the graph.  However, if you divide the *p=1* graph, the right side
will have a much higher mean than the left side.

How do these factors relate to each other?  I put together a quick random
simulation to determine exactly that.  Unfortunately at a sample size of 100 it
was too difficult to read, so the following represents what happens when hiring
1,000 employees.

{{% imgresponsive "/images/quality.png" %}}

Two things stand out to me immediately.

If you want a chance of hiring an organization that performs in the 90th+
percentile, you need an accuracy of at least 50%.  Your interview questions
need to be topical to the job function, demonstrable skills need to be
demonstrated, and you should try to get information from multiple interviewers.

But, you also need a bias of at least 75%!  In other words, you have to say
"no" to at least 3 out of 4 candidates, regardless of how accurate you think
your process is.  Looking at the slope, it's clear that bias becomes even more
important than accuracy as you try to exceed the 90th+ percentile of
performance.

Applicants should understand that great organizations are built by having high
precision but low recall.

*I don't want to belong to any club that will accept people like me as a
 member. -- Groucho Marx*