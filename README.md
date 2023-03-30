# Stellarator-Database-Utilities
Utility functions for a stellarator database

TODO:
- [ ] Make hashing function for an equilibrium based solely on physics quantities such as
  - Boundary Shape
  - Profiles evaluated at a given N points btwn $\rho=[0,1]$
  - Total enclosed toroidal flux
  - this function should only care about the first X sig figs of the quantities, to avoid any small numerical inconsistencies between output files that are really the same physical configuration
- [ ] Make conversion utility functions for DESC/VMEC outputs (2 separate functions, one for each code) , currently focusing on fixed-boundary equilibria
  - Input
    - the DESC/VMEC output (and possibly input file if available)
    - User-inputted provenance of file (where it came from)
    - User-inputted description (e.g. "W7-X high iota with a N=2 boundary perturbation"
    - User-inputted device_ID (physical device that the equilibrium is connected to e.g. "W7-X" or "HSX")
    - User-inputted class (type of configuration e.g. "tokamak", "QA", "QS", "heliotron")
    - User-inputted user name (e.g. "John Doe")
  - Output
    - a file (possibly .csv) containing the table values that the database requires (see [this document](https://docs.google.com/document/d/1UQY2uHWL4EgPugQ1YSjKtHJKClHbpHbP/edit?usp=share_link&ouid=104808552924700331813&rtpof=true&sd=true) for example)
