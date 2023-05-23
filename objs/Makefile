
CC =	cc
CFLAGS =  -pipe  -O -W -Wall -Wpointer-arith -Wno-unused-parameter -Werror -g 
CPP =	cc -E
LINK =	$(CC)


ALL_INCS = -I src/core \
	-I src/event \
	-I src/event/modules \
	-I src/os/win32 \
	-I objs/nginx-rtmp-module \
	-I objs/pcre2-10.42/src/ \
	-I objs/openssl-1.1.1t/.openssl/include \
	-I objs/zlib-1.2.13 \
	-I objs \
	-I src/http \
	-I src/http/modules \
	-I src/http/v2 \
	-I src/mail \
	-I src/stream


CORE_DEPS = src/core/nginx.h \
	src/core/ngx_config.h \
	src/core/ngx_core.h \
	src/core/ngx_log.h \
	src/core/ngx_palloc.h \
	src/core/ngx_array.h \
	src/core/ngx_list.h \
	src/core/ngx_hash.h \
	src/core/ngx_buf.h \
	src/core/ngx_queue.h \
	src/core/ngx_string.h \
	src/core/ngx_parse.h \
	src/core/ngx_parse_time.h \
	src/core/ngx_inet.h \
	src/core/ngx_file.h \
	src/core/ngx_crc.h \
	src/core/ngx_crc32.h \
	src/core/ngx_murmurhash.h \
	src/core/ngx_md5.h \
	src/core/ngx_sha1.h \
	src/core/ngx_rbtree.h \
	src/core/ngx_radix_tree.h \
	src/core/ngx_rwlock.h \
	src/core/ngx_slab.h \
	src/core/ngx_times.h \
	src/core/ngx_shmtx.h \
	src/core/ngx_connection.h \
	src/core/ngx_cycle.h \
	src/core/ngx_conf_file.h \
	src/core/ngx_module.h \
	src/core/ngx_resolver.h \
	src/core/ngx_open_file_cache.h \
	src/core/ngx_crypt.h \
	src/core/ngx_proxy_protocol.h \
	src/core/ngx_syslog.h \
	src/event/ngx_event.h \
	src/event/ngx_event_timer.h \
	src/event/ngx_event_posted.h \
	src/event/ngx_event_connect.h \
	src/event/ngx_event_pipe.h \
	src/event/ngx_event_udp.h \
	src/os/win32/ngx_win32_config.h \
	src/os/win32/ngx_time.h \
	src/os/win32/ngx_errno.h \
	src/os/win32/ngx_alloc.h \
	src/os/win32/ngx_files.h \
	src/os/win32/ngx_shmem.h \
	src/os/win32/ngx_process.h \
	src/os/win32/ngx_atomic.h \
	src/os/win32/ngx_thread.h \
	src/os/win32/ngx_socket.h \
	src/os/win32/ngx_os.h \
	src/os/win32/ngx_user.h \
	src/os/win32/ngx_dlopen.h \
	src/os/win32/ngx_process_cycle.h \
	src/event/ngx_event_openssl.h \
	src/core/ngx_regex.h \
	objs/pcre2-10.42/src/pcre2.h \
	objs/openssl-1.1.1t/.openssl/include/openssl/ssl.h \
	objs/ngx_auto_config.h


CORE_INCS = -I src/core \
	-I src/event \
	-I src/event/modules \
	-I src/os/win32 \
	-I objs/nginx-rtmp-module \
	-I objs/pcre2-10.42/src/ \
	-I objs/openssl-1.1.1t/.openssl/include \
	-I objs/zlib-1.2.13 \
	-I objs


HTTP_DEPS = src/http/ngx_http.h \
	src/http/ngx_http_request.h \
	src/http/ngx_http_config.h \
	src/http/ngx_http_core_module.h \
	src/http/ngx_http_cache.h \
	src/http/ngx_http_variables.h \
	src/http/ngx_http_script.h \
	src/http/ngx_http_upstream.h \
	src/http/ngx_http_upstream_round_robin.h \
	src/http/modules/ngx_http_ssi_filter_module.h \
	src/http/v2/ngx_http_v2.h \
	src/http/v2/ngx_http_v2_module.h \
	src/http/modules/ngx_http_ssl_module.h


HTTP_INCS = -I src/http \
	-I src/http/modules \
	-I src/http/v2


MAIL_DEPS = src/mail/ngx_mail.h \
	src/mail/ngx_mail_ssl_module.h \
	src/mail/ngx_mail_pop3_module.h \
	src/mail/ngx_mail_imap_module.h \
	src/mail/ngx_mail_smtp_module.h


MAIL_INCS = -I src/mail


STREAM_DEPS = src/stream/ngx_stream.h \
	src/stream/ngx_stream_variables.h \
	src/stream/ngx_stream_script.h \
	src/stream/ngx_stream_upstream.h \
	src/stream/ngx_stream_upstream_round_robin.h


STREAM_INCS = -I src/stream


ADDON_DEPS = $(CORE_DEPS)                                                                   objs/nginx-rtmp-module/ngx_rtmp_amf.h                               objs/nginx-rtmp-module/ngx_rtmp_bandwidth.h                         objs/nginx-rtmp-module/ngx_rtmp_cmd_module.h                        objs/nginx-rtmp-module/ngx_rtmp_codec_module.h                      objs/nginx-rtmp-module/ngx_rtmp_eval.h                              objs/nginx-rtmp-module/ngx_rtmp.h                                   objs/nginx-rtmp-module/ngx_rtmp_version.h                           objs/nginx-rtmp-module/ngx_rtmp_live_module.h                       objs/nginx-rtmp-module/ngx_rtmp_netcall_module.h                    objs/nginx-rtmp-module/ngx_rtmp_play_module.h                       objs/nginx-rtmp-module/ngx_rtmp_record_module.h                     objs/nginx-rtmp-module/ngx_rtmp_relay_module.h                      objs/nginx-rtmp-module/ngx_rtmp_streams.h                           objs/nginx-rtmp-module/ngx_rtmp_bitop.h                             objs/nginx-rtmp-module/ngx_rtmp_proxy_protocol.h                    objs/nginx-rtmp-module/hls/ngx_rtmp_mpegts.h                        objs/nginx-rtmp-module/dash/ngx_rtmp_mp4.h                           $(HTTP_DEPS) $(MAIL_DEPS) $(STREAM_DEPS)


build:	binary modules manpage

binary:	objs/nginx.exe

