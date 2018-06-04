cmake_minimum_required(VERSION 3.10)
project(sdk_example C)

set(CMAKE_C_STANDARD 99)

add_definitions(
    -Dhi3518ev200
    -DCHIP_ID=CHIP_HI3518E_V200
    -DSENSOR_TYPE=SONY_IMX222_DC_1080P_30FPS
)

include_directories(
    include/
    sample/common/
)

add_executable(sdk_example
    sample/venc/sample_venc.c
    sample/common/loadbmp.h
    sample/common/loadbmp.c
    sample/common/sample_comm_isp.c
    sample/common/sample_comm_venc.c
    sample/common/sample_comm_ive.c
    sample/common/sample_comm_vi.c
    sample/common/sample_comm.h
    sample/common/sample_comm_ive.h
    sample/common/sample_comm_vo.c
    sample/common/sample_comm_audio.c
    sample/common/sample_comm_sys.c
    sample/common/sample_comm_vpss.c
)
