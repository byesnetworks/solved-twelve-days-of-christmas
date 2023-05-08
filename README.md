Download Link: https://assignmentchef.com/product/solved-twelve-days-of-christmas
<br>
<a href="https://www.youtube.com/playlist?list=PLhOuww6rJJNNZEMX12PE1OvSKy02UQoB4" rel="nofollow">https://www.youtube.com/playlist?list=PLhOuww6rJJNNZEMX12PE1OvSKy02UQoB4</a>

Write a program that will generate the verse “The Twelve Days of Christmas” song:

<pre><code>$ ./twelve_days.py | tailTen lords a leaping,Nine ladies dancing,Eight maids a milking,Seven swans a swimming,Six geese a laying,Five gold rings,Four calling birds,Three French hens,Two turtle doves,And a partridge in a pear tree.</code></pre>

The program should accept a <code>-n</code> or <code>--number</code> (default 12) to control the number of verses that are generated:

<pre><code>$ ./twelve_days.py -n 2On the first day of Christmas,My true love gave to me,A partridge in a pear tree.On the second day of Christmas,My true love gave to me,Two turtle doves,And a partridge in a pear tree.</code></pre>

A number outside the range 1-12 should be rejected:

<pre><code>$ ./twelve_days.py -n 21usage: twelve_days.py [-h] [-n days] [-o FILE]twelve_days.py: error: --num "21" must be between 1 and 12</code></pre>

If the <code>-o</code> or <code>--outfile</code> argument is present, the output should be printed to the named file and no output should appear on the command line:

<pre><code>$ ./twelve_days.py -o out.txt</code></pre>

There should now be an <code>out.txt</code> file with the output:

<pre><code>$ wc -l out.txt     113 out.txt</code></pre>

The program should respond to <code>-h</code> and <code>--help</code> with a usage:

<pre><code>$ ./twelve_days.py -husage: twelve_days.py [-h] [-n days] [-o FILE]Twelve Days of Christmasoptional arguments:  -h, --help            show this help message and exit  -n days, --num days   Number of days to sing (default: 12)  -o FILE, --outfile FILE                        Outfile (default: &lt;_io.TextIOWrapper name='&lt;stdout&gt;'                        mode='w' encoding='utf-8'&gt;)</code></pre>

<pre><code>$ make testpytest -xv test.py============================= test session starts ==============================...collected 7 itemstest.py::test_exists PASSED                                              [ 14%]test.py::test_usage PASSED                                               [ 28%]test.py::test_bad_num PASSED                                             [ 42%]test.py::test_one PASSED                                                 [ 57%]test.py::test_two PASSED                                                 [ 71%]test.py::test_all_stdout PASSED                                          [ 85%]test.py::test_all PASSED                                                 [100%]============================== 7 passed in 1.92s ===============================</code></pre>