build.sh gets called by post-transfer hook to build the project. Can use whatever you want, but docker containers are recommended.

Dockerfile-build is used to build the heavyweight container that runs the project build process. This should be killed and cleaned up after it is created.

Dockerfile-host is used to build the lightweight container that runs the hosted process. This should be killed and removed before it is created, then cleaned up afterwards.

Dockerfile-data is a template used for a shared persistent volume. This should NOT be run, killed, or cleaned up unless it is not already running.

Dockerfile-db is a template used for a shared persistent database. This should NOT be run, killed, or cleaned up unless it is not already running.
