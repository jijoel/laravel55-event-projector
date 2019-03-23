# Event sourcing for Artisans 📽

This is a fork of spatie/laravel-event-projector, with support for Laravel 5.5.

In order to run tests, I manually had to enter type hinting for all of the methods in Illuminate\Foundation\Testing\Constraints\HasInDatabase.

Everything passes, except for `EventSerializerTest::it_serializes_an_event_to_json`, because it lacks the `'relations' => []` line in the resulting json. I am hoping this is not critical to the function of the system.

Definitely treat this as experimental.

---

Event sourcing is to data what Git is to code <sup>[1](#footnote1)</sup>. Most applications have their current state stored in a database. By storing only the current state a lot of information is lost. You don't know how the application got in this state.

Event sourcing tries to solve that problem by saving all events that happen in your app. The state of your application is built by listening to those events.

Here's a traditional example to make it more clear. Imagine you're a bank. Your clients have accounts. Instead of storing the balance of the accounts, you could store all the transactions. That way you not only know the balance of the account but also the reason why it's that specific number. There are many other benefits of storing events.

This package aims to be the simple and very pragmatic way to get started with event sourcing in Laravel.

## Documentation

You can find installation instructions and detailed instructions on how to use this package at [the dedicated documentation site](https://docs.spatie.be/laravel-event-projector).

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security

If you discover any security related issues, please email freek@spatie.be instead of using the issue tracker.

## Postcardware

You're free to use this package, but if it makes it to your production environment we highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using.

Our address is: Spatie, Samberstraat 69D, 2060 Antwerp, Belgium.

We publish all received postcards [on our company website](https://spatie.be/en/opensource/postcards).

## Credits

- [Freek Van der Herten](https://github.com/freekmurze)
- [All Contributors](../../contributors)

A big thank you to [Dries Vints](https://github.com/driesvints) for giving lots of valuable feedback while we were developing the package.

## Support us

Spatie is a webdesign agency based in Antwerp, Belgium. You'll find an overview of all our open source projects [on our website](https://spatie.be/opensource).

Does your business depend on our contributions? Reach out and support us on [Patreon](https://www.patreon.com/spatie).
All pledges will be dedicated to allocating workforce on maintenance and new awesome stuff.

## Footnotes

<a name="footnote1"><sup>1</sup></a> Quote taken from [Event Sourcing made Simple](https://kickstarter.engineering/event-sourcing-made-simple-4a2625113224)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
