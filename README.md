#DESCRIPTION

This is a patch for nginx to allow running it chroot(8)'d.
After applying this patch and running nginx, it will chroot
by default. To disable this feature, nginx has to be executed
with the -u option.

#INSTALLATION

    # download the source code of nginx
    wget http://nginx.org/download/nginx-1.9.3.tar.gz
    tar -zxvf nginx-1.9.3
    cd nginx-1.9.3

    # patch the nginx source tree.
    patch -p1 < /path/to/nginx-1.9-chroot.patch

    # configure and compile nginx
    ./configure && make

#COPYRIGHT & LICENSE

Copyright (c) 2014 Robert Nagy <robert@openbsd.org>

Permission to use, copy, modify, and distribute this software for any
purpose with or without fee is hereby granted, provided that the above
copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
