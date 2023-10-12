from building import *

cwd = GetCurrentDir()
CPPPATH = [cwd+'/include']

# add the general drivers.
src = Split("""
src/crc16.c
""")

#src += Glob("src/*.c")
# 提取当前工作目录的文件夹名称
folder_name = os.path.basename(cwd)
group = DefineGroup(folder_name, src, depend = ['PKG_USING_LIBCRC'], CPPPATH = CPPPATH)

list = os.listdir(cwd)
for item in list:
    if os.path.isfile(os.path.join(cwd, item, 'SConscript')):
        group = group + SConscript(os.path.join(item, 'SConscript'))

Return('group')
