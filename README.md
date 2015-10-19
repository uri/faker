# Faker [![Version](https://img.shields.io/hexpm/v/faker.svg?style=flat-square)](https://hex.pm/packages/faker)[![License](https://img.shields.io/hexpm/l/faker.svg?style=flat-square)](https://github.com/igas/faker/blob/master/LICENSE)[![Build Status](https://img.shields.io/travis/igas/faker.svg?style=flat-square)](https://travis-ci.org/igas/faker)[![Issues](https://img.shields.io/github/issues/igas/faker.svg?style=flat-square)](https://github.com/igas/faker/issues)[![Downloads](https://img.shields.io/hexpm/dt/faker.svg?style=flat-square)](https://hex.pm/packages/faker)[![Donation](https://img.shields.io/gratipay/igas.svg?style=flat-square)](https://gratipay.com/igas/)

**Faker** is a pure [Elixir](http://elixir-lang.org/) library for generating
fake data.

Inspired by:

* Ruby [faker](https://github.com/stympy/faker)
* Ruby [ffaker](https://github.com/EmmanuelOga/ffaker)
* PHP [Faker](https://github.com/fzaninotto/Faker)
* Python [faker](https://github.com/joke2k/Faker)
* Erlang [fakerl](https://github.com/mawuli-ypa/fakerl)
* Haskell [faker](https://github.com/gazay/faker)

## Install

In your `mix.exs` file, add the `:faker` project to your dependencies
(optionally include the version):

``` elixir
  defp deps do
    [{:faker, "~> 0.5", only: :test}]
  end
```

Do a `mix deps.get` to fetch the dependency. That's it.

If you want to use `faker` outside tests remove `, only: :test` part.

## Usage

You nead to start `:faker` application. Cause of many usages of fake data can be
(seed database, tests, etc) it's no right place to start it. For example, if you
want to use it in tests, just add `Faker.start` to `test/test_helper.exs`, and
use any function decribed below. For example, if you nead random name use
`Faker.Name.name`.

## TODO

* Add more generators
* Check performance
* Add documentation
* Promote library

## Troubleshooting

* If you get a message like the one below when you call `Faker.Address.city`,
you need to add `:faker` to your application's mix file, in the `applications`
function, as above.

``` elixir
** (FunctionClauseError) no function clause matching in Faker.Address.city_count/1
    lib/faker/address.ex:48: Faker.Address.city_count(nil)
    lib/faker/address.ex:41: Faker.Address.city/0
```

## Tools

Faker designed as lightweight library, because of it it can be easily used with
other tools.

## Templating

You can build templates for testing purposes with the
[Blacksmith](https://github.com/batate/blacksmith) project. See the Blacksmith

## Thanks

[![Sponsored by Evil Martians](https://evilmartians.com/badges/sponsored-by-evil-martians.svg)](http://evilmartians.com/)
[readme](https://github.com/batate/blacksmith#readme) for details.

# [License](https://github.com/igas/faker/blob/master/LICENSE)

Released under the MIT License.
