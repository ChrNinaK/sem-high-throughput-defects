---
title: Methodology
------
# Experimentally 

Samples were manufactured using Fe7336 powder on a S235JR baseplate via Powder Plasma Arc Additive Manufacturing at the Technical University of Munich. A single track of 10 cm in length was manufactured using Argon as shielding gas. The welding torch was operated at 120 A and 20 V, with a travel speed of 0.002 m/s and a standoff distance of 10 mm. A sample was cut from the central area of the weld track, ground and polished to 1 µm diamond size, and finished with OPS polishing.
SEM imaging was carried out using a ThermoFisherScientific Helios 5 Hydra PFIB system equipped with MAPS software (for acquisition and stitching of subsequentially taken SEM images, i.e. tiles), utilizing an interpolated focus strategy. SE imaging was performed with the Everhart-Thornley detector (ETD), while BSE imaging utilized the angular backscattered segmented detector (ABS). The accelerating voltage was set to 30 kV with a beam current of 6.4 nA, and the working distance was maintained at 4.2 mm. To improve the image stitching quality, tile overlap was set to 10 % in both X and Y directions, with an image resolution of 1536 × 1024 pixels per tile. SE image acquisition settings were varied by adjusting the dwell time (0.1 µs, 0.3 µs, 0.5 µs, 0.75 µs, 1 µs, 5 µs, and 10 µs) and pixel size (48.8 nm, 97.6 nm, 195.3 nm, and 390.6 nm per pixel). Due to MAPS software restrictions, only full tiles could be acquired, meaning that not all datasets represented the exact same area. To standardize the comparison, we used the alignment tool within the MAPS software to crop a consistent area of 1.1 × 1.5 mm from all datasets.
Although the SEM acquisition software provides estimated acquisition times, these values were not suitable for direct comparison since they correspond to differing areas. Instead, we scaled the estimated times according to the cropped area and calculated a relative time factor based on the benchmark dataset used in this study (10 µs dwell time and 195.3 nm pixel size), which was defined as 100%. {ref}`tbl:ParameterStudy` compares the parameters investigated and their relative acquisition times in percentages.

:::{table} MAPS software estimated acquisition times are presented as relative percentages, benchmarked against the reference dataset (10 µs and 195.3 nm, set at 100%)
:label: tbl:ParameterStudy
<table>
    <tr>
        <th rowspan="6" align="middle">Pixel Size [nm]</th> <!-- Merged over 6 rows -->
        <!-- <th rowspan="2">Pixel Size <br> [nm]</th> -->
        <th colspan="9" align="center">Dwell time [µs]</th>
    </tr>
    <tr>
        <th align="center"></th>
        <th align="center">0.1</th>
        <th align="center">0.3</th>
        <th align="center">0.5</th>
        <th align="center">0.75</th>
        <th align="center">1</th>
        <th align="center">5</th>
        <th align="center">10</th>
    </tr>
    <tr>
        <td align="center"><b>390.6</b></td>
        <td align="center">2</td>
        <td align="center">2</td>
        <td align="center">3</td>
        <td align="center">3</td>
        <td align="center">3</td>
        <td align="center">8</td>
        <td align="center">14</td>
    </tr>
    <tr>
        <td align="center"><b>195.3</b></td>
        <td align="center">8</td>
        <td align="center">9</td>
        <td align="center">10</td>
        <td align="center">12</td>
        <td align="center">13</td>
        <td align="center">33</td>
        <td align="center">100</td>
    </tr>
    <tr>
        <td align="center"><b>97.6</b></td>
        <td align="center">33</td>
        <td align="center">37</td>
        <td align="center">41</td>
        <td align="center">47</td>
        <td align="center">52</td>
        <td align="center">135</td>
        <td align="center">---</td>
    </tr>
    <tr>
        <td align="center"><b>48.8</b></td>
        <td align="center">134</td>
        <td align="center">151</td>
        <td align="center">167</td>
        <td align="center">188</td>
        <td align="center">209</td>
        <td align="center">---</td>
        <td align="center">---</td>
    </tr>
</table>
:::

The two different acquired signals, SE and BSE, were used for two distinct types of analysis. The BSE signal, with its strong contrast derived from slight differences in chemical composition and crystal orientation, has been used to detect the fusion boundary between the baseplate material and the AM-built part. Since the SE signal is primarily sensitive to surface structure (topology), it was chosen for surface defect analysis. 

# Defect Detection based on local contrast conditions 
Tiles were stitched into micrographs using MAPS, with blending between tiles as well as tile-to-tile contrast normalization. We developed our own python-based tool for detection of defects in micrographs, making it less sensitive to variations in contrast and brightness across large-area scans. 
{ref}`fig_algorithmWorkflow` highlights the general overview of the workflow. For a more detailed description of the individual steps and interactive tools we refer to the section ‘Algorithm details’. 

:::{figure} 
:name: fig_algorithmWorkflow
:placeholder: ./figures/Fig1.png
Illustrated Workflow in Defect Detection Algorithm with highlighted inputs.
:::


# Algorithm details

## Pre-Processing - Identification of region of Interest 

## Feature Identification

## Parameter Optimization

## Defect Analysis and Metrics

# Assessment of defect detection across varying acquisition parameters


:::{table} MAPS software estimated acquisition times are presented as relative percentages, benchmarked against the reference dataset (10 µs and 195.3 nm, set at 100%)
:label: tbl:ParameterStudy
<table>
    <tr>
        <th rowspan="6" align="middle">Pixel Size [nm]</th> <!-- Merged over 6 rows -->
        <!-- <th rowspan="2">Pixel Size <br> [nm]</th> -->
        <th colspan="9" align="center">Dwell time [µs]</th>
    </tr>
    <tr>
        <th align="center"></th>
        <th align="center">0.1</th>
        <th align="center">0.3</th>
        <th align="center">0.5</th>
        <th align="center">0.75</th>
        <th align="center">1</th>
        <th align="center">5</th>
        <th align="center">10</th>
    </tr>
    <tr>
        <td align="center"><b>390.6</b></td>
        <td align="center">2</td>
        <td align="center">2</td>
        <td align="center">3</td>
        <td align="center">3</td>
        <td align="center">3</td>
        <td align="center">8</td>
        <td align="center">14</td>
    </tr>
    <tr>
        <td align="center"><b>195.3</b></td>
        <td align="center">8</td>
        <td align="center">9</td>
        <td align="center">10</td>
        <td align="center">12</td>
        <td align="center">13</td>
        <td align="center">33</td>
        <td align="center">100</td>
    </tr>
    <tr>
        <td align="center"><b>97.6</b></td>
        <td align="center">33</td>
        <td align="center">37</td>
        <td align="center">41</td>
        <td align="center">47</td>
        <td align="center">52</td>
        <td align="center">135</td>
        <td align="center">---</td>
    </tr>
    <tr>
        <td align="center"><b>48.8</b></td>
        <td align="center">134</td>
        <td align="center">151</td>
        <td align="center">167</td>
        <td align="center">188</td>
        <td align="center">209</td>
        <td align="center">---</td>
        <td align="center">---</td>
    </tr>
</table>
