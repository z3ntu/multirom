project('multirom', 'c')

src = ['kexec.c', 'main.c', 'multirom.c', 'multirom_ui.c', 'multirom_ui_landscape.c', 'multirom_ui_portrait.c', 'multirom_ui_themes.c', 'pong.c', 'rcadditions.c', 'rom_quirks.c']

add_global_arguments('-DDPI_MUL=1', language : 'c')
add_global_arguments('-DMULTIROM_DEFAULT_ROTATION=0', language : 'c')
add_global_arguments('-DTARGET_DEVICE="generic"', language : 'c')
add_global_arguments('-DMULTIROM_DEFAULT_BRIGHTNESS=40', language : 'c')
add_global_arguments('-DMR_KEXEC_MEM_MIN="0"', language : 'c')
add_global_arguments('-DMR_DPI_FONT=96', language : 'c')

libbootimg = dependency('libbootimg', fallback : ['libbootimg', 'libbootimg'])

subdir('lib')

#libbootimg = subproject('libbootimg')


executable('multirom',
           src,
           dependencies : libbootimg,
           link_with : libmultirom)