objs/nginx.exe:	objs/src/core/nginx.o \
	objs/src/core/ngx_log.o \
	objs/src/core/ngx_palloc.o \
	objs/src/core/ngx_array.o \
	objs/src/core/ngx_list.o \
	objs/src/core/ngx_hash.o \
	objs/src/core/ngx_buf.o \
	objs/src/core/ngx_queue.o \
	objs/src/core/ngx_output_chain.o \
	objs/src/core/ngx_string.o \
	objs/src/core/ngx_parse.o \
	objs/src/core/ngx_parse_time.o \
	objs/src/core/ngx_inet.o \
	objs/src/core/ngx_file.o \
	objs/src/core/ngx_crc32.o \
	objs/src/core/ngx_murmurhash.o \
	objs/src/core/ngx_md5.o \
	objs/src/core/ngx_sha1.o \
	objs/src/core/ngx_rbtree.o \
	objs/src/core/ngx_radix_tree.o \
	objs/src/core/ngx_slab.o \
	objs/src/core/ngx_times.o \
	objs/src/core/ngx_shmtx.o \
	objs/src/core/ngx_connection.o \
	objs/src/core/ngx_cycle.o \
	objs/src/core/ngx_spinlock.o \
	objs/src/core/ngx_rwlock.o \
	objs/src/core/ngx_cpuinfo.o \
	objs/src/core/ngx_conf_file.o \
	objs/src/core/ngx_module.o \
	objs/src/core/ngx_resolver.o \
	objs/src/core/ngx_open_file_cache.o \
	objs/src/core/ngx_crypt.o \
	objs/src/core/ngx_proxy_protocol.o \
	objs/src/core/ngx_syslog.o \
	objs/src/event/ngx_event.o \
	objs/src/event/ngx_event_timer.o \
	objs/src/event/ngx_event_posted.o \
	objs/src/event/ngx_event_accept.o \
	objs/src/event/ngx_event_udp.o \
	objs/src/event/ngx_event_connect.o \
	objs/src/event/ngx_event_pipe.o \
	objs/src/os/win32/ngx_errno.o \
	objs/src/os/win32/ngx_alloc.o \
	objs/src/os/win32/ngx_files.o \
	objs/src/os/win32/ngx_shmem.o \
	objs/src/os/win32/ngx_time.o \
	objs/src/os/win32/ngx_process.o \
	objs/src/os/win32/ngx_thread.o \
	objs/src/os/win32/ngx_socket.o \
	objs/src/os/win32/ngx_wsarecv.o \
	objs/src/os/win32/ngx_wsarecv_chain.o \
	objs/src/os/win32/ngx_udp_wsarecv.o \
	objs/src/os/win32/ngx_wsasend.o \
	objs/src/os/win32/ngx_wsasend_chain.o \
	objs/src/os/win32/ngx_win32_init.o \
	objs/src/os/win32/ngx_user.o \
	objs/src/os/win32/ngx_dlopen.o \
	objs/src/os/win32/ngx_event_log.o \
	objs/src/os/win32/ngx_process_cycle.o \
	objs/src/event/ngx_event_acceptex.o \
	objs/src/event/modules/ngx_iocp_module.o \
	objs/src/event/modules/ngx_win32_select_module.o \
	objs/src/event/modules/ngx_win32_poll_module.o \
	objs/src/event/ngx_event_openssl.o \
	objs/src/event/ngx_event_openssl_stapling.o \
	objs/src/core/ngx_regex.o \
	objs/src/http/ngx_http.o \
	objs/src/http/ngx_http_core_module.o \
	objs/src/http/ngx_http_special_response.o \
	objs/src/http/ngx_http_request.o \
	objs/src/http/ngx_http_parse.o \
	objs/src/http/modules/ngx_http_log_module.o \
	objs/src/http/ngx_http_request_body.o \
	objs/src/http/ngx_http_variables.o \
	objs/src/http/ngx_http_script.o \
	objs/src/http/ngx_http_upstream.o \
	objs/src/http/ngx_http_upstream_round_robin.o \
	objs/src/http/ngx_http_file_cache.o \
	objs/src/http/ngx_http_huff_decode.o \
	objs/src/http/ngx_http_huff_encode.o \
	objs/src/http/ngx_http_write_filter_module.o \
	objs/src/http/ngx_http_header_filter_module.o \
	objs/src/http/modules/ngx_http_chunked_filter_module.o \
	objs/src/http/v2/ngx_http_v2_filter_module.o \
	objs/src/http/modules/ngx_http_range_filter_module.o \
	objs/src/http/modules/ngx_http_gzip_filter_module.o \
	objs/src/http/ngx_http_postpone_filter_module.o \
	objs/src/http/modules/ngx_http_ssi_filter_module.o \
	objs/src/http/modules/ngx_http_charset_filter_module.o \
	objs/src/http/modules/ngx_http_sub_filter_module.o \
	objs/src/http/modules/ngx_http_addition_filter_module.o \
	objs/src/http/modules/ngx_http_gunzip_filter_module.o \
	objs/src/http/modules/ngx_http_userid_filter_module.o \
	objs/src/http/modules/ngx_http_headers_filter_module.o \
	objs/src/http/ngx_http_copy_filter_module.o \
	objs/src/http/modules/ngx_http_not_modified_filter_module.o \
	objs/src/http/v2/ngx_http_v2.o \
	objs/src/http/v2/ngx_http_v2_table.o \
	objs/src/http/v2/ngx_http_v2_encode.o \
	objs/src/http/v2/ngx_http_v2_module.o \
	objs/src/http/modules/ngx_http_static_module.o \
	objs/src/http/modules/ngx_http_gzip_static_module.o \
	objs/src/http/modules/ngx_http_dav_module.o \
	objs/src/http/modules/ngx_http_autoindex_module.o \
	objs/src/http/modules/ngx_http_index_module.o \
	objs/src/http/modules/ngx_http_random_index_module.o \
	objs/src/http/modules/ngx_http_mirror_module.o \
	objs/src/http/modules/ngx_http_try_files_module.o \
	objs/src/http/modules/ngx_http_auth_basic_module.o \
	objs/src/http/modules/ngx_http_access_module.o \
	objs/src/http/modules/ngx_http_limit_conn_module.o \
	objs/src/http/modules/ngx_http_limit_req_module.o \
	objs/src/http/modules/ngx_http_realip_module.o \
	objs/src/http/modules/ngx_http_geo_module.o \
	objs/src/http/modules/ngx_http_map_module.o \
	objs/src/http/modules/ngx_http_split_clients_module.o \
	objs/src/http/modules/ngx_http_referer_module.o \
	objs/src/http/modules/ngx_http_rewrite_module.o \
	objs/src/http/modules/ngx_http_ssl_module.o \
	objs/src/http/modules/ngx_http_proxy_module.o \
	objs/src/http/modules/ngx_http_fastcgi_module.o \
	objs/src/http/modules/ngx_http_uwsgi_module.o \
	objs/src/http/modules/ngx_http_scgi_module.o \
	objs/src/http/modules/ngx_http_grpc_module.o \
	objs/src/http/modules/ngx_http_memcached_module.o \
	objs/src/http/modules/ngx_http_empty_gif_module.o \
	objs/src/http/modules/ngx_http_browser_module.o \
	objs/src/http/modules/ngx_http_secure_link_module.o \
	objs/src/http/modules/ngx_http_flv_module.o \
	objs/src/http/modules/ngx_http_mp4_module.o \
	objs/src/http/modules/ngx_http_upstream_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_ip_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_least_conn_module.o \
	objs/src/http/modules/ngx_http_upstream_random_module.o \
	objs/src/http/modules/ngx_http_upstream_keepalive_module.o \
	objs/src/http/modules/ngx_http_upstream_zone_module.o \
	objs/src/http/modules/ngx_http_stub_status_module.o \
	objs/src/mail/ngx_mail.o \
	objs/src/mail/ngx_mail_core_module.o \
	objs/src/mail/ngx_mail_handler.o \
	objs/src/mail/ngx_mail_parse.o \
	objs/src/mail/ngx_mail_ssl_module.o \
	objs/src/mail/ngx_mail_pop3_module.o \
	objs/src/mail/ngx_mail_pop3_handler.o \
	objs/src/mail/ngx_mail_imap_module.o \
	objs/src/mail/ngx_mail_imap_handler.o \
	objs/src/mail/ngx_mail_smtp_module.o \
	objs/src/mail/ngx_mail_smtp_handler.o \
	objs/src/mail/ngx_mail_auth_http_module.o \
	objs/src/mail/ngx_mail_proxy_module.o \
	objs/src/mail/ngx_mail_realip_module.o \
	objs/src/stream/ngx_stream.o \
	objs/src/stream/ngx_stream_variables.o \
	objs/src/stream/ngx_stream_script.o \
	objs/src/stream/ngx_stream_handler.o \
	objs/src/stream/ngx_stream_core_module.o \
	objs/src/stream/ngx_stream_log_module.o \
	objs/src/stream/ngx_stream_proxy_module.o \
	objs/src/stream/ngx_stream_upstream.o \
	objs/src/stream/ngx_stream_upstream_round_robin.o \
	objs/src/stream/ngx_stream_write_filter_module.o \
	objs/src/stream/ngx_stream_limit_conn_module.o \
	objs/src/stream/ngx_stream_access_module.o \
	objs/src/stream/ngx_stream_geo_module.o \
	objs/src/stream/ngx_stream_map_module.o \
	objs/src/stream/ngx_stream_split_clients_module.o \
	objs/src/stream/ngx_stream_return_module.o \
	objs/src/stream/ngx_stream_set_module.o \
	objs/src/stream/ngx_stream_upstream_hash_module.o \
	objs/src/stream/ngx_stream_upstream_least_conn_module.o \
	objs/src/stream/ngx_stream_upstream_random_module.o \
	objs/src/stream/ngx_stream_upstream_zone_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_init.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_handshake.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_handler.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_amf.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_send.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_shared.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_eval.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_receive.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_core_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_cmd_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_codec_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_access_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_record_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_live_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_play_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_flv_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_mp4_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_netcall_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_relay_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_bandwidth.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_exec_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_auto_push_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_notify_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_log_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_limit_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_bitop.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_proxy_protocol.o \
	objs/addon/hls/ngx_rtmp_hls_module.o \
	objs/addon/dash/ngx_rtmp_dash_module.o \
	objs/addon/hls/ngx_rtmp_mpegts.o \
	objs/addon/dash/ngx_rtmp_mp4.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_stat_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_control_module.o \
	objs/ngx_modules.o \
	src/os/win32/nginx.ico \
	objs/pcre2-10.42/.libs/libpcre2-8.a \
	objs/zlib-1.2.13/libz.a
	$(LINK) -o objs/nginx.exe \
	objs/src/core/nginx.o \
	objs/src/core/ngx_log.o \
	objs/src/core/ngx_palloc.o \
	objs/src/core/ngx_array.o \
	objs/src/core/ngx_list.o \
	objs/src/core/ngx_hash.o \
	objs/src/core/ngx_buf.o \
	objs/src/core/ngx_queue.o \
	objs/src/core/ngx_output_chain.o \
	objs/src/core/ngx_string.o \
	objs/src/core/ngx_parse.o \
	objs/src/core/ngx_parse_time.o \
	objs/src/core/ngx_inet.o \
	objs/src/core/ngx_file.o \
	objs/src/core/ngx_crc32.o \
	objs/src/core/ngx_murmurhash.o \
	objs/src/core/ngx_md5.o \
	objs/src/core/ngx_sha1.o \
	objs/src/core/ngx_rbtree.o \
	objs/src/core/ngx_radix_tree.o \
	objs/src/core/ngx_slab.o \
	objs/src/core/ngx_times.o \
	objs/src/core/ngx_shmtx.o \
	objs/src/core/ngx_connection.o \
	objs/src/core/ngx_cycle.o \
	objs/src/core/ngx_spinlock.o \
	objs/src/core/ngx_rwlock.o \
	objs/src/core/ngx_cpuinfo.o \
	objs/src/core/ngx_conf_file.o \
	objs/src/core/ngx_module.o \
	objs/src/core/ngx_resolver.o \
	objs/src/core/ngx_open_file_cache.o \
	objs/src/core/ngx_crypt.o \
	objs/src/core/ngx_proxy_protocol.o \
	objs/src/core/ngx_syslog.o \
	objs/src/event/ngx_event.o \
	objs/src/event/ngx_event_timer.o \
	objs/src/event/ngx_event_posted.o \
	objs/src/event/ngx_event_accept.o \
	objs/src/event/ngx_event_udp.o \
	objs/src/event/ngx_event_connect.o \
	objs/src/event/ngx_event_pipe.o \
	objs/src/os/win32/ngx_errno.o \
	objs/src/os/win32/ngx_alloc.o \
	objs/src/os/win32/ngx_files.o \
	objs/src/os/win32/ngx_shmem.o \
	objs/src/os/win32/ngx_time.o \
	objs/src/os/win32/ngx_process.o \
	objs/src/os/win32/ngx_thread.o \
	objs/src/os/win32/ngx_socket.o \
	objs/src/os/win32/ngx_wsarecv.o \
	objs/src/os/win32/ngx_wsarecv_chain.o \
	objs/src/os/win32/ngx_udp_wsarecv.o \
	objs/src/os/win32/ngx_wsasend.o \
	objs/src/os/win32/ngx_wsasend_chain.o \
	objs/src/os/win32/ngx_win32_init.o \
	objs/src/os/win32/ngx_user.o \
	objs/src/os/win32/ngx_dlopen.o \
	objs/src/os/win32/ngx_event_log.o \
	objs/src/os/win32/ngx_process_cycle.o \
	objs/src/event/ngx_event_acceptex.o \
	objs/src/event/modules/ngx_iocp_module.o \
	objs/src/event/modules/ngx_win32_select_module.o \
	objs/src/event/modules/ngx_win32_poll_module.o \
	objs/src/event/ngx_event_openssl.o \
	objs/src/event/ngx_event_openssl_stapling.o \
	objs/src/core/ngx_regex.o \
	objs/src/http/ngx_http.o \
	objs/src/http/ngx_http_core_module.o \
	objs/src/http/ngx_http_special_response.o \
	objs/src/http/ngx_http_request.o \
	objs/src/http/ngx_http_parse.o \
	objs/src/http/modules/ngx_http_log_module.o \
	objs/src/http/ngx_http_request_body.o \
	objs/src/http/ngx_http_variables.o \
	objs/src/http/ngx_http_script.o \
	objs/src/http/ngx_http_upstream.o \
	objs/src/http/ngx_http_upstream_round_robin.o \
	objs/src/http/ngx_http_file_cache.o \
	objs/src/http/ngx_http_huff_decode.o \
	objs/src/http/ngx_http_huff_encode.o \
	objs/src/http/ngx_http_write_filter_module.o \
	objs/src/http/ngx_http_header_filter_module.o \
	objs/src/http/modules/ngx_http_chunked_filter_module.o \
	objs/src/http/v2/ngx_http_v2_filter_module.o \
	objs/src/http/modules/ngx_http_range_filter_module.o \
	objs/src/http/modules/ngx_http_gzip_filter_module.o \
	objs/src/http/ngx_http_postpone_filter_module.o \
	objs/src/http/modules/ngx_http_ssi_filter_module.o \
	objs/src/http/modules/ngx_http_charset_filter_module.o \
	objs/src/http/modules/ngx_http_sub_filter_module.o \
	objs/src/http/modules/ngx_http_addition_filter_module.o \
	objs/src/http/modules/ngx_http_gunzip_filter_module.o \
	objs/src/http/modules/ngx_http_userid_filter_module.o \
	objs/src/http/modules/ngx_http_headers_filter_module.o \
	objs/src/http/ngx_http_copy_filter_module.o \
	objs/src/http/modules/ngx_http_not_modified_filter_module.o \
	objs/src/http/v2/ngx_http_v2.o \
	objs/src/http/v2/ngx_http_v2_table.o \
	objs/src/http/v2/ngx_http_v2_encode.o \
	objs/src/http/v2/ngx_http_v2_module.o \
	objs/src/http/modules/ngx_http_static_module.o \
	objs/src/http/modules/ngx_http_gzip_static_module.o \
	objs/src/http/modules/ngx_http_dav_module.o \
	objs/src/http/modules/ngx_http_autoindex_module.o \
	objs/src/http/modules/ngx_http_index_module.o \
	objs/src/http/modules/ngx_http_random_index_module.o \
	objs/src/http/modules/ngx_http_mirror_module.o \
	objs/src/http/modules/ngx_http_try_files_module.o \
	objs/src/http/modules/ngx_http_auth_basic_module.o \
	objs/src/http/modules/ngx_http_access_module.o \
	objs/src/http/modules/ngx_http_limit_conn_module.o \
	objs/src/http/modules/ngx_http_limit_req_module.o \
	objs/src/http/modules/ngx_http_realip_module.o \
	objs/src/http/modules/ngx_http_geo_module.o \
	objs/src/http/modules/ngx_http_map_module.o \
	objs/src/http/modules/ngx_http_split_clients_module.o \
	objs/src/http/modules/ngx_http_referer_module.o \
	objs/src/http/modules/ngx_http_rewrite_module.o \
	objs/src/http/modules/ngx_http_ssl_module.o \
	objs/src/http/modules/ngx_http_proxy_module.o \
	objs/src/http/modules/ngx_http_fastcgi_module.o \
	objs/src/http/modules/ngx_http_uwsgi_module.o \
	objs/src/http/modules/ngx_http_scgi_module.o \
	objs/src/http/modules/ngx_http_grpc_module.o \
	objs/src/http/modules/ngx_http_memcached_module.o \
	objs/src/http/modules/ngx_http_empty_gif_module.o \
	objs/src/http/modules/ngx_http_browser_module.o \
	objs/src/http/modules/ngx_http_secure_link_module.o \
	objs/src/http/modules/ngx_http_flv_module.o \
	objs/src/http/modules/ngx_http_mp4_module.o \
	objs/src/http/modules/ngx_http_upstream_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_ip_hash_module.o \
	objs/src/http/modules/ngx_http_upstream_least_conn_module.o \
	objs/src/http/modules/ngx_http_upstream_random_module.o \
	objs/src/http/modules/ngx_http_upstream_keepalive_module.o \
	objs/src/http/modules/ngx_http_upstream_zone_module.o \
	objs/src/http/modules/ngx_http_stub_status_module.o \
	objs/src/mail/ngx_mail.o \
	objs/src/mail/ngx_mail_core_module.o \
	objs/src/mail/ngx_mail_handler.o \
	objs/src/mail/ngx_mail_parse.o \
	objs/src/mail/ngx_mail_ssl_module.o \
	objs/src/mail/ngx_mail_pop3_module.o \
	objs/src/mail/ngx_mail_pop3_handler.o \
	objs/src/mail/ngx_mail_imap_module.o \
	objs/src/mail/ngx_mail_imap_handler.o \
	objs/src/mail/ngx_mail_smtp_module.o \
	objs/src/mail/ngx_mail_smtp_handler.o \
	objs/src/mail/ngx_mail_auth_http_module.o \
	objs/src/mail/ngx_mail_proxy_module.o \
	objs/src/mail/ngx_mail_realip_module.o \
	objs/src/stream/ngx_stream.o \
	objs/src/stream/ngx_stream_variables.o \
	objs/src/stream/ngx_stream_script.o \
	objs/src/stream/ngx_stream_handler.o \
	objs/src/stream/ngx_stream_core_module.o \
	objs/src/stream/ngx_stream_log_module.o \
	objs/src/stream/ngx_stream_proxy_module.o \
	objs/src/stream/ngx_stream_upstream.o \
	objs/src/stream/ngx_stream_upstream_round_robin.o \
	objs/src/stream/ngx_stream_write_filter_module.o \
	objs/src/stream/ngx_stream_limit_conn_module.o \
	objs/src/stream/ngx_stream_access_module.o \
	objs/src/stream/ngx_stream_geo_module.o \
	objs/src/stream/ngx_stream_map_module.o \
	objs/src/stream/ngx_stream_split_clients_module.o \
	objs/src/stream/ngx_stream_return_module.o \
	objs/src/stream/ngx_stream_set_module.o \
	objs/src/stream/ngx_stream_upstream_hash_module.o \
	objs/src/stream/ngx_stream_upstream_least_conn_module.o \
	objs/src/stream/ngx_stream_upstream_random_module.o \
	objs/src/stream/ngx_stream_upstream_zone_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_init.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_handshake.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_handler.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_amf.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_send.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_shared.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_eval.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_receive.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_core_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_cmd_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_codec_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_access_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_record_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_live_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_play_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_flv_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_mp4_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_netcall_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_relay_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_bandwidth.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_exec_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_auto_push_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_notify_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_log_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_limit_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_bitop.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_proxy_protocol.o \
	objs/addon/hls/ngx_rtmp_hls_module.o \
	objs/addon/dash/ngx_rtmp_dash_module.o \
	objs/addon/hls/ngx_rtmp_mpegts.o \
	objs/addon/dash/ngx_rtmp_mp4.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_stat_module.o \
	objs/addon/nginx-rtmp-module/ngx_rtmp_control_module.o \
	objs/ngx_modules.o \
	-ladvapi32 -lws2_32 objs/pcre2-10.42/.libs/libpcre2-8.a objs/openssl-1.1.1t/.openssl/lib/libssl.a objs/openssl-1.1.1t/.openssl/lib/libcrypto.a -lgdi32 -lcrypt32 -lws2_32 objs/zlib-1.2.13/libz.a \
	-Wl,--export-all-symbols -Wl,--out-implib=objs/libnginx.a
	


