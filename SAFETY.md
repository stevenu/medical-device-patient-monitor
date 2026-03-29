Safety and disclaimers

This project is not a medical device

This repository contains educational hardware and software projects.
None of the devices described or implemented here have been:
  - Cleared or approved by the FDA or any regulatory authority
  - Validated against any medical device standard (IEC 60601, ISO 13485, etc.)
  - Tested for clinical accuracy or safety

Do not use any part of this project for clinical diagnosis,
monitoring, or treatment of any person.

Phase 3 ECG circuit — electrical isolation warning

The Phase 3 ECG circuit connects electrode leads to a person's body.
This circuit has NO patient electrical isolation.

In production medical ECG equipment, a 4kV+ isolation barrier separates
the patient connection from system electronics per IEC 60601-1.
This project does not implement that barrier.

Safe use conditions:
  - Use ONLY with a battery-powered laptop (not connected to mains power)
  - Do not use if you have a cardiac condition or pacemaker
  - Do not use on anyone other than yourself
  - Disconnect immediately if you feel any sensation from the electrodes

AWS HealthLake and patient data

The Phase 6 AWS HealthLake datastore does not have a HIPAA BAA in place.
Never POST real patient health information to this infrastructure.
All test data used in this project is from the developer's own body
and is not protected health information (PHI).
