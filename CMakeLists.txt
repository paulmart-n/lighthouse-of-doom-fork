
project(lighthouse)

include_directories(
    include
)

set(C_SOURCE_FILES
    src/handlers.c
    src/inventory.c
    src/items.c
    src/main.c
    src/util.c
    src/world.c
)

add_executable(
    lighthouse
    ${C_SOURCE_FILES}
)