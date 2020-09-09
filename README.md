# s3ftp

A FTP server implemented in Go which writes to S3

## What

It's a (partially implemented) FTP server that writes to AWS's S3. It's only partially implemented since it only needs to be able to deal with the subset of FTP commands that this particular [ieGeek camera](https://www.amazon.co.uk/dp/B073GQ8T2L) uses.

## Why?

I bought a cheap IP camera to bolster the security of my garage. It writes data to a removable SD card, but can also write data to... FTP. Yes, FTP, in 2020. That seemed pretty rubbish. Luckily the [FTP protocol](https://tools.ietf.org/html/rfc959) is literally as old as I am and is well understood and blah blah blah, so I figured I'd write a thing, for fun, to throw data on S3 via the camera's FTP function.

You might be saying "well hur-de-hur you're a nutter, why not just use [AWS Transfer Family](https://aws.amazon.com/aws-transfer-family/)?". That stuff's pretty expensive and I just want to store what looks like about 20G of data per day. That would be about $250 a month. This will be a lot cheaper.

Why didn't I just use an existing solution? Because I fancied hacking away for lols.
