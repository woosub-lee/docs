# EventLoop

EventLoops are a combination of a single DispatchQueue with a context storage.
The DispatchQueue *must* be non-concurrent to ensure thread safety.

In Vapor 3, all HTTP Requests are ran on an EventLoop. If you want access to the EventLoop you can do so through a [Worker](../worker.md) such as [Request](../http/request.md).

## Context

The context of an EventLoop is used to store thread-unsafe entities such as [database drivers](../getting-started/databases.md), [ORMs](../fluent/getting-started/package.md) and [caches](../getting-started/cache.md).

The contexts are accessed through an extension on the `Worker` protocol to ensure a good user experience. EventLoop itself is also conformant to `Worker`.
