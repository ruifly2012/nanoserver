# Copyright 2014 The Go Authors. All rights reserved.
# Use of this source code is governed by a BSD-style
# license that can be found in the LICENSE file.

docker: Dockerfile
	docker build -t gobuilders/linux-x86-clang .

# TODO(bradfitz): test targets, using cmd/gomote and the buildlet in the container.

# TODO(bradfitz): docs on how to build a new image. In a nutshell,
#
#    $ go install golang.org/x/build/cmd/docker2boot
#    $ sudo docker2boot --image=gobuilders/linux-x86-clang --out=linux-buildlet-clang.tar.gz
#    $ gsutil cp -a public-read linux-buildlet-clang.tar.gz gs://go-builder-data/linux-buildlet-clang.tar.gz
#    $ gcloud compute --project symbolic-datum-552 images create linux-buildlet-clang --source-uri gs://go-builder-data/linux-buildlet-clang.tar.gz
