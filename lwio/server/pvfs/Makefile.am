if ENABLE_STATIC_DRIVERS
noinst_LTLIBRARIES = libpvfs.sys.la
DRIVER_CFLAGS =
DRIVER_LDFLAGS =
else
lib_LTLIBRARIES = libpvfs.sys.la
DRIVER_CFLAGS = -shared
DRIVER_LDFLAGS = -module -shared -avoid-version
endif

libpvfs_sys_la_SOURCES = \
    globals.c \
    driver.c \
    config.c \
    irpctx.c \
    async_handler.c \
    create.c \
    read.c   \
    write.c  \
    flush.c \
    lock.c \
    deviceio.c \
    fsctrl.c \
    fsctrl_stub.c \
    queryfile.c \
    querydir.c \
    queryvol.c \
    querysecdesc.c \
    close.c \
    create_file.c \
    create_dir.c \
    create_device.c \
    alloc.c \
    ccb.c \
    ccb_fileinfo.c \
    fcb.c \
    errno.c \
    syswrap.c \
    util_open.c \
    util_dir.c \
    unixpath.c \
    pathcache.c \
    string.c \
    wildcard.c \
    sharemode.c \
    locking.c \
    acl.c \
    acl_xattr.c \
    acl_posix.c \
    attrib.c \
    attrib_xattr.c \
    util_security.c \
    util_time.c \
    fileBasicInfo.c \
    fileStandardInfo.c \
    fileAllInfo.c \
    fileInternalInfo.c \
    fileNameInfo.c \
    fileBothDirInfo.c \
    fileFullDirInfo.c \
    fileIdBothDirInfo.c \
    fileIdFullDirInfo.c \
    fileNamesInfo.c \
    fileDirInfo.c \
    fileEaInfo.c \
    fileFullEaInfo.c \
    fileStreamInfo.c \
    fileEndOfFileInfo.c \
    fileAllocationInfo.c \
    fileCompressionInfo.c \
    fileDispositionInfo.c \
    fileRenameInfo.c \
    fileFsAttribInfo.c \
    fileFsVolInfo.c \
    fileFsSizeInfo.c \
    fileFsDeviceInfo.c \
    fileNetworkOpenInfo.c \
    fileAccessInfo.c \
    filePositionInfo.c \
    fileModeInfo.c \
    thread_worker.c \
    work_queue.c \
    oplock.c \
    notify.c \
    ioctlOpenFileInfo.c \
    listq.c \
    zct.c


libpvfs_sys_la_CPPFLAGS = \
    -I@top_srcdir@         \
    -I@top_srcdir@/include \
    -I@top_srcdir@/server/include \
    -D_FILE_OFFSET_BITS=64 \
    -DLW_ENABLE_THREADS=1

libpvfs_sys_la_CFLAGS = $(AM_CFLAGS) $(DRIVER_CFLAGS)

libpvfs_sys_la_LIBADD = \
    @top_builddir@/server/iomgr/libiomgr.la \
    @UUID_LIBS@ \
    @PTHREAD_LIBS@ \
    @XATTR_LIBS@

libpvfs_sys_la_LDFLAGS = $(DRIVER_LDFLAGS)

