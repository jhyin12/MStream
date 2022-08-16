# MStream

Here is the code of MStream and MStreamF.
The code is written by python3.6 with no dependence.

## Usage
- Modify the hyper-parameters in `main.py`.
- Run code with `python main.py`.

## File Structure
- `/data/`: We provide two datasets: `News`, `Tweets` and two processed datasets: `News-T`, `Tweets-T`. The datasets are in format of JSON like follows:
    ```
    {"Id": "006218", "clusterNo": 8, "textCleaned": "scottish independence alistair carmichael issue complacency warning"}
    {"Id": "000071", "clusterNo": 40, "textCleaned": "doggie scofflaw bagged dna testing"}
    ```

- `/result/` The outputs will be in the result folder and the result of each batch is saved separately in each folder.
    + `ClusteringResult.txt`: You can check the clustering results of each folder which are in format like follows: (The former is ID of each document and the latter is predicted cluster of each document.)
    ```
        006218 31
        000071 2
    ```
    

    + `PhiWordsInTopics.txt`: You can check the topic words of each folder which are in format like follows:
    ```
        Topic 0:
            pandemic	0.03410629654705485
            captured	0.03410629654705485
            unsure	0.025643195666892347
            higher	0.025643195666892347
            thought	0.025643195666892347
        Topic 2:
            favorite	0.03323826239578762
            nj	0.03323826239578762
            globe	0.02226853883282141
            won	0.02226853883282141
            seduced	0.02226853883282141
    ```

    + `SizeOfEachCluster.txt`: You can check the size of each cluster of each folder which are in format like follows: (The former is ID of each cluster and the latter is document number of each cluster.)
    ```
        0:9,
        2:5,
    ```
    




## Citation
```
@inproceedings{yin2018model,
  title={Model-based clustering of short text streams},
  author={Yin, Jianhua and Chao, Daren and Liu, Zhongkun and Zhang, Wei and Yu, Xiaohui and Wang, Jianyong},
  booktitle={Proceedings of the 24th ACM SIGKDD international conference on knowledge discovery \& data mining},
  pages={2634--2642},
  year={2018}
}
```