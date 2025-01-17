# Summary

When running the `FindSamplesAndBenchmark` wdl with many samples, it sometimes happens that a few fail in Terra while most succeed. 
Unfortunately, this means that the outputs of benchmarking the successful ones don't get compiled into one convenient .csv file to use for data analysis. 
If you don't mind sacrificing the few that failed, or want to get started analyzing the successful ones ASAP, this wdl will automatically collect 
the successful outputs and aggregate them into one .csv, similar to the last task of the benchmarking wdl. 

# Inputs

* `namespace`: the first personalized part of your workspace URL; e.g. if you see `<my_project>/<my_workspace>` at the top
  in Terra, then this should be `<my_project>` as a string.
* `workspace_name`: specific name for your workspace, e.g. `<my_workspace>` in the last example.
* `submission_id`: the submission id for the `FindSamplesAndBenchmark` run, found from the "Job History" tab.