modules:

objs/ngx_modules.o:	$(CORE_DEPS) \
	objs/ngx_modules.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/ngx_modules.o \
		objs/ngx_modules.c


objs/src/core/nginx.o:	$(CORE_DEPS) \
	src/core/nginx.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/nginx.o \
		src/core/nginx.c


objs/src/core/ngx_log.o:	$(CORE_DEPS) \
	src/core/ngx_log.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_log.o \
		src/core/ngx_log.c


objs/src/core/ngx_palloc.o:	$(CORE_DEPS) \
	src/core/ngx_palloc.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_palloc.o \
		src/core/ngx_palloc.c


objs/src/core/ngx_array.o:	$(CORE_DEPS) \
	src/core/ngx_array.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_array.o \
		src/core/ngx_array.c


objs/src/core/ngx_list.o:	$(CORE_DEPS) \
	src/core/ngx_list.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_list.o \
		src/core/ngx_list.c


objs/src/core/ngx_hash.o:	$(CORE_DEPS) \
	src/core/ngx_hash.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_hash.o \
		src/core/ngx_hash.c


objs/src/core/ngx_buf.o:	$(CORE_DEPS) \
	src/core/ngx_buf.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_buf.o \
		src/core/ngx_buf.c


objs/src/core/ngx_queue.o:	$(CORE_DEPS) \
	src/core/ngx_queue.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_queue.o \
		src/core/ngx_queue.c


