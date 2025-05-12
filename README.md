# cs214-project-2-solved
**TO GET THIS SOLUTION VISIT:** [CS214 Project 2 Solved](https://www.ankitcodinghub.com/product/cs214-project-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;90743&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS214 Project 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<h1>1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Summary</h1>
Write a program that analyzes a set of files and reports their similarity using the method described below. Your program will use two or more threads to read directory entries and analyze the word frequencies of text files, then compute the Jensen-Shannon distance between the word frequencies of pairs of files.

<h1>2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; User interface</h1>
Your program will be given the names of one or more files and directories, and up to four optional arguments specifying program parameters. The file names and directories are used to determine the set of files to analyze. File names given as arguments are added directly to the set of files. For each directory, your program will add any files whose names have a particular suffix to the set, and recursively traverse any subdirectories.

For each (unordered) pair of files in the analysis set, your program will output the Jensen-Shannon distance between their word frequencies. For example:

$ ls bar baz.txt quux spam/ $ ls bar/spam eggs.txt bacon.c $ ./compare foo bar

0.03000 foo bar/baz.txt

0.12000 foo bar/spam/eggs.txt

0.80000 bar/baz.txt bar/spam/eggs.txt

Table 1: Parameters specified by options

<table width="342">
<tbody>
<tr>
<td width="126">Parameter</td>
<td width="57">Option</td>
<td width="109">Argument Type</td>
<td width="51">Default</td>
</tr>
<tr>
<td width="126">Directory threads</td>
<td width="57">-d<em>N</em></td>
<td width="109">Positive integer</td>
<td width="51">1</td>
</tr>
<tr>
<td width="126">File threads</td>
<td width="57">-f<em>N</em></td>
<td width="109">Positive integer</td>
<td width="51">1</td>
</tr>
<tr>
<td width="126">Analysis threads</td>
<td width="57">-a<em>N</em></td>
<td width="109">Positive integer</td>
<td width="51">1</td>
</tr>
<tr>
<td width="126">File name suffix</td>
<td width="57">-s<em>S</em></td>
<td width="109">String</td>
<td width="51">“.txt”</td>
</tr>
</tbody>
</table>
In this example, the arguments are foo (a file) and bar (a directory). One file in bar matches the default suffix (“.txt”) and is added to the file set. The subdirectory bar/spam is also traversed, and its files that end with the suffix are added. This results in the file set foo, bar/baz.txt, and bar/spam/eggs.txt. (Note that foo does not need to end with the suffix, because it was explicitly given by the user.)

For each pair of files in the file set, the program outputs the JSD and the (path) names of the files being compared. Comparisons are printed in decreasing order of combined word count (that is, the total number of words in both files). Note that pairs are unordered, so the output will include comparisons of foo and bar/baz.txt or bar/baz.txt and foo, but not both.

<h2>2.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Regular arguments</h2>
Your program will take one or more regular arguments, which must be the name (or a path to) a file or directory.

Each file name is added to the set of files to examine.

Each directory name is added to the set of directories to traverse. For each directory in the set, your program will read through its entries. Any file whose name ends with the file name suffix is added to the set of files to examine. Any directory is added to the set of directories to traverse. Entries that are not directories and that do not end with the specified suffix are ignored.

Exception&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Any entry in a directory whose name begins with a period is ignored.

<h2>2.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Optional arguments</h2>
Your program takes up to four optional arguments, which are used to set program parameters. For simplicity, we will assume any argument that begins with a dash (-) specifies an option. The first character following the dash indicates which parameter is being specified, and the remainder of the argument gives the value for that parameter. Table 1 gives the syntax for the four options, and the default values for the parameters of the options are omitted.

For simplicity, you may require all optional arguments to occur before the regular arguments in the argument list, or allow them to be intermixed. You may require that an optional argument occur at most once, or allow later arguments to override earlier ones.

You must allow options to be given in any order.

Your program must detect any invalid optional arguments and halt with an error message. Possible errors are an invalid option (e.g., -x), or an invalid or missing argument (e.g., -f0 or -d).

Note&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The file name suffix may be an empty string, which would be indicated by the option -s.

Table 2: Word frequency distribution example

Text: I can’t understand thieves’ cant. Word Occurrences Frequency

cant&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2 0.4 i&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1 0.2 thieves 1 0.2 understand 1 0.2

<h1>3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Operation</h1>
Your program will compute the word frequency distribution for each file in a set of files. For each pair of files in this set, it will compute the Jensen-Shannon distance (JSD) between the distributions for those files

<h2>3.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Word frequency distribution (WFD)</h2>
The <em>frequency </em>of a word is the number of times the word appears divided by the total number of words. For example, in the text “spam eggs bacon spam”, the frequency of “spam” is 0.5, and the frequencies of “eggs” and “bacon” are both 0.25.

The <em>word frequency distribution </em>(WFD) for a file is a list of every word that occurs at least once in the file, along with its frequency. Ignoring rounding errors, the frequencies for all the words will add up to 1.

Tokenizing To compute the WFD for a file, your program must read the file and determine what words it contains. For this project, we define a word to be a sequence of word characters, where word characters include letters, numbers, and the dash (hyphen). Words are separated by whitespace characters. Other characters, such as punctuation, are ignored.

To compute the WFD, keep a list of every word found in the file and its count. Each time a word is encountered, look for it in the list and increment its count or add it with count 1. Once every word has been read, divide the count for each word by the total number of words.

Words are case-insensitive. The simplest way to handle this is to convert words to upper- or lowercase while reading.

Table 2 shows the WFD for a short example file. Note that “I” has been converted to lowercase and that “can’t” and “cant” are treated as the same word (because the apostrophe is ignored).

Data structure&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; You will need to maintain a list of mappings between words and counts (later frequencies). You are free to choose any data structure, but you may find a linked list to be a good balance of efficiency and simplicity. It is recommended that you choose a structure that allows you to iterate through the words in lexicographic order.

Your program must not assume a maximum word length. Instead, word storage will be dynamically allocated.

(b) <em>F</em>

(a) <em>F</em><sub>1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </sub>(c) <em>F</em>

hi&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; hi&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.5

hi&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.5

out 0.25&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; out 0.125

there&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 0.5

there 0.25&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; there 0.375

Figure 1: Computing the JSD for two files

<h2>3.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Jensen-Shannon distance (JSD)</h2>
The Jensen-Shannon distance (JSD) is a symmetric measure of the similarity of two discrete distributions. We will write <em>F<sub>i</sub></em>(<em>x</em>) to mean the frequency of word <em>x </em>in file <em>i</em>. Note that <em>F<sub>i</sub></em>(<em>x</em>) = 0 if <em>x </em>does not appear in file <em>i</em>.

We define the <em>mean frequency </em>for a word to be the average of its frequencies in the two files.

(1)

Next we compute the Kullbeck-Leibler Divergence (KLD) between each file and the mean.

(2)

This is computed by adding the frequencies of each word in the file scaled by the base-2 logarithm of the frequency divided by the mean frequency for that word. The result will be a value between 0 and 1.

Finally, the JSD is the square root of the mean KLD between the files and the mean distribution.

(3)

Figure 1 shows the steps to compute the JSD for two files containing “hi there hi there” and “hi hi out there”, respectively. Figures 1a and 1b give the WFD for the files, and fig. 1c shows their mean WFD.

Figure 2: Organization of the collection phase

Implementation&nbsp;&nbsp;&nbsp; If you have chosen a WFD structure that allows you to iterate through the word lists in alphabetical order, it is simple to compute the JSD using simultaneous iteration for both lists. Keep a running total of the KLD for both files. If you encounter a word appearing in both lists, compute the mean frequency and then add the scaled frequencies to both running totals. If word appears in one list but not the other, treat its frequency as 0 in the file where it does not appear. Once all words have been considered, compute the JSD.

<h1>4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Program organization</h1>
Your program will operate in two phases. The collection phase recursively traverses directories and reads files to find the WFD (see section 3.1) for each requested file. The analysis phase computes the JSD (see section 3.2) for each pair of requested files.

Both phases are multithreaded and use synchronized data structures to perform their tasks.

<h2>4.1&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Collection phase</h2>
The collection phase uses two groups of threads to find the WFD for each file in a set of requested files. It uses two synchronized queues to keep track of the directories and that need to be examined.

Figure 2 shows the organization of the collection phase. The components of the collection phase are:

Directory queue Contains a list of directories that have been seen but not yet traversed. This will be a synchronized queue (or stack) that must be unbounded.

File queue Contains a list of files that have been seen, but not yet examined. This will be a synchronized queue (or stack) that may be bounded or unbounded.

WFD repository Once a file has been examined, its name, count of tokens, and WFD is added to this structure. This may be any synchronized data structure. See section 3.1 for details of how to represent the WFD.

Main thread The main thread creates the queues and repository. For each regular argument, it determines whether it is a file or directory and adds it to the appropriate queue. Based on the program parameters (see section 2.2), it starts the requested number of file and directory threads. Once all the file threads have completed, it proceeds to the analysis phase.

Directory thread Each directory thread is a loop that repeatedly dequeues a directory name from the directory queue and reads through its directory listing. Each directory entry is added to the directory queue. Each non-directory entry that ends with the file name suffix is added to the file queue.

A directory thread will finish when the queue is empty and all other directory threads have finished or are waiting to dequeue.

File threads Each file thread is a loop that repeatedly dequeues a file name from the file queue, tokenizes the file and computes its WFD, and adds the data for that file to the WFD repository. A file thread will finish once the queue is empty and all directory threads have finished.

Note that the working directory is shared by all threads, so the directory threads will not be able to use chdir(). Instead, they will need to concatenate the directory name and the file or subdirectory name to get a path. Assume that all file and directory names given as arguments are relative to the working directory (that is, you do not need to modify or examine them).

We will discuss synchronized queues in class, but you will need to customize them somewhat to work here. When the directory queue is empty, you will need to keep track of the number of threads waiting to dequeue. Once the last thread tries to dequeue, you can be certain that no new directories will be found. At this point, you can set a flag indicating that traversal has ended and wake up the directory threads so that they can terminate. Similarly, file threads should terminate if the file queue is empty and traversal has ended (meaning no more files will be added).

Exercise&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Why is it safe for the file queue to be bounded, but not the directory queue?

Error conditions If any file or directory cannot be opened, report an error and continue processing. It is sufficient to call perror() with the name of the file or directory to report the error. You may also exit with status EXIT_FAILURE when the program completes.

For unexpected errors, such as failure to create threads or lock and unlock mutexes, your program may report an error and terminate immediately.

<h2>4.2&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Analysis phase</h2>
The analysis phase computes the JSD (see section 3.2) and combined word count for each pair of files listed in the WFD repository (see section 4.1). It divides this work among one or more analysis threads, as indicated by the analysis threads option (see section 2.2).

Each analysis thread is given a portion of the file pairs and computes the JSD for each pair. Once all comparisons have been made, the main thread will sort the list of comparisons in descending order of combined word count and then print the results.

Data structure&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; For each comparison, we will need the names of the files being compared, the combined word count, and the JSD. If there are <em>n </em>files, there will be &nbsp;comparisons, so it is feasible to create an array of structs, have each thread write to non-overlapping portions of the array, and finally sort the array using qsort().

Division of labor The simplest way to divide the work among the analysis threads is to give each thread a roughly-equal portion of the comparison set to compute. If there are 30 files and 5 analysis threads, then each thread will compute 93 of the 465 comparisons. (Naturally, we must be able ot handle cases where the number of comparisons does not divide evenly.)

While this method divides up the number of tasks (roughly) equally, it assumes that all comparisons will take equally long to compute. Another method to divide the work is to keep track of which comparison needs to be computed next and have each analysis thread take the next comparison needed. This will reduce the possibility that some threads will finish early while other threads have significant amounts of work left to do.

Error conditions&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If the collection phase found fewer than two files, report an error and exit.

Any numeric errors occurring in this phase (e.g., word frequencies outside the range [0,1]) indicate problems in the collection phase. You may choose to check these using assert().

<h1>5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Advice</h1>
Don’t panic! While this assignment has many components, the components themselves are relatively simple. If you begin before we have gone over synchronized queues in class, you can still design your data structures and begin work on the analysis phase.

While use of the C file IO functions (e.g., fopen()) is permitted for this assignment, you will not find them any easier or more convenient than using open() and read(). Using getline() will just add complexity to your program for no real benefit.

Recall that printf() and fprintf() are synchronized, meaning they can be safely used in different threads. During debugging, you may find it helpful to print log messages describing what actions your threads are doing. Use the DEBUG macro trick to easily enable or disable these messages as needed.

Always check for errors. Functions like malloc() or pthread_mutex_lock() never fail under normal circumstances, which means you definitely want to be informed if they do fail—it may indicate a logic error in your program! If writing the error checks becomes tedious, define a macro to write them for you. How best to handle error conditions is a design choice, but the usual thing to do when something “impossible” happens is to report an error and terminate the program.

That being said, checking printf() for an error result is probably overkill.
