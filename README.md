The Chronic Kidney Disease dataset, which comprises 25 features, 400 instances, and 2 classes. The dataset contains 1012 missing values, and the majority and minority
classes contain 908 and 104 missing values. We first pass the dataset through our subspace classifier generation using a Decision Tree classifier.
Starting with the entire set of 25 attributes, we calculate the class imbalance ratio by  comparing the number of minority instances to majority instances (step 1). We then  equally divided the number of instances in proportion to minority instances to create balanced datasets, resulting in 2 refined datasets (step 2). For each refined dataset, we add weights to the instances (Step 3) and continuously detect subspaces until the
convergence criterion is met, defined as the point when the attribute list of the Decision Tree remains unchanged (Steps 4-14). We repeat these steps until all attributes are exhausted from the refined datasets (step 15). We found four subspaces in refined dataset 1 and five subspaces in refined dataset 2. The set of subspace classifiers generated  from these refined datasets forms an ensemble classifier (step 16), which uses
the strengths of the subspace classifiers to classify the test data robustly.
