# website_corrections
Corrections I'd like to make to other peoples' websites or content.

By Gabriel Staples

**If you use any of my corrections, please cite me with my name and URL. You can link to my GitHub page if you like, or to me on LinkedIn, or (preferred) both. Example citation:**

> Gabriel Staples, Engineer and Senior Embedded Software Developer, GitHub: https://github.com/ElectricRCAircraftGuy, LinkedIn: https://www.linkedin.com/in/gabriel-staples

_If you are a website or company owner, you or your engineers can email me or call me if you have any questions or would like to discuss my corrections. I should have included my phone and email in any feedback I sent you._


# Table of Contents
<details>
<summary><b>(click to expand)</b></summary>
<!-- MarkdownTOC -->

1. [Corrections](#corrections)
    1. [20220213-1434hrs: arrow.com Nyquist Frequency](#20220213-1434hrs-arrowcom-nyquist-frequency)

<!-- /MarkdownTOC -->
</details>


<a id="corrections"></a>
# Corrections

[NEWEST on TOP]:

<a id="20220213-1434hrs-arrowcom-nyquist-frequency"></a>
## 20220213-1434hrs: arrow.com Nyquist Frequency

Feedback sent to: https://www.arrow.com/en/support/contact-support/contact-arrow --> I chose "Report a Website Issue"

Fundamental engineering errors regarding the Nyquist Frequency exist on this article: https://www.arrow.com/en/research-and-events/articles/engineering-resource-basics-of-analog-to-digital-converter

It states, for instance (emphasis added): 

> According to the [Nyquist] theorem, the sampling rate/frequency needs to be at least twice as much as the highest frequency in the signal **to recreate the original analog signal**. 

This is incorrect. 2x the sampled frequency is NOT enough to "recreate" the original signal, rather, it is simply enough to avoid aliasing and correctly **detect the frequency of** the original signal. I would modify the article to say: 

> According to the Nyquist theorem, the sampling rate/frequency needs to be at least twice as much as the highest frequency in the signal **in order to detect the frequency of the original signal.**

And: 

> "A good rule of thumb is that the sampling frequency should be 5x to 10x as high as the highest frequency of a signal you'd like to accurately recreate or plot. Sampling rates between 2x and \~5x of the signal being sampled are higher than the Nyquist frequency and therefore able to correctly detect the sampled signal's frequency without aliasing, but will suffer from higher distortion of the original signal than sample rates >= 5x the sampled signal.
