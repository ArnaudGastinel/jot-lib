
ADD_LIBRARY(dev
	dev.C
	devpoll.C
	tty.C
	tablet.C)

TARGET_LINK_LIBRARIES(dev
	mlib
	std)

