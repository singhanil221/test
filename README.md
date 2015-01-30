# test
Program to check that the the input string 2 is the anagram of input string 1
/**
 * Program to check that the the input string 2 is the anagram of input string 1
 */
 
/**
 * @var str1 is input string 1
 * @var str2 is input string 2
 */
$str1 = "Upshot Tech";
$str2 = "Hutches Top";

/**
 * sorting the input string 1 and 2 by sortString method
 */
$str2Sorted = sortString(strtolower($str2));

$str1Sorted = sortString(strtolower($str1));

/**
 * Checking if both the sorting strings are equal or not
 */
if ($str1Sorted == $str2Sorted)
{
   echo $str2.' is anagram of input sting '.$str1;
}
else
{
	echo $str2.' is not anagram of input sting '.$str1;
}	

/**
 * Methods return the sorting strings
 */
function sortString($s)
{
    $chars = array();
    $length = strlen($s);
    for ($i=0;$i<$length;$i++)
    {
       $chars[] = $s[$i];
    }
    sort($chars);

    return implode("",$chars);
}
