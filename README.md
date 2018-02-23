# Project 1: Finding Lane Lines on the Road #
## Reflection ##
### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

The project consists of modifications to two very similar functions.  The first, `test_pipeline`, runs a still image through a lane detection pipeline and saves the results.  The purpose of implementing this function is to test the effects of adjusting the numerous parameters to the pipeline algorithms.  The pipeline begins by applying a grayscale transform and then applies the following algorithms:
1. **Gaussian filter** applies local averaging to flatten noisy gradients.  This improves performance of next algorithm.  The parameter `kernel_size` is the only tunable setting.
2. **Canny Edge Detection** identifies edge pixels in areas of the image with a steep brightness gradient.  The relevant parameters are `low_threshold` and `high_threshold`.
3. **Hough Transform** identifies lines of edge pixels in the image.  The relevant parameters are `rho`, `theta`, `threshold`, `min_line_len`, and `max_line_gap`.
4. **Region Masking** retains only pixels in a polygonal region.  The relevant parameter is `vertices`.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
