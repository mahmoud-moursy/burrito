# Burrito -- Secrets n' Sauce

A simple, monadic, encryption-agnostic database for secrets.

## Why?

There were no good KeePassXC apps on iOS. All of them wanted a subscription, or 60 dollars!

I like free things, so I made a Free Thing. 100% MIT-licensed, 100% open-source, and 100% free.

## How?

The burrito database uses BSON under-the-hood.

This is convenient because it's a binary format, and it's easy to parse. This makes it easier to store
encrypted data compared to YAML/TOML/JSON, which are all text-based formats.

## Monadic!?

Monads! Monads are awesome! They are your `Option<T>`s and `Result<T, E>`s, for the uninitiated.

A monad is like a burrito. It's a container that holds a value, and it's also a function that can be used to transform
the value inside the burrito.

The burrito database is a monad.

## Why not other formats?

Encryption produces binary data, and binary data doesn't work with 100% of human-readable serialization formats, unless
I want to use base64, which I do not because it's [wack](https://eprint.iacr.org/2022/361).

You can use `serde` to export to any format you want, but I decided upon BSON because it's a binary format that is
purpose-made for this.

### Disclaimer:

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.