objs/src/core/ngx_output_chain.o:	$(CORE_DEPS) \
	src/core/ngx_output_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_output_chain.o \
		src/core/ngx_output_chain.c


objs/src/core/ngx_string.o:	$(CORE_DEPS) \
	src/core/ngx_string.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_string.o \
		src/core/ngx_string.c


objs/src/core/ngx_parse.o:	$(CORE_DEPS) \
	src/core/ngx_parse.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_parse.o \
		src/core/ngx_parse.c


objs/src/core/ngx_parse_time.o:	$(CORE_DEPS) \
	src/core/ngx_parse_time.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_parse_time.o \
		src/core/ngx_parse_time.c


objs/src/core/ngx_inet.o:	$(CORE_DEPS) \
	src/core/ngx_inet.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_inet.o \
		src/core/ngx_inet.c


objs/src/core/ngx_file.o:	$(CORE_DEPS) \
	src/core/ngx_file.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_file.o \
		src/core/ngx_file.c


objs/src/core/ngx_crc32.o:	$(CORE_DEPS) \
	src/core/ngx_crc32.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_crc32.o \
		src/core/ngx_crc32.c


objs/src/core/ngx_murmurhash.o:	$(CORE_DEPS) \
	src/core/ngx_murmurhash.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_murmurhash.o \
		src/core/ngx_murmurhash.c


objs/src/core/ngx_md5.o:	$(CORE_DEPS) \
	src/core/ngx_md5.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_md5.o \
		src/core/ngx_md5.c


objs/src/core/ngx_sha1.o:	$(CORE_DEPS) \
	src/core/ngx_sha1.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_sha1.o \
		src/core/ngx_sha1.c


objs/src/core/ngx_rbtree.o:	$(CORE_DEPS) \
	src/core/ngx_rbtree.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_rbtree.o \
		src/core/ngx_rbtree.c


objs/src/core/ngx_radix_tree.o:	$(CORE_DEPS) \
	src/core/ngx_radix_tree.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_radix_tree.o \
		src/core/ngx_radix_tree.c


objs/src/core/ngx_slab.o:	$(CORE_DEPS) \
	src/core/ngx_slab.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_slab.o \
		src/core/ngx_slab.c


objs/src/core/ngx_times.o:	$(CORE_DEPS) \
	src/core/ngx_times.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_times.o \
		src/core/ngx_times.c


objs/src/core/ngx_shmtx.o:	$(CORE_DEPS) \
	src/core/ngx_shmtx.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_shmtx.o \
		src/core/ngx_shmtx.c


objs/src/core/ngx_connection.o:	$(CORE_DEPS) \
	src/core/ngx_connection.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_connection.o \
		src/core/ngx_connection.c


objs/src/core/ngx_cycle.o:	$(CORE_DEPS) \
	src/core/ngx_cycle.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_cycle.o \
		src/core/ngx_cycle.c


