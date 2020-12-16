<?php
$text = '„Собственность — обман. Никто ничем не владеет. Когда Вы умрете, все останется здесь.';
echo $text . PHP_EOL;
$text1 = mb_convert_case($text, MB_CASE_TITLE);
$count = count(preg_split('/\s+/u', $text, null, PREG_SPLIT_NO_EMPTY)) . PHP_EOL;
echo '50: ', $count;
function countAndSort($string)
{
preg_match_all("/[a-zа-я]+/ium", $string, $words);
$counts = array_count_values(array_map('ucwords', $words[0]));
$words = array_keys($counts);
array_multisort($counts, SORT_NUMERIC, SORT_DESC); //, $words, SORT_STRING
return array_map(function ($a, $b) {
return "'$a' встречается $b раз";
}, $words, $counts);
}
print_r(countAndSort($text1));
