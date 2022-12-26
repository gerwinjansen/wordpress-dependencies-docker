# A docker image with Wordpress dependencies
The [Docker "Official Image" for wordpress](https://hub.docker.com/_/wordpress/), maintained in [docker-library/wordpress](https://github.com/docker-library/wordpress), provides images with Wordpress pre-installed.

It includes a volume and entrypoint.
https://github.com/docker-library/wordpress/blob/c705336b1dfe75c82fce00bb8aa7143755981747/latest/php8.2/apache/Dockerfile#L162-L168

This is not usable if you want to package your Wordpress application in an immutable container with only a volume for the upload directory, because you [can't undo a volume](https://stackoverflow.com/questions/44020785/remove-a-volume-in-a-dockerfile).

This repository provides a stripped version of the official Docker file with only the dependencies.
This is temporary till [#764 Provide a php dependency only image without wordpress specific files](https://github.com/docker-library/wordpress/issues/764) is resolved.