objs/src/core/ngx_spinlock.o:	$(CORE_DEPS) \
	src/core/ngx_spinlock.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_spinlock.o \
		src/core/ngx_spinlock.c


objs/src/core/ngx_rwlock.o:	$(CORE_DEPS) \
	src/core/ngx_rwlock.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_rwlock.o \
		src/core/ngx_rwlock.c


objs/src/core/ngx_cpuinfo.o:	$(CORE_DEPS) \
	src/core/ngx_cpuinfo.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_cpuinfo.o \
		src/core/ngx_cpuinfo.c


objs/src/core/ngx_conf_file.o:	$(CORE_DEPS) \
	src/core/ngx_conf_file.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_conf_file.o \
		src/core/ngx_conf_file.c


objs/src/core/ngx_module.o:	$(CORE_DEPS) \
	src/core/ngx_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_module.o \
		src/core/ngx_module.c


objs/src/core/ngx_resolver.o:	$(CORE_DEPS) \
	src/core/ngx_resolver.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_resolver.o \
		src/core/ngx_resolver.c


objs/src/core/ngx_open_file_cache.o:	$(CORE_DEPS) \
	src/core/ngx_open_file_cache.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_open_file_cache.o \
		src/core/ngx_open_file_cache.c


objs/src/core/ngx_crypt.o:	$(CORE_DEPS) \
	src/core/ngx_crypt.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_crypt.o \
		src/core/ngx_crypt.c


objs/src/core/ngx_proxy_protocol.o:	$(CORE_DEPS) \
	src/core/ngx_proxy_protocol.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_proxy_protocol.o \
		src/core/ngx_proxy_protocol.c


objs/src/core/ngx_syslog.o:	$(CORE_DEPS) \
	src/core/ngx_syslog.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_syslog.o \
		src/core/ngx_syslog.c


objs/src/event/ngx_event.o:	$(CORE_DEPS) \
	src/event/ngx_event.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event.o \
		src/event/ngx_event.c


objs/src/event/ngx_event_timer.o:	$(CORE_DEPS) \
	src/event/ngx_event_timer.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_timer.o \
		src/event/ngx_event_timer.c


objs/src/event/ngx_event_posted.o:	$(CORE_DEPS) \
	src/event/ngx_event_posted.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_posted.o \
		src/event/ngx_event_posted.c


objs/src/event/ngx_event_accept.o:	$(CORE_DEPS) \
	src/event/ngx_event_accept.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_accept.o \
		src/event/ngx_event_accept.c


objs/src/event/ngx_event_udp.o:	$(CORE_DEPS) \
	src/event/ngx_event_udp.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_udp.o \
		src/event/ngx_event_udp.c


objs/src/event/ngx_event_connect.o:	$(CORE_DEPS) \
	src/event/ngx_event_connect.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_connect.o \
		src/event/ngx_event_connect.c


objs/src/event/ngx_event_pipe.o:	$(CORE_DEPS) \
	src/event/ngx_event_pipe.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_pipe.o \
		src/event/ngx_event_pipe.c


objs/src/os/win32/ngx_errno.o:	$(CORE_DEPS) \
	src/os/win32/ngx_errno.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_errno.o \
		src/os/win32/ngx_errno.c


objs/src/os/win32/ngx_alloc.o:	$(CORE_DEPS) \
	src/os/win32/ngx_alloc.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_alloc.o \
		src/os/win32/ngx_alloc.c


objs/src/os/win32/ngx_files.o:	$(CORE_DEPS) \
	src/os/win32/ngx_files.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_files.o \
		src/os/win32/ngx_files.c


objs/src/os/win32/ngx_shmem.o:	$(CORE_DEPS) \
	src/os/win32/ngx_shmem.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_shmem.o \
		src/os/win32/ngx_shmem.c


objs/src/os/win32/ngx_time.o:	$(CORE_DEPS) \
	src/os/win32/ngx_time.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_time.o \
		src/os/win32/ngx_time.c


objs/src/os/win32/ngx_process.o:	$(CORE_DEPS) \
	src/os/win32/ngx_process.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_process.o \
		src/os/win32/ngx_process.c


objs/src/os/win32/ngx_thread.o:	$(CORE_DEPS) \
	src/os/win32/ngx_thread.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_thread.o \
		src/os/win32/ngx_thread.c


objs/src/os/win32/ngx_socket.o:	$(CORE_DEPS) \
	src/os/win32/ngx_socket.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_socket.o \
		src/os/win32/ngx_socket.c


objs/src/os/win32/ngx_wsarecv.o:	$(CORE_DEPS) \
	src/os/win32/ngx_wsarecv.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_wsarecv.o \
		src/os/win32/ngx_wsarecv.c


objs/src/os/win32/ngx_wsarecv_chain.o:	$(CORE_DEPS) \
	src/os/win32/ngx_wsarecv_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_wsarecv_chain.o \
		src/os/win32/ngx_wsarecv_chain.c


objs/src/os/win32/ngx_udp_wsarecv.o:	$(CORE_DEPS) \
	src/os/win32/ngx_udp_wsarecv.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_udp_wsarecv.o \
		src/os/win32/ngx_udp_wsarecv.c


objs/src/os/win32/ngx_wsasend.o:	$(CORE_DEPS) \
	src/os/win32/ngx_wsasend.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_wsasend.o \
		src/os/win32/ngx_wsasend.c


objs/src/os/win32/ngx_wsasend_chain.o:	$(CORE_DEPS) \
	src/os/win32/ngx_wsasend_chain.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_wsasend_chain.o \
		src/os/win32/ngx_wsasend_chain.c


objs/src/os/win32/ngx_win32_init.o:	$(CORE_DEPS) \
	src/os/win32/ngx_win32_init.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_win32_init.o \
		src/os/win32/ngx_win32_init.c


objs/src/os/win32/ngx_user.o:	$(CORE_DEPS) \
	src/os/win32/ngx_user.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_user.o \
		src/os/win32/ngx_user.c


objs/src/os/win32/ngx_dlopen.o:	$(CORE_DEPS) \
	src/os/win32/ngx_dlopen.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_dlopen.o \
		src/os/win32/ngx_dlopen.c


objs/src/os/win32/ngx_event_log.o:	$(CORE_DEPS) \
	src/os/win32/ngx_event_log.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_event_log.o \
		src/os/win32/ngx_event_log.c


objs/src/os/win32/ngx_process_cycle.o:	$(CORE_DEPS) \
	src/os/win32/ngx_process_cycle.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/os/win32/ngx_process_cycle.o \
		src/os/win32/ngx_process_cycle.c


objs/src/event/ngx_event_acceptex.o:	$(CORE_DEPS) \
	src/event/ngx_event_acceptex.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_acceptex.o \
		src/event/ngx_event_acceptex.c


objs/src/event/modules/ngx_iocp_module.o:	$(CORE_DEPS) \
	src/event/modules/ngx_iocp_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/modules/ngx_iocp_module.o \
		src/event/modules/ngx_iocp_module.c


objs/src/event/modules/ngx_win32_select_module.o:	$(CORE_DEPS) \
	src/event/modules/ngx_win32_select_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/modules/ngx_win32_select_module.o \
		src/event/modules/ngx_win32_select_module.c


objs/src/event/modules/ngx_win32_poll_module.o:	$(CORE_DEPS) \
	src/event/modules/ngx_win32_poll_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/modules/ngx_win32_poll_module.o \
		src/event/modules/ngx_win32_poll_module.c


objs/src/event/ngx_event_openssl.o:	$(CORE_DEPS) \
	src/event/ngx_event_openssl.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_openssl.o \
		src/event/ngx_event_openssl.c


objs/src/event/ngx_event_openssl_stapling.o:	$(CORE_DEPS) \
	src/event/ngx_event_openssl_stapling.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/event/ngx_event_openssl_stapling.o \
		src/event/ngx_event_openssl_stapling.c


objs/src/core/ngx_regex.o:	$(CORE_DEPS) \
	src/core/ngx_regex.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) \
		-o objs/src/core/ngx_regex.o \
		src/core/ngx_regex.c


