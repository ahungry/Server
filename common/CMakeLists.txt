CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

SET(common_sources
	base_packet.cpp
	classes.cpp
	condition.cpp
	crash.cpp
	crc16.cpp
	crc32.cpp
	database.cpp
	database_conversions.cpp
	database_instances.cpp
	dbcore.cpp
	deity.cpp
	emu_constants.cpp
	emu_legacy.cpp
	emu_limits.cpp
	emu_opcodes.cpp
	emu_tcp_connection.cpp
	emu_tcp_server.cpp
	emu_versions.cpp
	eqdb.cpp
	eqdb_res.cpp
	eqemu_exception.cpp
	eqemu_config.cpp
	eqemu_logsys.cpp
	eq_limits.cpp
	eq_packet.cpp
	eq_stream.cpp
	eq_stream_factory.cpp
	eq_stream_ident.cpp
	eq_stream_proxy.cpp
	eqtime.cpp
	extprofile.cpp
	faction.cpp
	guild_base.cpp
	guilds.cpp
	ipc_mutex.cpp
	item.cpp
	item_base.cpp
	light_source.cpp
	md5.cpp
	memory_buffer.cpp
	memory_mapped_file.cpp
	misc.cpp
	misc_functions.cpp
	mutex.cpp
	mysql_request_result.cpp
	mysql_request_row.cpp
	opcode_map.cpp
	opcodemgr.cpp
	packet_dump.cpp
	packet_dump_file.cpp
	packet_functions.cpp
	perl_eqdb.cpp
	perl_eqdb_res.cpp
	proc_launcher.cpp
	ptimer.cpp
	races.cpp
	rdtsc.cpp
	rulesys.cpp
	say_link.cpp
	serverinfo.cpp
	shareddb.cpp
	skills.cpp
	spdat.cpp
	string_util.cpp
	struct_strategy.cpp
	tcp_connection.cpp
	tcp_server.cpp
	textures.cpp
	timeoutmgr.cpp
	timer.cpp
	unix.cpp
	worldconn.cpp
	xml_parser.cpp
	platform.cpp
	patches/patches.cpp
	patches/sod.cpp
	patches/sod_limits.cpp
	patches/sof.cpp
	patches/sof_limits.cpp
	patches/rof.cpp
	patches/rof_limits.cpp
	patches/rof2.cpp
	patches/rof2_limits.cpp
	patches/titanium.cpp
	patches/titanium_limits.cpp
	patches/uf.cpp
	patches/uf_limits.cpp
	SocketLib/Base64.cpp
	SocketLib/File.cpp
	SocketLib/HttpdCookies.cpp
	SocketLib/HttpdForm.cpp
	SocketLib/HttpdSocket.cpp
	SocketLib/HTTPSocket.cpp
	SocketLib/MemFile.cpp
	SocketLib/Mime.cpp
	SocketLib/Parse.cpp
	SocketLib/socket_include.cpp
	SocketLib/Utility.cpp
	StackWalker/StackWalker.cpp
	tinyxml/tinystr.cpp
	tinyxml/tinyxml.cpp
	tinyxml/tinyxmlerror.cpp
	tinyxml/tinyxmlparser.cpp
)

SET(common_headers
	any.h
	base_packet.h
	base_data.h
	bodytypes.h
	classes.h
	condition.h
	crash.h
	crc16.h
	crc32.h
	data_verification.h
	database.h
	dbcore.h
	deity.h
	emu_constants.h
	emu_legacy.h
	emu_limits.h
	emu_opcodes.h
	emu_oplist.h
	emu_tcp_connection.h
	emu_tcp_server.h
	emu_versions.h
	eq_constants.h
	eq_packet_structs.h
	eqdb.h
	eqdb_res.h
	eqemu_exception.h
	eqemu_config.h
	eqemu_config_elements.h
	eqemu_logsys.h
	eq_limits.h
	eq_packet.h
	eq_stream.h
	eq_stream_factory.h
	eq_stream_ident.h
	eq_stream_intf.h
	eq_stream_locator.h
	eq_stream_proxy.h
	eq_stream_type.h
	eqtime.h
	errmsg.h
	extprofile.h
	faction.h
	features.h
	fixed_memory_hash_set.h
	fixed_memory_variable_hash_set.h
	global_define.h
	guild_base.h
	guilds.h
	ipc_mutex.h
	item.h
	item_base.h
	item_fieldlist.h
	languages.h
	light_source.h
	linked_list.h
	loottable.h
	mail_oplist.h
	md5.h
	memory_buffer.h
	memory_mapped_file.h
	misc.h
	misc_functions.h
	mutex.h
	mysql_request_result.h
	mysql_request_row.h
	op_codes.h
	opcode_dispatch.h
	opcodemgr.h
	packet_dump.h
	packet_dump_file.h
	packet_functions.h
	platform.h
	proc_launcher.h
	profiler.h
	ptimer.h
	queue.h
	races.h
	random.h
	rdtsc.h
	rulesys.h
	ruletypes.h
	say_link.h
	seperator.h
	serverinfo.h
	servertalk.h
	shareddb.h
	skills.h
	spdat.h
    string_util.h
	struct_strategy.h
	tcp_basic_server.h
	tcp_connection.h
	tcp_server.h
	textures.h
	timeoutmgr.h
	timer.h
	types.h
	unix.h
	useperl.h
	version.h
	worldconn.h
	xml_parser.h
	zone_numbers.h
	patches/patches.h
	patches/sod.h
#	patches/sod_itemfields.h
	patches/sod_limits.h
	patches/sod_ops.h
	patches/sod_structs.h
	patches/sof.h
#	patches/sof_itemfields.h
	patches/sof_limits.h
#	patches/sof_opcode_list.h
	patches/sof_ops.h
	patches/sof_structs.h
	patches/ss_declare.h
	patches/ss_define.h
	patches/ss_register.h
	patches/rof.h
#	patches/rof_itemfields.h
	patches/rof_limits.h
	patches/rof_ops.h
	patches/rof_structs.h
	patches/rof2.h
#	patches/rof2_itemfields.h
	patches/rof2_limits.h
	patches/rof2_ops.h
	patches/rof2_structs.h
	patches/titanium.h
#	patches/titanium_itemfields_a.h
#	patches/titanium_itemfields_b.h
	patches/titanium_limits.h
	patches/titanium_ops.h
	patches/titanium_structs.h
	patches/uf.h
#	patches/uf_itemfields.h
	patches/uf_limits.h
	patches/uf_ops.h
	patches/uf_structs.h
	SocketLib/Base64.h
	SocketLib/File.h
	SocketLib/HttpdCookies.h
	SocketLib/HttpdForm.h
	SocketLib/HttpdSocket.h
	SocketLib/HTTPSocket.h
	SocketLib/IFile.h
	SocketLib/MemFile.h
	SocketLib/Mime.h
	SocketLib/Parse.h
	SocketLib/socket_include.h
	SocketLib/Utility.h
	StackWalker/StackWalker.h
	tinyxml/tinystr.h
	tinyxml/tinyxml.h
)

