# Feature-wise CCC rates for top-performing handcrafted Feature Representations (FR).

## VAM database
|Dimension   | Type  | FR ID  | FR desription | CCC  | 
|---|---|---|---|---|
|Valence | Sysytem | mfcc_sma[1]_upleveltime75 | segment duration where signal is above 0.75*range of 1st MFCC coefficient | 0.199 |
| Valence | System |  mfcc_sma[3]_percentile1.0 | first percentile of 3rd MFCC coefficient | 0.171 |
| Arousal | System |  audspec_lengthL1norm_sma_quartile3 | 3rd quantile for magnitude of L1 norm of Auditory Spectrum | 0.725 |
| Arousal |  System | audspec_lengthL1norm_sma_peakMeanAbs | arithmetic mean of peaks for L1 norm of Auditory Spectrum |  0.716 |
| Dominance | System | audspec_lengthL1norm_sma_percentile99.0 | 99th percentile for L1 norm of Auditory Spectrum | 0.659 |
| Dominance | System |  audspec_lengthL1norm_sma_peakMeanAbs | arithmetic mean of peaks for L1 norm of Auditory Spectrum | 0.669 |

## IEMOCAP database
|Dimension   | Type  | FR ID  | FR desription | CCC  | 
|---|---|---|---|---|
| Valence | Sysytem | audspec_lengthL1norm_sma_de_flatness | contour flatness for delta values of magnitude of L1 norm of Auditory Spectrum |0.166 |
| Valence | Sysytem | audSpec_Rfilt_sma_de[23]_flatness | ontour flatness for delta coefficient of 23rd coefficient of Relative Spectral Transform (RASTA)-style filtered applied to Auditory Spectrum | 0.144 |
| Arousal | Sysytem | mfcc_sma[2]_range | range of 2nd MFCC coefficient | 0.469 |
| Arousal | Sysytem | mfcc_sma[2]_pctlrange0-1 | he range of the 1% and the 99% for 2nd MFCC coefficient | 0.473 |
| Dominance | Sysytem | mfcc_sma[2]_pctlrange0-1 | he range of the 1% and the 99% for 2nd MFCC coefficient |0.375 |
| Dominance | Sysytem | mfcc_sma_de[4]_lpc1 | 1st linear prediction filter coefficient for the delta coefficient of 4th MFCC coefficient |0.355 |

For both datasets, the top feature-wise CCC rates. FR represents vocal tract systems.
Descriptions of the top-performing FR can be found in the four columns of tables.

The Python code for extracting WavLM FR used in our study can be found in the following repository:
https://github.com/idiap/ExVo-2022
