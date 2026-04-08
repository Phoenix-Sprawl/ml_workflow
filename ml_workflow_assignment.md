## Task 1
### Identify which column in the dataset is the label, and which column, if included as a feature, would introduce data leakage. For each, write one sentence justifying your choice.

* repeat_purchase_flag = label - this feature is giving a desired categorical output like yes or no. In this scenario, it’s flagging the repeat purchase customers within 30 days as 1, otherwise as 0.
* discount_used_on_repeat_order = leaky feature - this feature is directly derived from the label ‘repeat_purchase_flag’.

## Task 2
### Your manager skips straight to training a gradient boosting model. Suggest two steps from the complete ML workflow that should have been completed first, and briefly explain why each step matters before jumping to a complex model.

Suggested ML workflow:
* Data Split - Data should be split into training, validation & test set. Test data should be held out of the training set. If the model is trained on a full dataset, it is a form of leakage.
* Baseline model - A baseline model should be there to set a minimum performance level that this gradient boosting model should surpass.
