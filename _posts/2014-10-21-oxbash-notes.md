---
layout: post
title:  "Some notes on codes I use for theoretical nuclear physics."
date:   2014-10-21 11:04:45
description: Oxbash, WSAW, FOLD, DWHI, oh my!
categories:
- blog
---

## Oxbash and NuShellX
Oxbash and NuShellX are nuclear shell model codes written and maintained by B. Alex Brown (NSCL).

Booting NuShellX on a linus distro.
{% highlight bash %}
$ cd aaa/
$ source bash_profile_nushell
$ dens / shell / ... etc
{% endhighlight %}

Calculate nuclear densities with NuShellX (should be identical in Oxbash)--an excerpt from Mike Scott's manual:
{% highlight bash %}
dens         #start the density calculation
az           #choose nucleus
28,14        #A,Z nucleus
cp           #choose potential
sk20         #skyrme potential for masses 16O to 208Pb
gd           #calculate groundstate densities
wr           #write densitie
,,,,si28     #ouput densities to file si28.rho
st           #end calculation
{% endhighlight %}



A note on DWHI:
Sometimes the Optical Model that is used does is parameterized in the $r_c A^{\frac{1}{3}}$ manner instead of $r_c (A_t^{\frac{1}{3}} + A_p^{\frac{1}{3}})$ in which case an effective coulomb radius $r_c$ must be defined to take this into account in the DWHI input file.

The Q-value used in DWHI is defined as $Q = Q_p - Q_t$ with $Q_i = Q_i^{gs} - E_i^x$ where i is p or t, the parent or target respectively.
{% highlight bash %}
{% endhighlight %}
{% highlight bash %}
{% endhighlight %}
{% highlight bash %}
{% endhighlight %}
