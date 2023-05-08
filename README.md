Download Link: https://assignmentchef.com/product/solved-swe3021-project-4-counting-sort-using-cuda
<br>



<h1>1        Counting Sort</h1>

In this assignment, you will implement a parallel counting sort algorithm in CUDA. Counting sort is a non-comparative sorting algorithm, which can be easily implemented in C function as follows.

void counting_sort(int arr[], int size, int MAX)

{ int histogram[MAX];

for (i=0; i&lt;MAX; i++){ histogram[i] = 0;

}

for (i=0; i&lt;size; i++){ histogram[arr[i]]++;

}

for (i=0;i&lt;MAX;i++){ for (j=0;j&lt;histogram[i];j++){ cout &lt;&lt; i &lt;&lt; ” “;

}

}

}

Skeleton codes are located in /home/swe3021/project4. Note that you need to implement all CUDA functions in counting_sort.cu file since it is the only file that you will submit. Driver files will be changed to measure the performance of your code with different inputs. You are free to change the driver code for testing purpose.

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="5f26302a2d363b1f2b362b3e316e">[email protected]</a>:~$ cp -r ~swe3021/project4 .

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="443d2b31362d2004302d30252a75">[email protected]</a>:~$ cd project4 <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="126b7d67607b7652667b66737c23">[email protected]</a>:~/project4$ ls counting_sort.cu driver1.cpp Makefile

In order to compile, simply run make command as follows. <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="770e1802051e1337031e03161946">[email protected]</a>$ make

<h1>2        Grading</h1>

Again, your project score will be given as follows.

<ol>

 <li>If you do not submit, you will get 0 point.</li>

 <li>If your code does not compile, you will get only 1 point.</li>

 <li>If your code compiles and runs CUDA kernel functions but outputs are incorrect, you will get only 2 points.</li>

</ol>

1

<ol start="4">

 <li>The remaining 8 points are the performance score, which will be prorated by the following equation.</li>

</ol>

This project will not require a significant amount of your time to implement. Note that you can even find some counting sort implementations in CUDA from github. But please do not look at those implementations. If you do, you code is likely to be similar to that and my “cheating detection program” may catch it. Again, this project is easy and I believe this will be a good practice for those who never wrote a CUDA program before.

<h1>3        How to Submit</h1>

To submit your project, you must make sure that your file is counting_sort.cu and run multicore_submit command in your project directory in swin.skku.edu server.

$ multicore_submit project4 counting_sort.cu

For any questions, please post them in Piazza so that we can share your questions and answers with other students. Please feel free to raise any issues and post any questions. Also, if you can answer other students’ questions, please don’t hesitate to post your answer. You would get some credits for posting questions and answers in Piazza.

2