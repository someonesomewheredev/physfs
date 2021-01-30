physfs_base_src = [
	'physfs.c',
	'physfs_unicode.c',
	'physfs_byteorder.c'
]

physfs_archiver_src = [
	'physfs_archiver_7z.c',
	'physfs_archiver_dir.c',
	'physfs_archiver_grp.c',
	'physfs_archiver_hog.c',
	'physfs_archiver_iso9660.c',
	'physfs_archiver_mvl.c',
	'physfs_archiver_qpak.c',
	'physfs_archiver_slb.c',
	'physfs_archiver_unpacked.c',
	'physfs_archiver_vdf.c',
	'physfs_archiver_wad.c',
	'physfs_archiver_zip.c'
]

physfs_platform_src = []

if host_machine.system() == 'windows'
	physfs_platform_src += 'physfs_platform_windows.c'
elif host_machine.system() == 'linux'
	physfs_platform_src += 'physfs_platform_unix.c'
endif

physfs_inc = include_directories('.')
physfs = library('physfs', physfs_platform_src + physfs_archiver_src + physfs_base_src)

physfs_dep = declare_dependency(link_with: physfs, include_directories: physfs_inc)
