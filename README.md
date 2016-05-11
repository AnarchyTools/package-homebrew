# package-homebrew

package-homebrew is an atbin packager that builds homebrew packages.

# Usage

See [documentation](http://anarchytools.org/docs/package-homebrew.html)

# AT internal release process

To get AT tools in our official repos, do the following:

1.  Run CI
2.  Download an xz and `.rb` built from CI
3.  Upload xz package to a GitHub release
4.  Check the built `.rb` into our [homebrew tap](https://github.com/AnarchyTools/homebrew-homebrew).

# Maintainer notes

`package-homebrew` is self-hosting; it does not require AT to build.  This is primarily because we want to use it to package [`atbuild`](https://github.com/AnarchyTools/atbuild) itself, so it cannot depend on `atbuild` to work.

For these reasons, it's written in shell, largely glues together standard OSX tools, and there is no compile step.  It's a manually-mananged [`atbin`](http://anarchytools.org/docs/atbin.html) format.  

As a result, `package-homebrew` is used to package itself, which is basically the test of its correctness.



