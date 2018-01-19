![Twirp Logo](./logo.png)

---

Twirp is a framework for service-to-service communication emphasizing simplicity
and minimalism. It generates routing and serialization from API definition files
and lets you focus on your application's logic instead of thinking about
folderol like HTTP methods and paths and JSON.

Define your service in a
[Protobuf](https://developers.google.com/protocol-buffers/docs/proto3) file and
then Twirp autogenerates Go code with a server interface and fully functional
clients. It's similar to [gRPC](http://www.grpc.io/), but without the custom
HTTP server and transport implementations: it runs on the standard library's
extremely-well-tested-and-high-performance `net/http` Server. It can run on HTTP
1.1, not just http/2, and supports JSON clients for easy integrations across
languages

Twirp handles routing and serialization for you in a well-tested, standardized,
thoughtful way so you don't have to. Serialization and deserialization code is
error-prone and tricky, and you shouldn't be wasting your time deciding whether
it should be "POST /friends/:id/new" or "POST /:id/friend" or whatever. Just
get to the real work of building services!

Along the way, you get an autogenerated client and a simple, smart framework for
passing error messages. Nice!

For more on the motivation behind Twirp (and a comparison to REST APIs and gRPC), the
[announcement blog post](https://blog.twitch.tv/twirp-a-sweet-new-rpc-framework-for-go-5f2febbf35f)
is a good read.

### Installation
Use `go get` to install the Go client-and-server generator:

```
go get github.com/twitchtv/twirp/protoc-gen-twirp
```

You will also need:
 - [protoc](https://github.com/golang/protobuf), the protobuf compiler. You need
   version 3+.
 - [github.com/golang/protobuf/protoc-gen-go](https://github.com/golang/protobuf/),
   the Go protobuf generator plugin. Get this with `go get`.

### Documentation
Thorough documentation is [on the wiki](https://github.com/twitchtv/twirp/wiki).

### Support and Community
We have a channel on the Gophers slack, [#twirp](https://gophers.slack.com/messages/twirp),
which is the best place to get quick answers to your questions. You can join the
Gopher slack [here](https://invite.slack.golangbridge.org/).

### Releases
Twirp follows semantic versioning through git tags, and uses Github Releases for
release notes and upgrade guides:
[Twirp Releases](https://github.com/twitchtv/twirp/releases)

### Contributing
Check out [CONTRIBUTING.md](./CONTRIBUTING.md) for notes on making contributions.

### License

This library is licensed under the Apache 2.0 License.
