cmake_minimum_required(VERSION 3.0)

project(jimtcl)

add_library(libjim
    jim.h
    jim-eventloop.h
    jimiocompat.h
    jimregexp.h
    jim-signal.h
    jim-subcmd.h
    jim-tty.h
    jim-win32compat.h
    linenoise.h
    utf8.h
    
    jim.c
    jim-aio.c
    jim-array.c
    jim-clock.c
    jim-eventloop.c
    jim-exec.c
    jim-file.c
    jim-format.c
    jim-history.c
    jim-interactive.c
    jim-interp.c
    jimiocompat.c
    jim-load.c
    jim-namespace.c
    jim-nosignal.c
    jim-pack.c
    jim-package.c
    jim-posix.c
    jim-readdir.c
    jim-readline.c
    jimregexp.c
    jim-regexp.c
    jim-sdl.c
    jimsh.c
    jim-signal.c
    jim-sqlite3.c
    jim-subcmd.c
    jim-syslog.c
    jim-tclprefix.c
    jim-tty.c
    jim-win32.c
    jim-win32compat.c
    jim-zlib.c
    linenoise.c
    utf8.c
    
    jim-mk.cpp
    )
set_property(TARGET libjim PROPERTY C_STANDARD 99)
set_target_properties(libjim PROPERTIES FOLDER "libs")

add_executable(jimsh
    jimsh.c
    )
set_property(TARGET jimsh PROPERTY C_STANDARD 99)
