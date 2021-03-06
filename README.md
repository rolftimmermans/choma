# choma
Random ordering for mocha

## Why?

It is very easy to accidentally create a fragile test suite by leaving lingering state after a test case, that is then inadvertently used as a precondition for a subsequent test. This can then cause problems trying to run single tests or test suites in isolation.

By executing files in a random order on each execution of a test suite the risk of accidental introduction of state is eliminated, or at least reduced, since any dependency on leftover state will result in test failures.

## Usage

Pass `choma` as a `require` option to mocha, either by appending to your test command:

```shell
> mocha ./tests/ --require choma
```

or by adding a line to `mocha.opts`

```
--require choma
```

