# Bookmarker

[![Build Status](https://travis-ci.org/lubien/bookmarker.svg?branch=master)](https://travis-ci.org/lubien/bookmarker)

> Convert your Google Chrome's bookmarks into markdown files

## Build

Enter the cloned repo folder then:

```
mix deps.get
mix #=> aliased mix.escript_build
```

## Usage

```
Usage: bookmarker [options]

  -f, --file            Set where your chrome bookmarks file is.
			Default: ~/.config/google-chrome/Default/Bookmarks
  -t, --title           Set a title for the rendered markdown.
			Default: Google Chrome Bookmarks
  -d, --description     Set a description for the rendered markdown.
			Default: Generated by Bookmarker
  --no-timestamp        Prevent appending of build datetime after description.
			Default: use timestamp
  -i, --ignore          Ignore folders. You may set this multiple times.
  -o, --output          Save rendered markdown to a file.
			Default: none (output to stdin)

Examples:

  bookmarker
    # output into your stdout.

  bookmarker -i "Foo/Bar"
    # ignore the folder named Bar inside Foo.

  bookmarker -o "./foo.md"
    # save rendered markdown into a file named "foo.md" in your cwd.
```

## License

[MIT](LICENSE.md)
