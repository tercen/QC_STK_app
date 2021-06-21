# STK_QC_app

##### Description

`STK_QC_app` is an application that estimates nominal CV's that can be used for setting a peptide cut-off. 
Nominal CV's are estimated without the need of using technical replicates. In contrast, the App for Replicate QC measures nominal CVs based on the evaluation of technical replicates.

##### Details

* The CV's are estimated using the model for the CV as a function of signal level described for the Two Component Error Model. For estimating Sigma0 for this model
it is assumed that a quantile of spots with the lowest signal does not show a signal in any included condition. Sigma0 is then estimated by the overall standard deviation of this quantile of spots. Sigma1 is set to an assumed value (instrument parameter) for the technical replication CV.

* Default values for
   - Quantile of lowest signal spots to use for estimating Sigma0: 0.1
   - Assumed technical CV (Sigma1): 0.1
  
* Advanced users may edit the above values may by opening the app and changing the properties of the "Estimate Nominal CV" operator.

The input data is the [ptk dataset](https://tercen.com/r/7f865df18753ebf56ca2bbafe1ef7497)

This workflow has 3 operators:

* [check_input_operator](https://github.com/tercen/check_input1_operator)
* [Nominal CV Estimate operator](https://github.com/tercen/nominal_cv_estimate_operator)
* [Log Cutoff operator](https://github.com/tercen/log_cutoff_operator)

This workflow has 1 view:

* Log Signals by Nominal CV

##### See Also

[STK_QC_app](https://github.com/tercen/STK_QC_app)
