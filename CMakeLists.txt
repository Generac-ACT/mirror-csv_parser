add_library(csv-parser "")

set_target_properties(csv-parser PROPERTIES
        VERSION ${PROJECT_VERSION}
        SOVERSION ${PROJECT_VERSION_MAJOR}

)

target_sources(csv-parser
    PUBLIC
        csv.h
        PRIVATE
        csv.c
        fread_csv_line.c
        split.c
)

target_include_directories(csv-parser
        PUBLIC
        .
)