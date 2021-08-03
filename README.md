# checs

This project is a fork of [hecs](https://github.com/Ralith/hecs), but designed for concurrent access.
Whereas hecs would panic or error when illegally borrowing an archetype more than once, this version
will either await a lock in a multithreaded scenario, or deadlock if the same thread attempts to perform
an illegal double borrow. View the original repository for an overview of how hecs works.
