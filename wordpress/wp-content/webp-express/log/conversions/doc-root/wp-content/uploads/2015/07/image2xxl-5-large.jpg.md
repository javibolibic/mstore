WebP Express 0.17.2. Conversion triggered using bulk conversion, 2019-10-12 08:49:06

*WebP Convert 2.3.0*  ignited.
- PHP version: 7.0.33
- Server software: Apache

Stack converter ignited

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2015/07/image2xxl-5-large.jpg
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/07/image2xxl-5-large.jpg.webp
- log-call-arguments: true
- converters: (array of 9 items)

The following options have not been explicitly set, so using the following defaults:
- converter-options: (empty array)
- shuffle: false
- preferred-converters: (empty array)
- extra-converters: (empty array)

The following options were supplied and are passed on to the converters in the stack:
- default-quality: 70
- encoding: "auto"
- max-quality: 80
- metadata: "none"
- near-lossless: 60
- quality: "auto"
------------


*Trying: cwebp* 

Options:
------------
The following options have been set explicitly. Note: it is the resulting options after merging down the "jpeg" and "png" options and any converter-prefixed options.
- source: [doc-root]/wp-content/uploads/2015/07/image2xxl-5-large.jpg
- destination: [doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/07/image2xxl-5-large.jpg.webp
- default-quality: 70
- encoding: "auto"
- low-memory: true
- log-call-arguments: true
- max-quality: 80
- metadata: "none"
- method: 6
- near-lossless: 60
- quality: "auto"
- use-nice: true
- command-line-options: ""
- try-common-system-paths: true
- try-supplied-binary-for-os: true

The following options have not been explicitly set, so using the following defaults:
- alpha-quality: 85
- auto-filter: false
- preset: "none"
- size-in-percentage: null (not set)
- skip: false
- rel-path-to-precompiled-binaries: *****
- try-cwebp: true
- try-discovering-cwebp: true
------------

Encoding is set to auto - converting to both lossless and lossy and selecting the smallest file

Converting to lossy
Looking for cwebp binaries.
Discovering if a plain cwebp call works (to skip this step, disable the "try-cwebp" option)
- Executing: cwebp -version. Result: *Exec failed* (the cwebp binary was not found at path: cwebp)
Nope a plain cwebp call does not work
Discovering binaries using "which -a cwebp" command. (to skip this step, disable the "try-discovering-cwebp" option)
Found 0 binaries
Discovering binaries by peeking in common system paths (to skip this step, disable the "try-common-system-paths" option)
Found 1 binaries: 
- /usr/local/bin/cwebp
Discovering binaries which are distributed with the webp-convert library (to skip this step, disable the "try-supplied-binary-for-os" option)
Checking if we have a supplied precompiled binary for your OS (Darwin)... We do.
Found 1 binaries: 
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14
Detecting versions of the cwebp binaries found
- Executing: /usr/local/bin/cwebp -version. Result: version: *1.0.3*
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14 -version. Result: *Exec failed* (the cwebp binary was not found at path: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14)
Binaries ordered by version number.
- /usr/local/bin/cwebp: (version: 1.0.3)
Trying the first of these. If that should fail (it should not), the next will be tried and so on.
Creating command line options for version: 1.0.3
Quality of source is 90. This is higher than max-quality, so using max-quality instead (80)
The near-lossless option ignored for lossy
Trying to convert by executing the following command:
nice /usr/local/bin/cwebp -metadata none -q 80 -alpha_q '85' -m 6 -low_memory '[doc-root]/wp-content/uploads/2015/07/image2xxl-5-large.jpg' -o '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/07/image2xxl-5-large.jpg.webp.lossy.webp' 2>&1

*Output:* 
Saving file '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/07/image2xxl-5-large.jpg.webp.lossy.webp'
File:      [doc-root]/wp-content/uploads/2015/07/image2xxl-5-large.jpg
Dimension: 803 x 1024
Output:    23676 bytes Y-U-V-All-PSNR 44.84 49.27 50.04   45.94 dB
           (0.23 bpp)
block count:  intra4:        901  (27.60%)
              intra16:      2363  (72.40%)
              skipped:      1646  (50.43%)
bytes used:  header:            138  (0.6%)
             mode-partition:   4905  (20.7%)
 Residuals bytes  |segment 1|segment 2|segment 3|segment 4|  total
  intra4-coeffs:  |   12916 |     387 |     103 |     129 |   13535  (57.2%)
 intra16-coeffs:  |     321 |     232 |     111 |     784 |    1448  (6.1%)
  chroma coeffs:  |    3053 |     149 |      62 |     360 |    3624  (15.3%)
    macroblocks:  |      22%|       3%|       2%|      74%|    3264
      quantizer:  |      27 |      26 |      20 |      15 |
   filter level:  |       8 |      17 |      27 |       3 |
------------------+---------+---------+---------+---------+-----------------
 segments total:  |   16290 |     768 |     276 |    1273 |   18607  (78.6%)

Success
Reduction: 68% (went from 72 kb to 23 kb)

Converting to lossless
Looking for cwebp binaries.
Discovering if a plain cwebp call works (to skip this step, disable the "try-cwebp" option)
- Executing: cwebp -version. Result: *Exec failed* (the cwebp binary was not found at path: cwebp)
Nope a plain cwebp call does not work
Discovering binaries using "which -a cwebp" command. (to skip this step, disable the "try-discovering-cwebp" option)
Found 0 binaries
Discovering binaries by peeking in common system paths (to skip this step, disable the "try-common-system-paths" option)
Found 1 binaries: 
- /usr/local/bin/cwebp
Discovering binaries which are distributed with the webp-convert library (to skip this step, disable the "try-supplied-binary-for-os" option)
Checking if we have a supplied precompiled binary for your OS (Darwin)... We do.
Found 1 binaries: 
- [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14
Detecting versions of the cwebp binaries found
- Executing: /usr/local/bin/cwebp -version. Result: version: *1.0.3*
- Executing: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14 -version. Result: *Exec failed* (the cwebp binary was not found at path: [doc-root]/wp-content/plugins/webp-express/vendor/rosell-dk/webp-convert/src/Convert/Converters/Binaries/cwebp-103-mac-10_14)
Binaries ordered by version number.
- /usr/local/bin/cwebp: (version: 1.0.3)
Trying the first of these. If that should fail (it should not), the next will be tried and so on.
Creating command line options for version: 1.0.3
Trying to convert by executing the following command:
nice /usr/local/bin/cwebp -metadata none -q 80 -alpha_q '85' -near_lossless 60 -m 6 -low_memory '[doc-root]/wp-content/uploads/2015/07/image2xxl-5-large.jpg' -o '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/07/image2xxl-5-large.jpg.webp.lossless.webp' 2>&1

*Output:* 
Saving file '[doc-root]/wp-content/webp-express/webp-images/doc-root/wp-content/uploads/2015/07/image2xxl-5-large.jpg.webp.lossless.webp'
File:      [doc-root]/wp-content/uploads/2015/07/image2xxl-5-large.jpg
Dimension: 803 x 1024
Output:    195514 bytes (1.90 bpp)
Lossless-ARGB compressed size: 195514 bytes
  * Header size: 3123 bytes, image data size: 192366
  * Lossless features used: PREDICTION CROSS-COLOR-TRANSFORM SUBTRACT-GREEN
  * Precision Bits: histogram=5 transform=4 cache=10

Success
Reduction: -164% (went from 72 kb to 191 kb)

Picking lossy
cwebp succeeded :)

Converted image in 1253 ms, reducing file size with 68% (went from 72 kb to 23 kb)
