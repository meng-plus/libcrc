import os
from building import *

cwd  = GetCurrentDir()
CPPPATH = [cwd + "/include"]
# add general drivers
src = []
if GetDepend(['BSP_LIBCRC_CRC8']):
    src += ['src/crc8.c']
if GetDepend(['BSP_LIBCRC_CRC16']):
    src += ['src/crc16.c']
if GetDepend(['BSP_LIBCRC_CRC32']):
    src += ['src/crc32.c']
if GetDepend(['BSP_LIBCRC_CRC64']):
    src += ['src/crc64.c']
if GetDepend(['BSP_LIBCRC_CRC_CITT']):
    src += ['src/crcccitt.c']
if GetDepend(['BSP_LIBCRC_CRC_DNP']):
    src += ['src/crcdnp.c']
if GetDepend(['BSP_LIBCRC_CRC_KRMIT']):
    src += ['src/crckrmit.c']
if GetDepend(['BSP_LIBCRC_CRC_SICK']):
    src += ['src/crcsick.c']
if GetDepend(['BSP_LIBCRC_NMEA_CHK']):
    src += ['src/nmea-chk.c']



group = DefineGroup('libcrc', src, depend = ['BSP_USING_LIBCRC'], CPPPATH = CPPPATH)


Return('group')
