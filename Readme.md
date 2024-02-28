# Chinese Grammatical Error Diagnosis
## Introduction
Unlike the English learning setting for which many learning technologies have been developed, those to support Asian language learners are relatively rare. In response, the NLPTEA (Natural Language Processing Techniques for Educational Applications) workshops were organized to provide a forum where international participants can share knowledge on the computer-assisted techniques for Asian language learning and teaching. In NLPTEA workshops, a series of shared tasks for Chinese grammatical error diagnosis was hosted (Yu et al., 2014; Lee et al., 2015b; Lee et al., 2016). The goal of these tasks is to develop NLP techniques to automatically diagnose grammatical errors in Chinese sentences written by Chinese as a foreign language learners. The grammatical errors are broadly categorized into 4 error types: word ordering, redundant, missing, and incorrect selection of linguistic components (also called PADS error types, denoting errors of Permutation, Addition, Deletion, and Selection, correspondingly). In the first edition in NLPTEA 2014 workshop, a sentence with/without one of grammatical errors is given, and the developed system should indicate whether it contains a grammatical error and further identify the error type if any error occurs. In the second edition in NLPTEA 2015 workshop, in addition to detecting whether a given sentence contains a grammatical error and identify the error type, the system should also indicate the range of occurring errors. In the third edition in NLPTEA 2016 workshop, the task is basically the same, except that a sentence may contain more than one errors and the HSK learner corpus is also included for the task.

## Summary
<table class="tg">
<thead>
  <tr>
    <th class="tg-c3ow">Shared Task</th>
    <th class="tg-0pky">NLPTEA 2014 Task<br>(Yu et al., 2014)</th>
    <th class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">NLPTEA 2015 Task</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(Lee et al., 2014)</span></th>
    <th class="tg-0pky"><span style="font-weight:400;font-style:normal;text-decoration:none">NLPTEA 2016 Task</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(Lee et al., 2014)</span></th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Examples</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal">Example 1:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Input: (sid=C1-1876-2) 對社會國家不同的影響</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Output: C1-1876-2, Missing</span><br><span style="font-weight:400;font-style:normal;text-decoration:none"> </span><br><span style="font-weight:400;font-style:normal">Example 2:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Input: (sid=A2-0775-2) 我起床很早</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Output: A2-0775-2, Disorder</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal">Example 1:</span><br><span style="font-weight:400;font-style:normal">I</span><span style="font-weight:400;font-style:normal;text-decoration:none">nput: (sid=B2-0080) 他是我的以前的室友 </span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Output: B2-0080, 4, 4, Redundant </span><br><br><span style="font-weight:400;font-style:normal">Example 2: </span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Input: (sid=B1-1193) 吳先生是修理腳踏車的拿手 </span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Output: B1-1193, 11, 12, Selection</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal">Example 1:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Input: (sid=A2-0011-1) 我聽到你找到工作。恭喜恭喜！</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Output: A2-0011-1, 2, 3, S</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">A2-0011-1, 9, 9, M</span><br><span style="font-weight:400;font-style:normal;text-decoration:none"> </span><br><span style="font-weight:400;font-style:normal">Example 2:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Input: (sid=00038800464) 我真不明白。她们可能是追求一些前代的浪漫。</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Output: 00038800464, correct</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Data Source</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">TOCFL Learner Corpus</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">TOCFL Learner Corpus</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">TOCFL Learner Corpus</span>&amp;<br><span style="font-weight:400;font-style:normal;text-decoration:none">HSK Dynamic Composition Corpus</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Training Set</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">1,506 writings</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(5,607 errors)</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">2,205 sentences</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(2,205 errors)</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal">TOCFL Track:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">10,693 sentences </span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(24,492 errors)</span><br><span style="font-weight:400;font-style:normal;text-decoration:none"> </span><br><span style="font-weight:400;font-style:normal">HSK Track:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">10,071 sentences </span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(24,797 errors)</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Test Set</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">This set consists of 1,750 testing sentences. Half of these instances contained no grammatical errors. Another half included one grammatical error.</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">This set consists of 1,000 testing sentences. Half of these sentences contained no grammatical errors, while the other half included one error.</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal">TOCFL Track:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">3,528 sentences</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(1703 correct &amp; 1,825 errors)</span><br><br><span style="font-weight:400;font-style:normal">HSK Track:</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">3,011 sentences</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">(1,539 correct &amp; 1,472 errors)</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Technical Challenges</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">Error Detection</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Error Identification</span></td>
    <td class="tg-0lax" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none">Error Detection (binary class categorization problem)</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Error Identification (multi-class categorization problem)</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Error Position (sequence labeling problem)</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Evaluation Metrics</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">False Positive Rate</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Detection-/Identification-level Acc./Prec./Recall/F1</span></td>
    <td class="tg-0lax" colspan="2"><span style="font-weight:400;font-style:normal;text-decoration:none">False Positive Rate</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Detection-level Accuracy/Precision /Recall/ F1</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Identification-level Accuracy/Precision /Recall/ F1</span><br><span style="font-weight:400;font-style:normal;text-decoration:none">Position-level Accuracy/Precision /Recall/ F1</span></td>
  </tr>
  <tr>
    <td class="tg-0lax">Registered Teams</td>
    <td class="tg-0lax">13 teams (4 from Taiwan, 3 from China, and the remaining 6 from Japan, USA, UK, Germany, New Zealand, and Russia)</td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">13 teams (4 from Taiwan, 3 from China, 2 from USA, 2 from UK, 1 from Japan, and 1 from Poland)</span></td>
    <td class="tg-0lax"><span style="font-weight:400;font-style:normal;text-decoration:none">15 teams (8 from China, 4 from Taiwan, 1 from Dublin, 1 from Germany, and 1 private firm)</span><br></td>
  </tr>
</tbody>
</table>

## Citations
* Lung-Hao Lee, Gaoqi Rao, Liang-Chih Yu, Endong Xun, Baolin Zhang, and Li-Ping Chang (2016). [Overview of the NLP-TEA 2016 Shared Task for Chinese Grammatical Error Diagnosis.](https://aclanthology.org/W16-4906/) In *Proceedings of NLPTEA'16*, pp. 40-48.
* Lung-Hao Lee, Liang-Chih Yu, and Li-Ping Chang (2015). [Overview of the NLP-TEA 2015 Shared Task for Chinese Grammatical Error Diagnosis.](https://aclanthology.org/W15-4401.pdf) In *Proceedings of NLPTEA'15*, pp. 1-6.
* Liang-Chih Yu, Lung-Hao Lee, and Li-Ping Chang (2014). [Overview of Grammatical Error Diagnosis for Learning Chinese as a Foreign Language](https://www.researchgate.net/publication/268802971_Overview_of_Grammatical_Error_Diagnosis_for_Learning_Chinese_as_a_Foreign_Language). In *Proceedings of NLPTEA'14*, pp.42-47.
