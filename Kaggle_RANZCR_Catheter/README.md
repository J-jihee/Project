# Kaggle Competition - RANZCR CliP - Catheter and Line Position Challenge

## Development environment
- Python 3.9.1
- Tenserflow.keras version 2.4.0
- MongoDB server version 4.4.3

## Model used
- EfficientNet (b0-b7)

## Competition Overview
Serious complications can occur as a result of malpositioned lines and tubes in patients. Doctors and nurses frequently use checklists for placement of lifesaving equipment to ensure they follow protocol in managing patients. Yet, these steps can be time consuming and are still prone to human error, especially in stressful situations when hospitals are at capacity.
Hospital patients can have catheters and lines inserted during the course of their admission and serious complications can arise if they are positioned incorrectly. Nasogastric tube malpositioning into the airways has been reported in up to 3% of cases, with up to 40% of these cases demonstrating complications. Airway tube malposition in adult patients intubated outside the operating room is seen in up to 25% of cases [4,5]. The likelihood of complication is directly related to both the experience level and specialty of the proceduralist. Early recognition of malpositioned tubes is the key to preventing risky complications (even death), even more so now that millions of COVID-19 patients are in need of these tubes and lines.
The gold standard for the confirmation of line and tube positions are chest radiographs. However, a physician or radiologist must manually check these chest x-rays to verify that the lines and tubes are in the optimal position. Not only does this leave room for human error, but delays are also common as radiologists can be busy reporting other scans. Deep learning algorithms may be able to automatically detect malpositioned catheters and lines. Once alerted, clinicians can reposition or remove them to avoid life-threatening complications.
In this competition, you’ll detect the presence and position of catheters and lines on chest x-rays. Use machine learning to train and test your model on 40,000 images to categorize a tube that is poorly placed.

## Dataset
The dataset has been labelled with a set of definitions to ensure consistency with labelling. The normal category includes lines that were appropriately positioned and did not require repositioning. The borderline category includes lines that would ideally require some repositioning but would in most cases still function adequately in their current position. The abnormal category included lines that required immediate repositioning.

- train image : 30,083 (6.4GB)
- test image : 3,582 (805MB)
- train.csv
- train TFRecords (4.45GB)
- test TFRecords (554MB)
- train_annotations.csv
- sample_submission.csv

## Evaluation
Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target.
To calculate the final score, AUC is calculated for each of the 11 labels, then averaged. The score is then the average of the individual AUCs of each predicted column.

