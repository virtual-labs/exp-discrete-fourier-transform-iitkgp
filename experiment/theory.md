## Theory

                        
<p class="heading-content">The discrete-time Fourier transform (DTFT) of a sequence is a continuous function of &omega;, and 
repeats with period 2&pi; 
In practice we usually want to obtain the Fourier components using digital computation, and can only evaluate them for
a discrete set of frequencies. The discrete Fourier transform (DFT) provides a means for achieving this .</p>
<p class="heading-content"> The DFT is itself a sequence, and it corresponds roughly to samples, equally spaced in frequency,
of the Fourier transform of the signal. The discrete Fourier transform of a length N signal x[n], n = 0, 1... N - 1 is given by
  
$$x[k]=\sum_{n=0}^{n-1}x[n]e^{-j(2 \frac{\pi}{N})kn}|$$

<p class="heading-content">This is the analysis equation. The corresponding inverse equation is </p>

$$x[n]=\frac{1}{N} \sum_{n=0}^{n-1}x[k]e^{j(2 \frac{\pi}{N})kn}|$$

<p>With this notation the DFT analysis-inverse pair becomes</p>

$$W_N=e^{-j(2\frac{\pi}{N})}|$$

<p>With this notation the DFT analysis-inverse pair becomes</p>

$$x[k]=\sum_{n=0}^{n-1}x[n]w_n^{kn}|$$

$$x[n]=\frac{1}{N} \sum_{n=0}^{n-1}x[k]w_n^-{kn}|$$

<p class="heading-content">An important property of the DFT is that it is cyclic, with period N, both in the discrete-time 
and discrete-frequency domains. For example, for any integer r</p>

$$X[K+rN]=\sum_{n=0}^{n-1}x[n]w_N^{K+rN}.n=\sum_{n=0}^{n-1}W_N^{Kn}({W_N^N})^{rn}|$$

$$=\sum_{n=0}^{n-1}x[n]W_N^{Kn}=X[K],|$$

Since,

$$W N^N=e^{-j(2\frac{\pi}{N})N}=e^{-j2\pi}=1|$$

Similarly, it is easy to show that x[n + rN] = x[n], implying periodicity 
of the inverse equation. This is important - even though the DFT only depends on samples in the 
interval 0 to N - 1, it is implicitly assumed that the signals repeat with period N in both the time and
frequency domains.</p>
<p style="text-align:">To this end, it is sometimes useful to define the periodic extension of the signal X[n] to be
  
$$x[n]=x[n \ mod \ N]=x[((n))N]|$$

<p style="text-align:">Here n mod N and((n))N are taken to mean n modulo N, which has the value of the remainder 
after n is divided by N.Alternatively, if n is written in the form n = kN + l for 0 &leq; l &leq; N, then</p>
<p>n mod N = ((n))N = l </p><center><img src="images/pic-1.png" style="height:50%;width:50%;" align="center" /></center>
<p style="text-align:">Similarly, the periodic extension of X[k] is defined to be</p>

$$X[k]=X[k \ mod \ N]=X[((K))n]|$$

<p style="text-align:">It is sometimes better to reason in terms of these periodic extensions when dealing with the DFT. 
Specifically, if X[k] is the DFT of x[n], then the inverse DFT of X[k] is [n]. The signals x[n] and [n] are identical 
over the interval 0 to N-1,but may differ outside of this range. Similar statements can be made regarding the 
transform X[k].</p>
</div>


 <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3.2.2/es5/tex-mml-chtml.js"></script>    
 
