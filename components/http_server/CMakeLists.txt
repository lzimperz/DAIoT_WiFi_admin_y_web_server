cmake_minimum_required(VERSION 3.16)

set(EXTRA_COMPONENT_DIRS $ENV{IDF_PATH}/examples/common_components/protocol_examples_common)

idf_component_register(SRCS 
                                        "http_server.c"
                                        "wsvr_miscs.c"
                    INCLUDE_DIRS .

                    EMBED_TXTFILES 
                                        html_page_index.html
                                        html_page_wifi_config.html
                                        html_page_device_data.html

                    REQUIRES 
                                        nvs_flash
                                        esp_event
                                        esp_timer
                                        esp_http_server
                                        json
                                                        )
