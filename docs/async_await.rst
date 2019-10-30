.. _async_await:

Using async and await
=====================

Routes, error handlers, before request, after request, and teardown
functions can all be coroutines i.e.::

    @app.route("/")
    async def index():
        return await ...

This allows asyncio based libraries to be used, but comes with a
performance cost over using standard synchronous functions. If your
codebase is fully async `Quart <https://gitlab.com/pgjones/quart>`_
may be a better choice.
