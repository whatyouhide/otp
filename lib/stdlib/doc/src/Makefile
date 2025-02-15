#
# %CopyrightBegin%
#
# Copyright Ericsson AB 1997-2022. All Rights Reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# %CopyrightEnd%
#
include $(ERL_TOP)/make/target.mk
include $(ERL_TOP)/make/$(TARGET)/otp.mk

# ----------------------------------------------------
# Application version
# ----------------------------------------------------
include ../../vsn.mk
VSN=$(STDLIB_VSN)
APPLICATION=stdlib

# ----------------------------------------------------
# Target Specs
# ----------------------------------------------------
XML_APPLICATION_FILES = ref_man.xml

XML_REF3_FILES = \
	argparse.xml \
	array.xml \
	base64.xml \
	beam_lib.xml \
	binary.xml \
	c.xml \
	calendar.xml \
	dets.xml \
	dict.xml \
	digraph.xml \
	digraph_utils.xml \
	edlin_expand.xml \
	epp.xml \
	erl_anno.xml \
	erl_error.xmlsrc \
	erl_eval.xml \
	erl_expand_records.xml \
	erl_features.xml \
	erl_id_trans.xml \
	erl_internal.xml \
	erl_lint.xml \
	erl_parse.xml \
	erl_pp.xml \
	erl_scan.xml \
	erl_tar.xml \
	ets.xml \
	file_sorter.xml \
	filelib.xml \
	filename.xml \
	gb_sets.xml \
	gb_trees.xml \
	gen_event.xml \
	gen_fsm.xml \
	gen_server.xml \
	gen_statem.xml \
	io.xml \
	io_lib.xml \
	lists.xml \
	log_mf_h.xml \
	maps.xml \
	math.xml \
	ms_transform.xml \
	orddict.xml \
	ordsets.xml \
	peer.xml \
	pool.xml \
	proc_lib.xml \
	proplists.xml \
	qlc.xml \
	queue.xml \
	rand.xml \
	random.xml \
	re.xml \
	sets.xml \
	shell.xml \
	shell_default.xml \
	shell_docs.xml \
	slave.xml \
	sofs.xml \
	string.xml \
	supervisor.xml \
	supervisor_bridge.xml \
	sys.xml \
	timer.xml \
	unicode.xml \
	uri_string.xml \
	win32reg.xml \
	zip.xml

XML_REF6_FILES = stdlib_app.xml

XML_PART_FILES = part.xml
XML_CHAPTER_FILES = introduction.xml io_protocol.xml unicode_usage.xml \
	uri_string_usage.xml notes.xml assert_hrl.xml

BOOK_FILES = book.xml

XML_FILES = \
	$(BOOK_FILES) $(XML_CHAPTER_FILES) \
	$(XML_PART_FILES) $(XML_REF3_FILES) $(XML_REF6_FILES) $(XML_APPLICATION_FILES)

TOP_SPECS_FILE = specs.xml

$(SPECDIR)/specs_erl_id_trans.xml:
	$(gen_verbose)escript $(SPECS_EXTRACTOR) $(SPECS_FLAGS) \
		-o$(dir $@) -module erl_id_trans

NO_CHUNKS = erl_id_trans.xml

include $(ERL_TOP)/make/doc.mk
