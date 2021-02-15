# Contrastive Learning for Cold-start Recommendation
This is our Pytorch implementation for our paper.

## Environment Requirement
The code has been tested running under Python 3.5.2. The required packages are as follows:
- Pytorch == 1.1.0
- torch-cluster == 1.4.2
- torch-geometric == 1.2.1
- torch-scatter == 1.2.0
- torch-sparse == 0.4.0
- numpy == 1.16.0

## Example to Run the Codes
The instruction of commands has been clearly stated in the codes.
- Movielens dataset  
`python main.py --model_name='CLCRec' --l_r=0.001 --reg_weight=0.1 --num_workers=4 --num_neg=128 --has_a=True --has_t=True --has_v=True --lr_lambda=0.5 --temp_value=2.0 --num_sample=0.5` 
- Amazon dataset  
`python main.py --model_name='CLCRec' --data_path=amazon --l_r=0.001 --reg_weight=0.001 --num_workers=4 --num_neg=512 --has_v=True --lr_lambda=0.9  --num_sample=0.5`  

Some important arguments:  

- `lr_lambda` It specifics the value of lambda to balance the U-I and R-E mutual information. 

- `num_sample` This parameter indicates the number of negative sampling. 

- `temp_value` It specifics the temprature value in density ratio functions.

## Dataset
- We provide two processed datasets: Movielens and Amazon. (The details could be found in our article)  
- For Kwai and Tiktok datasets, due to the copyright, please connect the owners of datasets via [Kwai](https://www.kuaishou.com/activity/uimc) and [Tiktok](http://ai-lab-challenge.bytedance.com/tce/vc/).

## Copyright (C) <year> 

This program is licensed under the GNU General Public License 3.0 (https://www.gnu.org/licenses/gpl-3.0.html). Any derivative work obtained under this license must be licensed under the GNU General Public License as published by the Free Software Foundation, either Version 3 of the License, or (at your option) any later version, if this derivative work is distributed to a third party.
