gsth264_sources = [
    'gsth264.c'
]

gsth264 = library('gsth264',
    gsth264_sources,
    include_directories: include_directories('..' / '..'),
    dependencies: [
        gstbase_dep,
        gstaudio_dep
    ],
    install: true,
    install_dir: plugins_install_dir,
)
