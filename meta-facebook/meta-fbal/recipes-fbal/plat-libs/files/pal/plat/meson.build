pal_headers += [
    'pal_cm.h',
    'pal_ep.h',
    'pal_health.h',
    'pal_power.h',
    'pal_sbmc.h',
    ]

pal_sources += [
    'pal_cm.c',
    'pal_ep.c',
    'pal_health.c',
    'pal_power.c',
    'pal_sbmc.c',
    'pal_sensors.c',
    ]

pal_deps += [
    cc.find_library('fbal-fruid'),
    cc.find_library('gpio-ctrl'),
    cc.find_library('ncsi'),
    cc.find_library('nl-wrapper'),
    cc.find_library('nm'),
    cc.find_library('obmc-i2c'),
    cc.find_library('obmc-pmbus'),
    cc.find_library('obmc-sensors'),
    cc.find_library('peci'),
    ]
