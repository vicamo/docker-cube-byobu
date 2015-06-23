FROM vicamo/ubuntu-sdk:frameworks-vivid-armhf

RUN apt-get update \
	&& apt-get install --no-install-recommends -y --force-yes \
		bash-completion \
		bzr-builddeb \
		ccache \
		sudo \
		time \
		vim \
	&& apt-get clean \
	&& rm -f /var/lib/apt/lists/*_dists_*

RUN adduser --home /home/vicamo --no-create-home \
		--shell /bin/bash \
		--disabled-password \
		--uid 1000 \
		--quiet \
		vicamo \
	&& adduser vicamo sudo
