core_inc = include_directories('N32G031xx/firmware/CMSIS/core')
device_inc = include_directories('N32G031xx/firmware/CMSIS/device')
cmsis_src = ['N32G031xx/firmware/CMSIS/device/system_n32g031.c']

periph_path = 'N32G031xx/firmware/n32g031_std_periph_driver'
periph_inc = include_directories(periph_path / 'inc')

periph_src_path = periph_path / 'src'
periph_src = [periph_src_path / 'misc.c',
              periph_src_path / 'n32g031_adc.c',
              periph_src_path / 'n32g031_beeper.c',
              periph_src_path / 'n32g031_comp.c',
              periph_src_path / 'n32g031_crc.c',
              periph_src_path / 'n32g031_dbg.c',
              periph_src_path / 'n32g031_dma.c',
              periph_src_path / 'n32g031_exti.c',
              periph_src_path / 'n32g031_flash.c',
              periph_src_path / 'n32g031_gpio.c',
              periph_src_path / 'n32g031_hdiv.c',
              periph_src_path / 'n32g031_i2c.c',
              periph_src_path / 'n32g031_iwdg.c',
              periph_src_path / 'n32g031_lptim.c',
              periph_src_path / 'n32g031_lpuart.c',
              periph_src_path / 'n32g031_opamp.c',
              periph_src_path / 'n32g031_pwr.c',
              periph_src_path / 'n32g031_rcc.c',
              periph_src_path / 'n32g031_rtc.c',
              periph_src_path / 'n32g031_spi.c',
              periph_src_path / 'n32g031_tim.c',
              periph_src_path / 'n32g031_usart.c',
              periph_src_path / 'n32g031_wwdg.c']

sdk_src = ['startup_n32g031_gcc.s', cmsis_src, periph_src]
sdk_inc = [core_inc, device_inc, periph_inc]

sdklib = static_library('sdk',
                        sdk_src,
                        include_directories : sdk_inc,
                        install : true)

sdklib_dependency = declare_dependency(include_directories : sdk_inc,
                                       link_with : sdklib,
                                       sources : sdk_src)