objs/src/http/ngx_http.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http.o \
		src/http/ngx_http.c


objs/src/http/ngx_http_core_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_core_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_core_module.o \
		src/http/ngx_http_core_module.c


objs/src/http/ngx_http_special_response.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_special_response.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_special_response.o \
		src/http/ngx_http_special_response.c


objs/src/http/ngx_http_request.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_request.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_request.o \
		src/http/ngx_http_request.c


objs/src/http/ngx_http_parse.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_parse.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_parse.o \
		src/http/ngx_http_parse.c


objs/src/http/modules/ngx_http_log_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_log_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_log_module.o \
		src/http/modules/ngx_http_log_module.c


objs/src/http/ngx_http_request_body.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_request_body.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_request_body.o \
		src/http/ngx_http_request_body.c


objs/src/http/ngx_http_variables.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_variables.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_variables.o \
		src/http/ngx_http_variables.c


objs/src/http/ngx_http_script.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_script.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_script.o \
		src/http/ngx_http_script.c


objs/src/http/ngx_http_upstream.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_upstream.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_upstream.o \
		src/http/ngx_http_upstream.c


objs/src/http/ngx_http_upstream_round_robin.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_upstream_round_robin.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_upstream_round_robin.o \
		src/http/ngx_http_upstream_round_robin.c


objs/src/http/ngx_http_file_cache.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_file_cache.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_file_cache.o \
		src/http/ngx_http_file_cache.c


objs/src/http/ngx_http_huff_decode.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_huff_decode.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_huff_decode.o \
		src/http/ngx_http_huff_decode.c


objs/src/http/ngx_http_huff_encode.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_huff_encode.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_huff_encode.o \
		src/http/ngx_http_huff_encode.c


objs/src/http/ngx_http_write_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_write_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_write_filter_module.o \
		src/http/ngx_http_write_filter_module.c


objs/src/http/ngx_http_header_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_header_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_header_filter_module.o \
		src/http/ngx_http_header_filter_module.c


objs/src/http/modules/ngx_http_chunked_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_chunked_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_chunked_filter_module.o \
		src/http/modules/ngx_http_chunked_filter_module.c


objs/src/http/v2/ngx_http_v2_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/v2/ngx_http_v2_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/v2/ngx_http_v2_filter_module.o \
		src/http/v2/ngx_http_v2_filter_module.c


objs/src/http/modules/ngx_http_range_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_range_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_range_filter_module.o \
		src/http/modules/ngx_http_range_filter_module.c


objs/src/http/modules/ngx_http_gzip_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gzip_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_gzip_filter_module.o \
		src/http/modules/ngx_http_gzip_filter_module.c


objs/src/http/ngx_http_postpone_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_postpone_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_postpone_filter_module.o \
		src/http/ngx_http_postpone_filter_module.c


objs/src/http/modules/ngx_http_ssi_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_ssi_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_ssi_filter_module.o \
		src/http/modules/ngx_http_ssi_filter_module.c


objs/src/http/modules/ngx_http_charset_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_charset_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_charset_filter_module.o \
		src/http/modules/ngx_http_charset_filter_module.c


objs/src/http/modules/ngx_http_sub_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_sub_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_sub_filter_module.o \
		src/http/modules/ngx_http_sub_filter_module.c


objs/src/http/modules/ngx_http_addition_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_addition_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_addition_filter_module.o \
		src/http/modules/ngx_http_addition_filter_module.c


objs/src/http/modules/ngx_http_gunzip_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gunzip_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_gunzip_filter_module.o \
		src/http/modules/ngx_http_gunzip_filter_module.c


objs/src/http/modules/ngx_http_userid_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_userid_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_userid_filter_module.o \
		src/http/modules/ngx_http_userid_filter_module.c


objs/src/http/modules/ngx_http_headers_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_headers_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_headers_filter_module.o \
		src/http/modules/ngx_http_headers_filter_module.c


objs/src/http/ngx_http_copy_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_copy_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/ngx_http_copy_filter_module.o \
		src/http/ngx_http_copy_filter_module.c


objs/src/http/modules/ngx_http_not_modified_filter_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_not_modified_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_not_modified_filter_module.o \
		src/http/modules/ngx_http_not_modified_filter_module.c


objs/src/http/v2/ngx_http_v2.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/v2/ngx_http_v2.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/v2/ngx_http_v2.o \
		src/http/v2/ngx_http_v2.c


objs/src/http/v2/ngx_http_v2_table.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/v2/ngx_http_v2_table.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/v2/ngx_http_v2_table.o \
		src/http/v2/ngx_http_v2_table.c


objs/src/http/v2/ngx_http_v2_encode.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/v2/ngx_http_v2_encode.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/v2/ngx_http_v2_encode.o \
		src/http/v2/ngx_http_v2_encode.c


objs/src/http/v2/ngx_http_v2_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/v2/ngx_http_v2_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/v2/ngx_http_v2_module.o \
		src/http/v2/ngx_http_v2_module.c


objs/src/http/modules/ngx_http_static_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_static_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_static_module.o \
		src/http/modules/ngx_http_static_module.c


objs/src/http/modules/ngx_http_gzip_static_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gzip_static_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_gzip_static_module.o \
		src/http/modules/ngx_http_gzip_static_module.c


objs/src/http/modules/ngx_http_dav_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_dav_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_dav_module.o \
		src/http/modules/ngx_http_dav_module.c


objs/src/http/modules/ngx_http_autoindex_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_autoindex_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_autoindex_module.o \
		src/http/modules/ngx_http_autoindex_module.c


objs/src/http/modules/ngx_http_index_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_index_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_index_module.o \
		src/http/modules/ngx_http_index_module.c


objs/src/http/modules/ngx_http_random_index_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_random_index_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_random_index_module.o \
		src/http/modules/ngx_http_random_index_module.c


objs/src/http/modules/ngx_http_mirror_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_mirror_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_mirror_module.o \
		src/http/modules/ngx_http_mirror_module.c


objs/src/http/modules/ngx_http_try_files_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_try_files_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_try_files_module.o \
		src/http/modules/ngx_http_try_files_module.c


objs/src/http/modules/ngx_http_auth_basic_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_auth_basic_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_auth_basic_module.o \
		src/http/modules/ngx_http_auth_basic_module.c


objs/src/http/modules/ngx_http_access_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_access_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_access_module.o \
		src/http/modules/ngx_http_access_module.c


objs/src/http/modules/ngx_http_limit_conn_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_limit_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_limit_conn_module.o \
		src/http/modules/ngx_http_limit_conn_module.c


objs/src/http/modules/ngx_http_limit_req_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_limit_req_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_limit_req_module.o \
		src/http/modules/ngx_http_limit_req_module.c


objs/src/http/modules/ngx_http_realip_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_realip_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_realip_module.o \
		src/http/modules/ngx_http_realip_module.c


objs/src/http/modules/ngx_http_geo_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_geo_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_geo_module.o \
		src/http/modules/ngx_http_geo_module.c


objs/src/http/modules/ngx_http_map_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_map_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_map_module.o \
		src/http/modules/ngx_http_map_module.c


objs/src/http/modules/ngx_http_split_clients_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_split_clients_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_split_clients_module.o \
		src/http/modules/ngx_http_split_clients_module.c


objs/src/http/modules/ngx_http_referer_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_referer_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_referer_module.o \
		src/http/modules/ngx_http_referer_module.c


objs/src/http/modules/ngx_http_rewrite_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_rewrite_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_rewrite_module.o \
		src/http/modules/ngx_http_rewrite_module.c


objs/src/http/modules/ngx_http_ssl_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_ssl_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_ssl_module.o \
		src/http/modules/ngx_http_ssl_module.c


objs/src/http/modules/ngx_http_proxy_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_proxy_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_proxy_module.o \
		src/http/modules/ngx_http_proxy_module.c


objs/src/http/modules/ngx_http_fastcgi_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_fastcgi_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_fastcgi_module.o \
		src/http/modules/ngx_http_fastcgi_module.c


objs/src/http/modules/ngx_http_uwsgi_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_uwsgi_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_uwsgi_module.o \
		src/http/modules/ngx_http_uwsgi_module.c


