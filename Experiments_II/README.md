- Test matrix is in the "test_matrix.csv" file. (one sea-state with 10 realisations)

- Runs are identified by "ID" (for instance "350")

- Runs with the ship are in matlab files "run_ID.csv.zip". And corresponding calibration runs (same wave, no ship) are in "run_ID_calibration.csv.zip"


- Relevant channels are :
  -"WGi" : wave probes
  -"My_ATI" : VBM at midship
  -"Body-pitch" : Pitch
  -"Body-Z" : vertical position (heave)
  -"Body-X" : Longitudinal position (low + wave frequencies)

- Data are in model scale (1/65)

- For runs with the ship, position of wave probes are indicated in "probes.csv". Wave probes located at CoG_x, on the side of the basin, is WG2.

- For calibration runs, the probes positions and numbering is different. The one at the ship location is "WG4".
