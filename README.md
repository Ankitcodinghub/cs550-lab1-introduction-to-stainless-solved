# cs550-lab1-introduction-to-stainless-solved
**TO GET THIS SOLUTION VISIT:** [CS550 Lab1-Introduction to stainless Solved](https://www.ankitcodinghub.com/product/cs550-lab-1-introduction-to-stainless-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;118165&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS550 Lab1-Introduction to stainless Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
            5/5 - (2 votes)    </div>
    </div>
In this first lab, you will use stainless to verify a short scala file.

Installation

Java Development Kit

In order to run stainless, as well as the programs you will verify, you will need Java 17.

You can check your Java version using “`shell

On some Linux distributions, a command exists to change your “active” JDK if multiple ones are installed on your machine. Examples include: Debian-based: update-alternatives -config java; – ArchLinux-based: archlinux-java set java-17-openjdk.

Scala

You will also need a way to compile scala programs. We will provide files meant to be used with scala-cli while working with stainless, but you will also need sbt when working with LISA in future labs. As such, we recommend that you install coursier, which will come with the scala compiler, scala-cli and sbt. Install instructions can be found here.

You will need to add coursier’s bin directory to your path. The bin directory’s path (typically ~/.local/share/coursier/bin on Linux) will be printed in the terminal near the end of the installation.

You can test your installation with “`shell

Stainless

Download the latest stainless release (0.9.8.1) from its repository (download the file named stainless-dotty-standalone-0.9.8.1&lt;your_os&gt;.zip). On Windows, it is recommended to run the linux version on top of the Windows Subsystem for Linux (WSL).

The release is an archive containing, among other things, a script called stainless, that you should make available on your path. Detailed instructions can be found in this video.

On Mac, you should also make the z3 executable (which is part of the stainless release) available on your path.

Tutorial

To have a bit more intuition for how to do induction proofs, consider the following arithmetic example that verifies in Stainless:

“`scala def sumTo(n: BigInt): BigInt = require(0 &lt;= n) if n == 0 then BigInt(0) else n + sumTo(n-1)

def sumToIsCorrect(n: BigInt): Unit = { require(0 &lt;= n) if n == 0 then () else sumToIsCorrect(n-1) } ensuring { _ =&gt; sumTo(n) == n*(n+1)/2 }

“`

Whereas we could have modified sumTo to state the postcondition res == n*(n+1)/2, here we decided to leave sumTo as is. To ensure that Stainless proves property by induction, we repeat the recursive structure of sumTo inside the body of sumToIsCorrect. The result is the same induction schema as if we added apostcondition to sumTo. Simple cases of such induction can be simulated by adding induct annotation to the original method, but writing explicitly induction schema as we did here is more general.

Lab

Getting the source

To start working on this lab, you can either clone this entire repository, or download the present directory alone from Gitlab (there should be a button for this on the top right of the web interface).

The sublist relation

The file Sublist.scala (in this directory) defines a relation sublist on lists, also noted $sqsubseteq$, which holds when all the elements of the first list appear in the second in the same order. Some examples: math ewcommand{slist}[0]{sqsubseteq} ewcommand{seq}

[1]{langle#1 angle} egin{align*} seq{0,2} &amp;slist seq{0,1,2} \ seq{0,0,2} &amp; otslist seq{0, 2}\

seq{1,0} &amp; otslist seq{0,0,1} \ seq{10,5,25} &amp;slist seq{70,10,11,8,5,25,22} end{align*}

The file includes a main function which checks the examples above “`shell

scala-cli run Sublist.scala &lt;0,2&gt; âŠ‘ &lt;0,1,2&gt; = true &lt;0,0,2&gt; âŠ‘ &lt;0,2&gt; = false &lt;1,0&gt; âŠ‘ &lt;0,0,1&gt; = false &lt;10,5,25&gt; âŠ‘ &lt;70,10,11,8,5,25,22&gt; = true &lt;25,11,53,38&gt; âŠ‘ &lt;15,25,11,8,53,22,38&gt; = true “`

Goal of the lab

The List data-structure as well as the sublist relation are already implemented; your job is now to prove some properties on the latter, such as reflexivity, transitivity, and antisymmetry. These properties are stated in the form of functions which “do nothing”: they return Unit and have no effects. You have to fill these functions with a proof of their statement.

As an example, the first property to prove is reflexivity. It is stated as follows scala def reflexivity[T](l: List[T]): Unit = { /*

TODO: Prove me */ }.ensuring(_ =&gt; sublist(l, l) ) which should be understood mathematically as math ewcommand{slist}

[0]{sqsubseteq} ewcommand{seq}[1]{langle#1 angle} orall l, l slist l Another example: transitivity scala def transitivity[T](l1: List[T], l2: List[T], l3: List[T]): Unit = { require(sublist(l1, l2) &amp;&amp; sublist(l2, l3)) /* TODO: Prove me */ }.ensuring(_ =&gt; sublist(l1, l3) ) which should be interpreted as math ewcommand{slist}[0] {sqsubseteq} ewcommand{seq}[1]{langle#1 angle} orall l_1, l_2, l_3, l_1 slist l_2 land l_2 slist l_3 implies l_1 slist l_3

The file contains eleven properties on sublist that you have to prove.

To check your proofs, use “`shell

On Linux and WSL

stainless Sublist.scala

On Mac

stainless –solvers=smt-z3 Sublist.scala “`

The provided configuration file (stainless.conf) will automatically set the SMT solver’s timeout to 2 seconds. You can override this while experimenting with your proofs by either changing the configuration file or using the command line, by adding e.g. –timeout=5 to set the timeout to 5 seconds. You can also add –watch for stainless to automatically run on file save: “`shell stainless –timeout=5 –watch Sublist.scala “`

You are not allowed to change the definition of sublist or the statement (parameters/return types, function name, requirements, conclusion, …) of any of the properties. The only exception to this rule is the @induct annotation, which you are allowed to add to any parameter.

Some advice: – Try to understand how you would prove these properties with paper and pencil, and use examples to gain intuition; – Induction is the main proof method in many cases; see the videos on how to write inductive proofs; – Prove lemmas in order: earlier lemmas (and their structure) will help you with subsequent lemmas; – Even though it is not necessary, you can define new lemmas if it helps (but you then have to prove them correct as well ðŸ˜Š); – Regarding the four lemmas about concatenation: two very similar lemmas can have vastly different proofs (in both size and difficulty â€“ can you tell why ?).

Submission

Once you’ve completed all proofs, you can submit your Sublist.scala file on Moodle.

You also need to pick your groups (min 2, max 3) for the labs and projects on Moodle.

Only one member of each group should submit a solution.
