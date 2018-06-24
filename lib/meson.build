libmr_src = ['animation.c', 'button.c', 'colors.c', 'containers.c', 'framebuffer.c', 'framebuffer_generic.c', 'framebuffer_png.c', 'framebuffer_truetype.c', 'fstab.c', 'inject.c', 'input.c', 'listview.c', 'keyboard.c', 'mrom_data.c', 'notification_card.c', 'progressdots.c', 'tabview.c', 'touch_tracker.c', 'util.c', 'workers.c']
libmr_src += ['input_type_b.c']

cc = meson.get_compiler('c')
libm = cc.find_library('m', required : false)
libpthread = cc.find_library('pthread', required : false)

ft2 = dependency('freetype2')
libpng16 = dependency('libpng16')

libmultirom = static_library('multirom',
                             libmr_src,
                             dependencies : [libbootimg, ft2, libpng16, libm, libpthread])