objs/src/http/modules/ngx_http_scgi_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_scgi_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_scgi_module.o \
		src/http/modules/ngx_http_scgi_module.c


objs/src/http/modules/ngx_http_grpc_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_grpc_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_grpc_module.o \
		src/http/modules/ngx_http_grpc_module.c


objs/src/http/modules/ngx_http_memcached_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_memcached_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_memcached_module.o \
		src/http/modules/ngx_http_memcached_module.c


objs/src/http/modules/ngx_http_empty_gif_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_empty_gif_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_empty_gif_module.o \
		src/http/modules/ngx_http_empty_gif_module.c


objs/src/http/modules/ngx_http_browser_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_browser_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_browser_module.o \
		src/http/modules/ngx_http_browser_module.c


objs/src/http/modules/ngx_http_secure_link_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_secure_link_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_secure_link_module.o \
		src/http/modules/ngx_http_secure_link_module.c


objs/src/http/modules/ngx_http_flv_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_flv_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_flv_module.o \
		src/http/modules/ngx_http_flv_module.c


objs/src/http/modules/ngx_http_mp4_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_mp4_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_mp4_module.o \
		src/http/modules/ngx_http_mp4_module.c


objs/src/http/modules/ngx_http_upstream_hash_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_hash_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_hash_module.o \
		src/http/modules/ngx_http_upstream_hash_module.c


objs/src/http/modules/ngx_http_upstream_ip_hash_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_ip_hash_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_ip_hash_module.o \
		src/http/modules/ngx_http_upstream_ip_hash_module.c


objs/src/http/modules/ngx_http_upstream_least_conn_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_least_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_least_conn_module.o \
		src/http/modules/ngx_http_upstream_least_conn_module.c


objs/src/http/modules/ngx_http_upstream_random_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_random_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_random_module.o \
		src/http/modules/ngx_http_upstream_random_module.c


objs/src/http/modules/ngx_http_upstream_keepalive_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_keepalive_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_keepalive_module.o \
		src/http/modules/ngx_http_upstream_keepalive_module.c


objs/src/http/modules/ngx_http_upstream_zone_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_zone_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_upstream_zone_module.o \
		src/http/modules/ngx_http_upstream_zone_module.c


objs/src/http/modules/ngx_http_stub_status_module.o:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_stub_status_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(HTTP_INCS) \
		-o objs/src/http/modules/ngx_http_stub_status_module.o \
		src/http/modules/ngx_http_stub_status_module.c


objs/src/mail/ngx_mail.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail.o \
		src/mail/ngx_mail.c


objs/src/mail/ngx_mail_core_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_core_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_core_module.o \
		src/mail/ngx_mail_core_module.c


objs/src/mail/ngx_mail_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_handler.o \
		src/mail/ngx_mail_handler.c


objs/src/mail/ngx_mail_parse.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_parse.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_parse.o \
		src/mail/ngx_mail_parse.c


objs/src/mail/ngx_mail_ssl_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_ssl_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_ssl_module.o \
		src/mail/ngx_mail_ssl_module.c


objs/src/mail/ngx_mail_pop3_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_pop3_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_pop3_module.o \
		src/mail/ngx_mail_pop3_module.c


objs/src/mail/ngx_mail_pop3_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_pop3_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_pop3_handler.o \
		src/mail/ngx_mail_pop3_handler.c


objs/src/mail/ngx_mail_imap_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_imap_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_imap_module.o \
		src/mail/ngx_mail_imap_module.c


objs/src/mail/ngx_mail_imap_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_imap_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_imap_handler.o \
		src/mail/ngx_mail_imap_handler.c


objs/src/mail/ngx_mail_smtp_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_smtp_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_smtp_module.o \
		src/mail/ngx_mail_smtp_module.c


objs/src/mail/ngx_mail_smtp_handler.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_smtp_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_smtp_handler.o \
		src/mail/ngx_mail_smtp_handler.c


objs/src/mail/ngx_mail_auth_http_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_auth_http_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_auth_http_module.o \
		src/mail/ngx_mail_auth_http_module.c


objs/src/mail/ngx_mail_proxy_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_proxy_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_proxy_module.o \
		src/mail/ngx_mail_proxy_module.c


objs/src/mail/ngx_mail_realip_module.o:	$(CORE_DEPS) $(MAIL_DEPS) \
	src/mail/ngx_mail_realip_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(MAIL_INCS) \
		-o objs/src/mail/ngx_mail_realip_module.o \
		src/mail/ngx_mail_realip_module.c


objs/src/stream/ngx_stream.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream.o \
		src/stream/ngx_stream.c


objs/src/stream/ngx_stream_variables.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_variables.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_variables.o \
		src/stream/ngx_stream_variables.c


objs/src/stream/ngx_stream_script.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_script.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_script.o \
		src/stream/ngx_stream_script.c


objs/src/stream/ngx_stream_handler.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_handler.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_handler.o \
		src/stream/ngx_stream_handler.c


objs/src/stream/ngx_stream_core_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_core_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_core_module.o \
		src/stream/ngx_stream_core_module.c


objs/src/stream/ngx_stream_log_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_log_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_log_module.o \
		src/stream/ngx_stream_log_module.c


objs/src/stream/ngx_stream_proxy_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_proxy_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_proxy_module.o \
		src/stream/ngx_stream_proxy_module.c


objs/src/stream/ngx_stream_upstream.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream.o \
		src/stream/ngx_stream_upstream.c


objs/src/stream/ngx_stream_upstream_round_robin.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_round_robin.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_round_robin.o \
		src/stream/ngx_stream_upstream_round_robin.c


objs/src/stream/ngx_stream_write_filter_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_write_filter_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_write_filter_module.o \
		src/stream/ngx_stream_write_filter_module.c


objs/src/stream/ngx_stream_limit_conn_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_limit_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_limit_conn_module.o \
		src/stream/ngx_stream_limit_conn_module.c


objs/src/stream/ngx_stream_access_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_access_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_access_module.o \
		src/stream/ngx_stream_access_module.c


objs/src/stream/ngx_stream_geo_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_geo_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_geo_module.o \
		src/stream/ngx_stream_geo_module.c


objs/src/stream/ngx_stream_map_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_map_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_map_module.o \
		src/stream/ngx_stream_map_module.c


objs/src/stream/ngx_stream_split_clients_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_split_clients_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_split_clients_module.o \
		src/stream/ngx_stream_split_clients_module.c


objs/src/stream/ngx_stream_return_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_return_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_return_module.o \
		src/stream/ngx_stream_return_module.c


objs/src/stream/ngx_stream_set_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_set_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_set_module.o \
		src/stream/ngx_stream_set_module.c


objs/src/stream/ngx_stream_upstream_hash_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_hash_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_hash_module.o \
		src/stream/ngx_stream_upstream_hash_module.c


objs/src/stream/ngx_stream_upstream_least_conn_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_least_conn_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_least_conn_module.o \
		src/stream/ngx_stream_upstream_least_conn_module.c


objs/src/stream/ngx_stream_upstream_random_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_random_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_random_module.o \
		src/stream/ngx_stream_upstream_random_module.c


objs/src/stream/ngx_stream_upstream_zone_module.o:	$(CORE_DEPS) $(STREAM_DEPS) \
	src/stream/ngx_stream_upstream_zone_module.c
	$(CC) -c $(CFLAGS) $(CORE_INCS) $(STREAM_INCS) \
		-o objs/src/stream/ngx_stream_upstream_zone_module.o \
		src/stream/ngx_stream_upstream_zone_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp.o \
		objs/nginx-rtmp-module/ngx_rtmp.c


objs/addon/nginx-rtmp-module/ngx_rtmp_init.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_init.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_init.o \
		objs/nginx-rtmp-module/ngx_rtmp_init.c


objs/addon/nginx-rtmp-module/ngx_rtmp_handshake.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_handshake.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_handshake.o \
		objs/nginx-rtmp-module/ngx_rtmp_handshake.c


objs/addon/nginx-rtmp-module/ngx_rtmp_handler.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_handler.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_handler.o \
		objs/nginx-rtmp-module/ngx_rtmp_handler.c


