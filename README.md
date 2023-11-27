# homebrew-tom-test-tap

A homebrew tap storing a specific GDAL revision.

## Using the tap

```
brew add grumbling-tom/tom-test-tap
brew install grumbling-tom/tom-test-tap/gdal
```

## Updating

- Navigate to the [gdal formula in homebrew-core](https://github.com/Homebrew/homebrew-core/commits/master/Formula/g/gdal.rb). 
- Find the commit that corresponds to the version you want to use.
- Copy the commit hash.

```
export GDAL_COMMIT_SHA=<sha>

https://raw.githubusercontent.com/Homebrew/homebrew-core/$GDAL_COMMIT_SHA/Formula/g/gdal.rb
curl -X GET https://raw.githubusercontent.com/Homebrew/homebrew-core/$GDAL_COMMIT_SHA/Formula/g/gdal.rb > Formula/gdal.rb 
```

## What's wrong with `brew extract --version=3.7.2 gdal grumbling-tom/tom-test-tap`

In running an extact, the formula loses its `bottle`s (pre-built binaries).

One main advantage of using `brew` for GDAL is to _avoid_ needing to compile on a given machine. Given that, we are motivated to find an alternative solution that avails of upstream `bottle`s.

## Is this a good idea?

Probably not, for reasons that [Future Tom](mailto:tom@thefuture.com) can elaborate on.
