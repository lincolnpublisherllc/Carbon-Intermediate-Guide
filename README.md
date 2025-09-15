How folders are named

chapter_XX_<slug>/ — chapter number and title slug

Each chapter includes a main.carbon entry script and, where relevant, additional examples under examples/

Per-file explanations
main.carbon (present in every chapter)

Entry example tailored to the chapter’s topic. Prints a short banner, defines a tiny helper (add(a, b)), and demonstrates control flow. Use it as the minimal, runnable-style snippet for the chapter.

examples/io_example.carbon (if present)

Text file I/O. Demonstrates creating and reading a file using write_file and read_file. It writes hello.txt and prints its contents.
Concepts: opening/closing files, reading, writing, simple error-free flow.

examples/concurrency.carbon (if present)

Threads & shared state. Spawns two worker threads that increment a shared Counter, then calls join() and prints the final count.
Concepts: basic threading model, sharing data, work splitting, synchronization ideas (teaching level).

examples/data_structures.carbon (if present)

Collections & graph traversal. Shows a set, dictionary (map), and a tuple, then performs a tiny BFS over an adjacency map.
Concepts: sets vs. maps, tuple indexing, queue-style processing, visited sets.

examples/testing.carbon (if present)

Tiny test harness. Implements assert_eq(actual, expected, msg) and tests a simple add function, printing pass/fail-style output.
Concepts: assertions, fast feedback loop, organizing micro-tests.

examples/database.carbon (if present)

Mock database layer. Provides a Db.query(sql) that returns sample rows and iterates them.
Concepts: data access abstraction, row iteration, separation of concerns (scaffold for real DBs).

examples/performance.carbon (if present)

Micro-benchmark target. Implements sum_loop(n) accumulation to illustrate where hot loops live and what you’d measure/tune.
Concepts: algorithmic cost, hotspots, guardrails for profiling.

Typical chapter layout

Every chapter contains:

README.md — short overview of what that chapter’s code demonstrates

main.carbon — entry example

examples/ — optional, contains one or more of the files listed above depending on the chapter focus

If your chapter includes I/O, concurrency, data structures, testing, databases, or performance topics, you’ll find the corresponding example file(s) inside examples/.

Running the snippets

These samples are teaching aids; adapt to your compiler/runtime if you’re experimenting hands-on. The structure is intentionally small and focused so you can copy/paste into your environment.

Notes

Names and folder slugs follow the manuscript’s chapter list or a sensible default outline.

If you’d like sub-section-level samples (e.g., 2.3, 4.2), I can add those as examples/section_2_3_<topic>.carbon, etc.