objs/addon/nginx-rtmp-module/ngx_rtmp_amf.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_amf.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_amf.o \
		objs/nginx-rtmp-module/ngx_rtmp_amf.c


objs/addon/nginx-rtmp-module/ngx_rtmp_send.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_send.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_send.o \
		objs/nginx-rtmp-module/ngx_rtmp_send.c


objs/addon/nginx-rtmp-module/ngx_rtmp_shared.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_shared.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_shared.o \
		objs/nginx-rtmp-module/ngx_rtmp_shared.c


objs/addon/nginx-rtmp-module/ngx_rtmp_eval.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_eval.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_eval.o \
		objs/nginx-rtmp-module/ngx_rtmp_eval.c


objs/addon/nginx-rtmp-module/ngx_rtmp_receive.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_receive.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_receive.o \
		objs/nginx-rtmp-module/ngx_rtmp_receive.c


objs/addon/nginx-rtmp-module/ngx_rtmp_core_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_core_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_core_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_core_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_cmd_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_cmd_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_cmd_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_cmd_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_codec_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_codec_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_codec_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_codec_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_access_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_access_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_access_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_access_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_record_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_record_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_record_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_record_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_live_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_live_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_live_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_live_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_play_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_play_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_play_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_play_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_flv_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_flv_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_flv_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_flv_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_mp4_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_mp4_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_mp4_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_mp4_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_netcall_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_netcall_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_netcall_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_netcall_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_relay_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_relay_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_relay_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_relay_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_bandwidth.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_bandwidth.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_bandwidth.o \
		objs/nginx-rtmp-module/ngx_rtmp_bandwidth.c


objs/addon/nginx-rtmp-module/ngx_rtmp_exec_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_exec_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_exec_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_exec_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_auto_push_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_auto_push_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_auto_push_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_auto_push_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_notify_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_notify_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_notify_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_notify_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_log_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_log_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_log_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_log_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_limit_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_limit_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_limit_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_limit_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_bitop.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_bitop.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_bitop.o \
		objs/nginx-rtmp-module/ngx_rtmp_bitop.c


objs/addon/nginx-rtmp-module/ngx_rtmp_proxy_protocol.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_proxy_protocol.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_proxy_protocol.o \
		objs/nginx-rtmp-module/ngx_rtmp_proxy_protocol.c


objs/addon/hls/ngx_rtmp_hls_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/hls/ngx_rtmp_hls_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/hls/ngx_rtmp_hls_module.o \
		objs/nginx-rtmp-module/hls/ngx_rtmp_hls_module.c


objs/addon/dash/ngx_rtmp_dash_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/dash/ngx_rtmp_dash_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/dash/ngx_rtmp_dash_module.o \
		objs/nginx-rtmp-module/dash/ngx_rtmp_dash_module.c


objs/addon/hls/ngx_rtmp_mpegts.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/hls/ngx_rtmp_mpegts.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/hls/ngx_rtmp_mpegts.o \
		objs/nginx-rtmp-module/hls/ngx_rtmp_mpegts.c


objs/addon/dash/ngx_rtmp_mp4.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/dash/ngx_rtmp_mp4.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/dash/ngx_rtmp_mp4.o \
		objs/nginx-rtmp-module/dash/ngx_rtmp_mp4.c


objs/addon/nginx-rtmp-module/ngx_rtmp_stat_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_stat_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_stat_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_stat_module.c


objs/addon/nginx-rtmp-module/ngx_rtmp_control_module.o:	$(ADDON_DEPS) \
	objs/nginx-rtmp-module/ngx_rtmp_control_module.c
	$(CC) -c $(CFLAGS)  $(ALL_INCS) \
		-o objs/addon/nginx-rtmp-module/ngx_rtmp_control_module.o \
		objs/nginx-rtmp-module/ngx_rtmp_control_module.c


objs/pcre2-10.42/src/pcre2.h:	objs/pcre2-10.42/Makefile

objs/pcre2-10.42/Makefile:	objs/Makefile
	cd objs/pcre2-10.42 \
	&& if [ -f Makefile ]; then $(MAKE) distclean; fi \
	&& CC="$(CC)" CFLAGS="-O2 -fomit-frame-pointer -pipe " \
	./configure --disable-shared 

objs/pcre2-10.42/.libs/libpcre2-8.a:	objs/pcre2-10.42/Makefile
	cd objs/pcre2-10.42 \
	&& $(MAKE) libpcre2-8.la


objs/openssl-1.1.1t/.openssl/include/openssl/ssl.h:	objs/Makefile
	cd objs/openssl-1.1.1t \
	&& if [ -f Makefile ]; then $(MAKE) clean; fi \
	&& ./config --prefix=/home/nginx-1.23.4/objs/openssl-1.1.1t/.openssl no-shared no-threads no-asm \
	&& $(MAKE) \
	&& $(MAKE) install_sw LIBDIR=lib


objs/zlib-1.2.13/libz.a:	objs/Makefile
	cd objs/zlib-1.2.13 \
	&& $(MAKE) distclean \
	&& $(MAKE) -f win32/Makefile.gcc \
		CFLAGS="-O2 -fomit-frame-pointer -pipe " CC="$(CC)" \
		libz.a


manpage:	objs/nginx.8

objs/nginx.8:	man/nginx.8 objs/ngx_auto_config.h
	sed -e "s|%%PREFIX%%|.|" \
		-e "s|%%PID_PATH%%|./logs/nginx.pid|" \
		-e "s|%%CONF_PATH%%|./conf/nginx.conf|" \
		-e "s|%%ERROR_LOG_PATH%%|./logs/error.log|" \
		< man/nginx.8 > $@

install:	build 
	test -d '$(DESTDIR).' || mkdir -p '$(DESTDIR).'

	test -d '$(DESTDIR).' \
		|| mkdir -p '$(DESTDIR).'
	test ! -f '$(DESTDIR)./nginx.exe' \
		|| mv '$(DESTDIR)./nginx.exe' \
			'$(DESTDIR)./nginx.exe.old'
	cp objs/nginx '$(DESTDIR)./nginx.exe'

	test -d '$(DESTDIR)./conf' \
		|| mkdir -p '$(DESTDIR)./conf'

	cp conf/koi-win '$(DESTDIR)./conf'
	cp conf/koi-utf '$(DESTDIR)./conf'
	cp conf/win-utf '$(DESTDIR)./conf'

	test -f '$(DESTDIR)./conf/mime.types' \
		|| cp conf/mime.types '$(DESTDIR)./conf'
	cp conf/mime.types '$(DESTDIR)./conf/mime.types.default'

	test -f '$(DESTDIR)./conf/fastcgi_params' \
		|| cp conf/fastcgi_params '$(DESTDIR)./conf'
	cp conf/fastcgi_params \
		'$(DESTDIR)./conf/fastcgi_params.default'

	test -f '$(DESTDIR)./conf/fastcgi.conf' \
		|| cp conf/fastcgi.conf '$(DESTDIR)./conf'
	cp conf/fastcgi.conf '$(DESTDIR)./conf/fastcgi.conf.default'

	test -f '$(DESTDIR)./conf/uwsgi_params' \
		|| cp conf/uwsgi_params '$(DESTDIR)./conf'
	cp conf/uwsgi_params \
		'$(DESTDIR)./conf/uwsgi_params.default'

	test -f '$(DESTDIR)./conf/scgi_params' \
		|| cp conf/scgi_params '$(DESTDIR)./conf'
	cp conf/scgi_params \
		'$(DESTDIR)./conf/scgi_params.default'

	test -f '$(DESTDIR)./conf/nginx.conf' \
		|| cp conf/nginx.conf '$(DESTDIR)./conf/nginx.conf'
	cp conf/nginx.conf '$(DESTDIR)./conf/nginx.conf.default'

	test -d '$(DESTDIR)./logs' \
		|| mkdir -p '$(DESTDIR)./logs'

	test -d '$(DESTDIR)./logs' \
		|| mkdir -p '$(DESTDIR)./logs'

	test -d '$(DESTDIR)./html' \
		|| cp -R html '$(DESTDIR).'

	test -d '$(DESTDIR)./logs' \
		|| mkdir -p '$(DESTDIR)./logs'
