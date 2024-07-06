project('robertson-radio', 'c')

src = ['src/main.c', 'src/n32g031_it.c']
inc = ['src']

subdir('sdk')

executable('robertson-radio',
           ['src/main.c', 'src/n32g031_it.c'],
           include_directories: [inc],
           dependencies: sdklib_dependency,
           install: false)