SOURCE_GROUP(Patches FILES
	patches/patches.h
	patches/sod.h
#	patches/sod_itemfields.h
	patches/sod_limits.h
	patches/sod_ops.h
	patches/sod_structs.h
	patches/sof.h
#	patches/sof_itemfields.h
	patches/sof_limits.h
#	patches/sof_opcode_list.h
	patches/sof_ops.h
	patches/sof_structs.h
	patches/ss_declare.h
	patches/ss_define.h
	patches/ss_register.h
	patches/rof.h
#	patches/rof_itemfields.h
	patches/rof_limits.h
	patches/rof_ops.h
	patches/rof_structs.h
	patches/rof2.h
#	patches/rof2_itemfields.h
	patches/rof2_limits.h
	patches/rof2_ops.h
	patches/rof2_structs.h
	patches/titanium.h
#	patches/titanium_itemfields_a.h
#	patches/titanium_itemfields_b.h
	patches/titanium_limits.h
	patches/titanium_ops.h
	patches/titanium_structs.h
	patches/uf.h
#	patches/uf_itemfields.h
	patches/uf_limits.h
	patches/uf_ops.h
	patches/uf_structs.h
	patches/patches.cpp
	patches/sod.cpp
	patches/sod_limits.cpp
	patches/sof.cpp
	patches/sof_limits.cpp
	patches/rof.cpp
	patches/rof_limits.cpp
	patches/rof2.cpp
	patches/rof2_limits.cpp
	patches/titanium.cpp
	patches/titanium_limits.cpp
	patches/uf.cpp
	patches/uf_limits.cpp
)

SOURCE_GROUP(SocketLib FILES
	SocketLib/Base64.h
	SocketLib/File.h
	SocketLib/HttpdCookies.h
	SocketLib/HttpdForm.h
	SocketLib/HttpdSocket.h
	SocketLib/HTTPSocket.h
	SocketLib/IFile.h
	SocketLib/MemFile.h
	SocketLib/Mime.h
	SocketLib/Parse.h
	SocketLib/socket_include.h
	SocketLib/Utility.h
	SocketLib/Base64.cpp
	SocketLib/File.cpp
	SocketLib/HttpdCookies.cpp
	SocketLib/HttpdForm.cpp
	SocketLib/HttpdSocket.cpp
	SocketLib/HTTPSocket.cpp
	SocketLib/MemFile.cpp
	SocketLib/Mime.cpp
	SocketLib/Parse.cpp
	SocketLib/socket_include.cpp
	SocketLib/Utility.cpp
)

SOURCE_GROUP(StackWalker FILES
	StackWalker/StackWalker.h
	StackWalker/StackWalker.cpp
)

SOURCE_GROUP(TinyXML FILES
	tinyxml/tinystr.h
	tinyxml/tinyxml.h
	tinyxml/tinystr.cpp
	tinyxml/tinyxml.cpp
	tinyxml/tinyxmlerror.cpp
	tinyxml/tinyxmlparser.cpp
)

INCLUDE_DIRECTORIES(Patches SocketLib StackWalker TinyXML)

ADD_LIBRARY(common ${common_sources} ${common_headers})

IF(UNIX)
	ADD_DEFINITIONS(-fPIC)
	SET_SOURCE_FILES_PROPERTIES("SocketLib/Mime.cpp" PROPERTY COMPILE_FLAGS -Wno-unused-result)
	SET_SOURCE_FILES_PROPERTIES("patches/sod.cpp" "patches/sof.cpp" "patches/rof.cpp"  "patches/rof2.cpp" "patches/uf.cpp" PROPERTIES COMPILE_FLAGS -O0)
ENDIF(UNIX)


SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)
