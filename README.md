# m-eec041-project-1-solved
**TO GET THIS SOLUTION VISIT:** [M.EEC041 Project 1 Solved](https://www.ankitcodinghub.com/product/m-eec041-project-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94396&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;M.EEC041 Project 1 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 0px;">
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
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
This project consists in implementing a sequential calculator of the square root for 32-bit unsigned integer numbers. The circuit must be built as a synthesizable Verilog module implementing the logic diagram shown in figure 1. The interface of the module is:

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>module psdsqrt(
          input
          input
          input
          input
          input
</pre>
</div>
<div class="column">
<pre>clock,
reset,
start,
stop,
</pre>
</div>
<div class="column">
// master clock rising edge

// synch reset active high

// start a new square root, one clock pulse // load output register, one clock pulse

// operand, unsigned integer 32 bits

// sqrt( xin ), unsigned integer 16 bits

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>       [31:0] xin,
output reg [15:0] sqrt
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
)

</div>
</div>
<div class="layoutArea">
<div class="column">
Figure 1 – RTL diagram of the sequential square root calculator.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
2. Functional description

This circuit implements a sequential square root calculator for 32-bit integer numbers, producing the result as a 16-bit integer. The integer square root result is truncated to nearest integer not greater than the square root of xin. The function implemented by this circuit is functionally equivalent to the C code below:

<pre>              unsigned int xin, sqrtx;
              sqrtx = (int) sqrt( (double) xin);
</pre>
The algorithm builds the result iteratively from the most significant bit to the least significant bit. Iteration i decides whether the bit bi is one or zero by comparing the square of a tentative result with that bit set (signals testsqrt and sqtestsqrt==(testsqrt)2) with the input argument xin. If xin is greater than sqtestsqrt then bit bi is set to one, otherwise it is reset back to zero.

To execute a square root calculation, the input start must be set high during one clock cycle to load the input argument into the input register. Then the iterative process proceeds for 16 clock cycles. At the end of the iterative process, one additional clock is necessary with the input stop high to load the output register.

3. Implementation of the RTL code

The system must be implemented as a behavioral Verilog synthesizable module using a single clock signal for all registers, active in the positive (rising) edge and a global synchronous reset, active high. The activation of the reset signal must set all the registers to zero.

4. Verification and automation of testbench

To verify this model you must adapt the testbench given and implement a convenient verification program to verify the functionality of your code. The task execsqrt already included in the testbench implements the correct sequence of signals start and stop to perform calculation. You should improve the testbench in order to automate the verification procedure.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
5. Additional developments

5.1 Modify your module using one parameter NBITSIN to configure the number of bits for the operand xin (and consequently for the result). The external controller that sequences the activation of the start and stop signals will use the same parameter to generate the appropriate timing for those signals, as the number of clock cycles is related to the number of bit of the result. The number of bits specified for the operand xin must be even and between 4 and 64.

5.2 The iterative process implemented by this circuit truncates the integer result to the floor of the square root of xin (the nearest integer not larger than the real value of sqrt( xin ). Modify your design to include a rounding mechanism, according to the following rules and considering at most 4 bits for representing internally the fractional part of the result:

<ul>
<li> &nbsp;Round down if the fractional part of the square root is less than 0.5 (0.1000b)</li>
<li> &nbsp;Round up if the fractional part is greater or equal to 0.5625 (0.1001b)</li>
<li> &nbsp;Round to the nearest even integer if the 4-bit fractional part is equal to 0.5
(0.1000b)

Examples:

sqrt(12) = 3.4641 -&gt; round down to 3

sqrt(13) = 3.6056 -&gt; round up to 4

sqrt(1057) = 32.512 = 10000.1000… -&gt; round down to 32 sqrt(4291) = 65.506 = 100001.1000… -&gt; round up to 66

To obtain the fractional part of the result do the following:
</li>
<li> &nbsp;Input X * 2k. This is equivalent to increasing the number of bits of X by k and
concatenating k zeros at the right of X.
</li>
<li> &nbsp;Theresultcomputedbythecircuitissqrt(X*2k )=sqrt(X)*sqrt(2k ).IfXis
N bits long, the input operand has N+k bits and the result generated by the circuit has (N+k)/2 bits. Note that sqrt(2k) = 2k/2, thus k must be even in order to the division by 2k/2 being equivalent to shifting right by k/2 bits.
</li>
<li> &nbsp;Thus, the result will contain the integer part of the square root in the leftmost N/2 bits and the fractional part in the k/2 rightmost bits. These k/2 bits will decide the operation for performing the rounding process described above.
5.3 Build a sequential controller to generate the signals start and stop, according to the number of bit of the input operand specified by the parameter NBITSIN. The sequential controller must receive a single clock pulse in input run to start one calculation and generate the 3 output signals start, stop and busy, implementing the timing diagram shown in figure 2 (this is for a 16-bit output result)
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Figure 2 – Timing diagram for the sequential controller.

</div>
</div>
</div>
