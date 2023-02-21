.DEFAULT_GOAL := build
SHELL := /bin/bash

../build/Makefile:
	mkdir -p ../build
	cd ../build && cmake ..

../build/build/rclone-browser: ../build/Makefile
	cd ../build && make  -j $$(nproc)

usr/bin/rclone-browser: ../build/build/rclone-browser
	cp ../build/build/rclone-browser usr/bin/rclone-browser

build: usr/bin/rclone-browser 
	
clean:
	rm -fr ../build usr/bin/rclone-browser 
