FROM phablet/platform-devel:arale

RUN apt-get update \
	&& apt-get install --no-install-recommends -y --force-yes \
		bash-completion \
		colormake \
		man-db \
		manpages-dev \
		sudo \
		time \
		vim \
	&& apt-get clean \
	&& rm -f /var/lib/apt/lists/*_dists_*

RUN addgroup --system --gid 110 bluetooth \
	&& addgroup --system --gid 112 netdev \
	&& addgroup --system --gid 129 kvm \
	&& addgroup --system --gid 130 docker \
	&& addgroup --system --gid 132 adb \
	&& adduser --home /home/vicamo --no-create-home \
		--shell /bin/bash \
		--disabled-password \
		--uid 1000 \
		--quiet \
		vicamo \
	&& adduser vicamo dialout \
	&& adduser vicamo cdrom \
	&& adduser vicamo floppy \
	&& adduser vicamo sudo \
	&& adduser vicamo audio \
	&& adduser vicamo dip \
	&& adduser vicamo video \
	&& adduser vicamo plugdev \
	&& adduser vicamo bluetooth \
	&& adduser vicamo netdev \
	&& adduser vicamo kvm \
	&& adduser vicamo docker \
	&& adduser vicamo adb
