#!/bin/sh
#
# /etc/init.d/btsync: Start the BTSync daemon
#
# This shell script should be placed in /etc/init.d/.
# It configures BitTorrent Sync as a background daemon on
# systems with init.d as a daemon system. Make sure to edit
# to your wishes before use.
#
# On systems using system.d intead (e.g. Raspbian since
# version Jessie), use btsync.service instead of this file.
#
# To enable btsync to start on boot as a daemon:
#		sudo update-rc.d btsync defaults
# To start it:
#		sudo service btsync start
#
#
### BEGIN INIT INFO
# Provides:		btsync
# Required-Start:	$local_fs $remote_fs $syslog
# Required-Stop:	$local_fs $remote_fs $syslog
# Should-Start:		$network
# Should-Stop:		$network
# Default-Start:	2 3 4 5
# Default-Stop:		0 1 6
# Short-Description: 	Runs BTSync
# Description:		Runs BitTorrent Sync
### END INIT INFO

start() {
	echo "Starting BitTorrent Sync..."
	sudo -u btsync /home/btsync/btsync --config /home/btsync/btsync.conf
}

stop() {
	echo "Stopping BitTorrent Sync..."
	killall btsync
}

case "$1" in
	start)
		start
		;;
	stop)
		stop
		;;
	restart|reload|force-reload)
		stop
		sleep 5s
		start
		;;
	status)
		;;
	*)
		echo "Usage: "
		echo "sudo /etc/init.d/btsync start|stop|restart"
		exit 1
		;;
esac

exit 0
