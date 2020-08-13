# installed version.h header generation
version_h_data = configuration_data()
version_h_data.set('VMAF_API_VERSION_MAJOR', vmaf_api_version_major)
version_h_data.set('VMAF_API_VERSION_MINOR', vmaf_api_version_minor)
version_h_data.set('VMAF_API_VERSION_PATCH', vmaf_api_version_revision)
version_h_target = configure_file(input: 'version.h.in',
                                  output: 'version.h',
                                  configuration: version_h_data)

# install headers
inc_hdr = files([ 'feature.h',
                  'libvmaf.h',
                  'libvmaf.rc.h',
                  'model.h',
                  'picture.h' ])
install_headers(inc_hdr,
                version_h_target,
                subdir : 'libvmaf')
