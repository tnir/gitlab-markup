# Contributing

Thank you for your interest in contributing to this GitLab project! We welcome
all contributions. By participating in this project, you agree to abide by the
[code of conduct](#code-of-conduct).

This library's only job is to decide which markup format to use and call out to an external library to convert the markup to HTML (see the [README](README.md) for more information on how markup is rendered)

## Contributor license agreement

By submitting code as an individual you agree to the [individual contributor
license agreement][individual-agreement].

By submitting code as an entity you agree to the [corporate contributor license
agreement][corporate-agreement].

## Code of conduct

As contributors and maintainers of this project, we pledge to respect all people
who contribute through reporting issues, posting feature requests, updating
documentation, submitting pull requests or patches, and other activities.

We are committed to making participation in this project a harassment-free
experience for everyone, regardless of level of experience, gender, gender
identity and expression, sexual orientation, disability, personal appearance,
body size, race, ethnicity, age, or religion.

Examples of unacceptable behavior by participants include the use of sexual
language or imagery, derogatory comments or personal attacks, trolling, public
or private harassment, insults, or other unprofessional conduct.

Project maintainers have the right and responsibility to remove, edit, or reject
comments, commits, code, wiki edits, issues, and other contributions that are
not aligned to this Code of Conduct. Project maintainers who do not follow the
Code of Conduct may be removed from the project team.

This code of conduct applies both within project spaces and in public spaces
when an individual is representing the project or its community.

Instances of abusive, harassing, or otherwise unacceptable behavior can be
reported by emailing contact@gitlab.com.

This Code of Conduct is adapted from the [Contributor Covenant][contributor-covenant], version 1.1.0,
available at [http://contributor-covenant.org/version/1/1/0/](http://contributor-covenant.org/version/1/1/0/).

[contributor-covenant]: http://contributor-covenant.org
[individual-agreement]: https://docs.gitlab.com/ee/legal/individual_contributor_license_agreement.html
[corporate-agreement]: https://docs.gitlab.com/ee/legal/corporate_contributor_license_agreement.html


## Submitting a Merge Request

1. Fork it.
2. Create a branch (`git checkout -b my_markup`)
3. Commit your changes (`git commit -am "Added Snarkdown"`)
4. Push to the branch (`git push origin my_markup`)
5. Open a [Merge Request][1]
6. Enjoy a refreshing Diet Coke and wait

## Testing

To run the tests:

    $ rake

If nothing complains, congratulations!

## Releasing a new version

If you are the current maintainer of this gem:

0. Bump the version number in `lib/github-markup.rb`, adhering to [Semantic Versioning](http://semver.org/)
0. Update `HISTORY.md`
0. Test the latest version on GitHub
  0. Build the new version with `rake build`
  0. Copy `pkg/gitlab-markup*.gem` to `vendor/cache` in your local checkout of GitHub
  0. Update the version for `gitlab-markup` in the `Gemfile`
  0. Run `bundle update --local gitlab-markup`
  0. Run any relevant tests and test it manually from the browser.
0. Push the new gem release with `rake release`. If you don't have permission to release to rubygems.org, contact one of the existing owners (`gem owners gitlab-markup`) and ask them to add you.

[1]: https://gitlab.com/gitlab-org/gitlab-markup/merge_requests
