# dependabot-bundler2-project

Test this update in dependabot-core:

```
bin/dry-run.rb bundler dsp-testing/dependabot-bundler2-project --cache=files --dep=excon
```

This update currently fails with `DependencyFileNotResolvable` error:

```
Bundler::VersionConflict with message: Bundler could not find compatible versions for gem "bundler":
  In Gemfile:
    guard-bundler (~> 3.0.0) was resolved to 3.0.0, which depends on
      bundler (>= 2.1, < 3)

  Current Bundler version:
    bundler (1.17.3)
This Gemfile requires a different version of Bundler.
Perhaps you need to update Bundler by running `gem install bundler`?

Could not find gem 'bundler (>= 2.1, < 3)', which is required by gem 'guard-bundler (~> 3.0.0)', in any of the sources.
```

When running this update with bundler 2.1.4 installed it raises a `DependencyFileNotEvaluatable` error.
