= Reoresented Values

Reoresented values is a string which represents a value, these can be standard (listed below), custom or a set either.

== Standard Reoresented Values

Boolish = icase( 'True' | 'False' | '0' | '1' )

Integral = (:nows=1) [+-] unsigned_integer

unsigned_integer = implied_dec_uint | hexdec_uint | dec_uint | oct_uint | bin_uint

implied_dec_uint = \d+

hexdec_uint = (:nows=1) i'0x' i[0..9a..f]+

dec_uint = (:nows=1) i'0d' [0..9]+

oct_uint = (:nows=1) i'0d' [0..7]+

bin_uint = (:nows=1) i'0b' [01]+

float = (:nows=1) [+-] ( implied_dec_uint ( '.' implied_dec_uint? )? | '.' implied_dec_uint ) [ i'e' [+-]? implied_dec_uint

comma_seperated_values = ...

tab_seperated_values = ...

fixed_width_values = ...
