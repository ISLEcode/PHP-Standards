## PHP Standard recommendations

### Overview

Rather then reinventing the wheel, we have taken the commonly discussed and adopted _PHP standard recommendations_ (PSR),
maintained by the [PHP Framework Interoperability Group][php-fig] (PHP-FIG), and customised them for our purposes and toolchains.

As clearly stated by the PHP-FIG, their standardisation efforts target a closed set of PHP projects:

> Our main audience is each other, but we’re very aware that the rest of the PHP community is watching. If other folks want to
> adopt what we’re doing they are welcome to do so, but that is not the aim.

While we adhere to the majority of the commonalities they have standardised, some are considered -- for our purposes, non
practical or in violation of our quality assurance and code base, as established, and evolved, over almost four decades, and
being used in many different programming languages. Hence the purpose of this repository to amend their works accordingly.

This is made available primarily for our staff, partners, and other contributors on public or private projects we manage. As such
it is a reference and not really open to debat. Nonetheless, we are [open to discuss][discuss] some standards which seem to go
against so-called industry standards and best practices -- for instance the archaic 80 columns rule. Don't fall in the trap of
simply stating your opinion; discussion is about experience, facts, and figures. We will respond to such discussions on a best
effort basis.

### Recommendations

| ID  | Title                                          | FIG status   | ISLE status   |
| :-: | --------------------------------------         | ------------ | -----------   |
| 0   | <del>[Autoloading Standard][psr0]</del>        | Deprecated   | n/a           |
| 1   | [Basic Coding Standard][psr1]                  | Accepted     | Proof reading |
| 2   | <del>[Coding Style Guide][psr2]</del>          | Deprecated   | n/a           |
| 3   | [Logger Interface][psr3]                       | Accepted     | Proof reading |
| 4   | [Autoloading Standard][psr4]                   | Accepted     | Proof reading |
| 5   | [PHPDoc Standard][psr5]                        | Draft        | Proof reading |
| 6   | [Caching Interface][psr6]                      | Accepted     | Proof reading |
| 7   | [HTTP Message Interface][psr7]                 | Accepted     | Proof reading |
| 8   | <del>[Huggable Interface][psr8]</del>          | Abandoned    | n/a           |
| 9   | <del>[Security Advisories][psr9]</del>         | Abandoned    | n/a           |
| 10  | <del>[Security Reporting Process][psr10]</del> | Abandoned    | n/a           |
| 11  | [Container Interface][psr11]                   | Accepted     | Proof reading |
| 12  | [Extended Coding Style Guide][psr12]           | Accepted     | Proof reading |
| 13  | [Hypermedia Links][psr13]                      | Accepted     | Proof reading |
| 14  | [Event Dispatcher][psr14]                      | Accepted     | Proof reading |
| 15  | [HTTP Handlers][psr15]                         | Accepted     | Proof reading |
| 16  | [Simple Cache][psr16]                          | Accepted     | Proof reading |
| 17  | [HTTP Factories][psr17]                        | Accepted     | Proof reading |
| 18  | [HTTP Client][psr18]                           | Accepted     | Proof reading |
| 19  | [PHPDoc tags][psr19]                           | Draft        | Proof reading |
| 20  | [Clock][psr20]                                 | Draft        | Proof reading |

[discuss]: https://github.com/ISLEcode/PHP-Standards/discussions
[php-fig]: https://github.com/php-fig/fig-standards
[psr0]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-0.md
[psr10]: https://github.com/ISLEcode/PHP-Standards/blob/master/proposed/security-reporting-process.md
[psr11]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-11-container.md
[psr12]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-12-extended-coding-style-guide.md
[psr13]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-13-links.md
[psr14]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-14-event-dispatcher.md
[psr15]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-15-request-handlers.md
[psr16]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-16-simple-cache.md
[psr17]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-17-http-factory.md
[psr18]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-18-http-client.md
[psr19]: https://github.com/ISLEcode/PHP-Standards/blob/master/proposed/phpdoc-tags.md
[psr1]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr20]: https://github.com/ISLEcode/PHP-Standards/blob/master/proposed/clock.md
[psr2]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr3]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-3-logger-interface.md
[psr4]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-4-autoloader-meta.md
[psr5]: https://github.com/ISLEcode/PHP-Standards/blob/master/proposed/phpdoc.md
[psr6]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-6-cache.md
[psr7]: https://github.com/ISLEcode/PHP-Standards/blob/master/accepted/PSR-7-http-message.md
[psr8]: https://github.com/ISLEcode/PHP-Standards/blob/master/proposed/psr-8-hug/
[psr9]: https://github.com/ISLEcode/PHP-Standards/blob/master/proposed/security-disclosure-publication.md
[workflow]: https://github.com/ISLEcode/PHP-Standards/blob/php-fig/bylaws/002-psr-workflow.md
