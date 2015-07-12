Tuning Growth
#############
:date: 2013-11-22 11:03
:author: curlyreggie
:category: Uncategorized
:slug: tuning-growth
:status: published

One of the most important faces of Computing is coding. We all tend to
code, code and code for the list of growing requirements all the time.
And there's developmental testing coupled with unit, function,
integration and regression tests to add to the load. If we're involved
in a huge project requiring thousands of lines of code, the coding phase
grows not just to the desktop phase but on a larger version. We
eventually get into a place where a data-center (read a centralized
database) and a web-server comes into foray of managing things. Things
are getting complicated.

Switch to \ `Server
Computing <http://en.wikipedia.org/wiki/Server_%28computing%29>`__. All
work is now zoomed into the server as an epicenter with the changes
leading to alterations (or repercussions) in the business logic. That's
when two important layers of Computing can lend a helping hand -
`Scalability <http://en.wikipedia.org/wiki/Scalability>`__ and
`Performance
Tuning <http://en.wikipedia.org/wiki/Performance_tuning>`__. Often,
these are ignored in a small company due to extreme workloads, but the
bigger ones, take them very seriously. We've seen dedicated teams of
huge sizes for a single process handler, haven't we?

Scalability. Means of making servers handle more user/process requests
from a meagre count of a thousand to upwards infinitium, process more
tasks and manage `databases <http://en.wikipedia.org/wiki/Database>`__
in parallel. This leads to a bigger number of machines to operate. But
the situation goes out of hand when there are too many processes on a
single machine - computations, database interactions and request
handling jobs, all working in parallel. If one process takes an extra
millisecond to operate, the rest of the dominoes fall, server queue
length overflows, web-server stop to respond, continuous incoming
requests fall back loosing data and the system breaks. Scalability can
be a huge factor where, the solution lies in expanding servers based on
tasks. Segregation is a big relief to the main guy where he is off
loaded with the entire process architecture. All he might be doing is
load balancing the requests based on the request type and leading that
task to the server handling that particular type of request. Database
segregation is also mandatory - split the databases on a live record
base based on a prefixed date boundary (live-caching) and transfer the
older data to an archived database (records that are not that "useful"
for the current objective, but are required for the business logic in
longer terms), cluster databases for handling fetch requests and
modularize based on growing time for insertions. Web-servers can also
follow similarly - one handling complex computations for fetch requests
asynchronously (read higher thread management), another processing
computations for record-insertions synchronously. One is managing these
two and returning responses back to clients directly. Dedicated `load
balancers <http://en.wikipedia.org/wiki/Load_balancing_%28computing%29>`__
can switch databases/servers based on load factors, maintenance
schedules, replications and unaccounted down-times. The system grows in
size, but is easily managed by a few. The swarm architecture, in short.

On the other hand, keeping in mind, the crunch in "costs" to the company
which cut down on supplies, the challenge lies in the way of making a
single (or two) servers, smarter - optimized process handling, reduced
task overheads, dedicated job management and a scheduled
auto-maintenance. The beauty of performance tuning might not be
observable but can have seriously good results. Your server begins to
get more robust, handles things better than traditional methods and
lives up to it's life span in full. A simple example was of implementing
an HTTP server to a
`Django <http://en.wikipedia.org/wiki/Django_%28web_framework%29>`__
project. The time taken to process incoming requests, zoomed to almost
ten times compared to Django's pathetic inbuilt web-server handlers. Or
take the case of database indexes. A secondary index on a table made
life much easier by faster process of incoming POST requests. A factor
of 20. Of course, there are trade-offs in these as we need more storage
space but these can be minimal.

Balancing these two can be a challenge in itself. Of course, testing all
of the above with some peer consultations and expert opinions can be a
daunting factor. The kind of opinion you go with, can even lead to your
rise or fall of your business, unless you pick more and more reading of
them.
