project('gsth264', 'c',
    version: '1.18.0.0',
    meson_version: '>= 0.54',
    default_options: [
        'warning_level=1',
        'buildtype=debugoptimized'
    ]
)

gst_version = meson.project_version()
version_arr = gst_version.split('.')
gst_version_major = version_arr[0].to_int()
gst_version_minor = version_arr[1].to_int()
gst_version_micro = version_arr[2].to_int()
if version_arr.length() == 4
    gst_version_nano = version_arr[3].to_int()
else
    gst_version_nano = 0
endif
gst_req = '>= @0@.@1@.0'.format(gst_version_major, gst_version_minor)
gstbase_dep = dependency('gstreamer-base-1.0', version: gst_req)
gstaudio_dep = dependency('gstreamer-audio-1.0', version: gst_req)

plugins_install_dir = join_paths(get_option('libdir'), 'gstreamer-1.0')

subdir('gst')
