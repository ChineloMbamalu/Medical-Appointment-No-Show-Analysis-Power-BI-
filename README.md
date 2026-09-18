# Medical-Appointment-No-Show-Analysis-Power-BI-
What tracking a 100k+ appointment record taught me

<img width="1000" height="558" alt="image" src="https://github.com/user-attachments/assets/62754a4b-8a90-416f-99e1-d7d7c70be1f7" />

**Overview**

This is a healthcare analytics dashboard built on the well-known Kaggle "Medical Appointment No Shows" dataset (Brazil, 2016), tracking ~100k+ outpatient appointments.

**Data Model**

The report runs on a single table, KaggleV2-May-2016, with variables split (per the author's own framing) into:

**Independent variables:** No_Show, Gender, Age

**Dependent fields:** Patient_ID, Appointment_ID, Scheduled_Day, Appointment_Day, Neighbourhood, Scholarship, Hypertension, Diabetes, Alcoholism, Handicap.

Age_Group - a calculated column created to group the continuous Age field. Three DAX measures: Average Age, Count of Patient ID, and No Show Rate -  each purpose-built rather than relying on default column aggregation.

**Demographics**

Patients under 20 account for the highest volume of appointments; the 60+ cohort books the fewest. ~65% of appointments are made by women, vs. ~35% by men - a striking gender skew worth investigating further (e.g., is it driven by maternal/reproductive care visits?).

**Attendance & seasonality**

Attendance peaked in May (~64,000) and dropped sharply in April (~2,600) - a volatility signal that likely reflects scheduling/data artifacts (this Kaggle dataset is known to be concentrated around a narrow date window) rather than a genuine seasonal pattern, and is worth a sanity-check against raw record counts.
Overall, ~79% of patients attended their appointment vs. ~20% no-shows - a solid headline attendance rate.

**Chronic conditions**

Hypertensive patients showed up more often (~18,000) than diabetic patients (~4,000) - plausibly because hypertension requires more frequent routine monitoring.

**SMS reminders - the counter-intuitive finding**

This is the most interesting insight in the whole report: the raw numbers show a large group who received an SMS reminder and still didn't show up, and post-analysis synthesis goes further, concluding that patients who did not receive an SMS reminder actually showed up more than those who did.

**Recommendations**

**Male engagement programmes** - workplace- and community-based outreach, since men are both under-represented in bookings and slightly more prone to no-shows.
Flexible clinic hours for working-age patients of both genders.

**Diabetes-specific follow-up care** - nutrition counselling, education sessions, peer support groups - to close the attendance gap versus hypertensive patients.

**Smarter SMS strategy** - multi-stage reminders (48h/24h out), personalised messaging, interactive confirm-by-reply, and voice calls for elderly patients - directly responding to the finding that current SMS reminders aren't moving the needle.

**Structured no-show policy** - easy rescheduling, telemedicine options, and tracking of repeat defaulters, plus transportation/carer support for elderly patients.
