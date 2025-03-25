project('fft2d', 'cpp', default_options : ['default_library=static',
                                         'buildtype=debugoptimized',
                                         'warning_level=1',
                                         'cpp_std=gnu++14'])

if not meson.is_subproject() 
  cc = meson.get_compiler('cpp')
endif

include = include_directories('.')

fft2d_sources = files(
  'fftsg.c',
  'fftsg2d.c'
)

fft2d = library('fft2d',
  fft2d_sources,
  include_directories : [include],
  install : true,
  link_args : [],
)

fft2d_dep = declare_dependency(
  link_with : fft2d,
  include_directories : [include]
)
