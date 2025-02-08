# Document Section Syntax

document = section_body { section }

section = section_head section_body

section_head_begin = DEFAULT_SECTION_HEAD_BEGIN
section_head_end = DEFAULT_SECTION_HEAD_END

section_head = section_head_begin [..]+ section_head_end

section_body = { attribute | assignment | block_comment | multi_line }

attribute = identifier ':' represented_value [ line_comment ]

assignment = identifier '=' represented_value [ line_comment ]

block_comment = indent <capture:'#'{5,}> newline { indent block_comment_line newline } indent <capture> newline

multi_line = [^#\n\\]* line_comment?  {  '\\\n' [^#\n\\]* line_comment? } '\n'

line_comment = '#' [^\n\\]+ ?( '\\'? '\n' )


DEFAULT_SECTION_HEAD_BEGIN = '\n\n[['
DEFAULT_SECTION_HEAD_END = ']]\n'
