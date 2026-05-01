# Machine Learning

## Summary

- Supervised, unsupervised, semisupervised, Reinforcement Learning
- Online versus batch learning
- Instance-based versus model-based learning

### Algorithms

1. Supervised learning
    1. k-Nearest Neighbors
    1. Linear Regression
    1. Logistic Regression
    1. Support Vector Machines (SVMs)
    1. Decision Trees and Random Forests
    1. Neural networks

1. Unsupervised learning
    1. Clustering
        1. K-Means
        1. DBSCAN
        1. Hierarchical Cluster Analysis (HCA)
    1. Anomaly detection and novelty detection
        1. One-class SVM
        1. Isolation Forest
    1. Visualization and dimensionality reduction
        1. Principal Component Analysis (PCA)
        1. Kernel PCA
        1. Locally-Linear Embedding (LLE)
        1. t-distributed Stochastic Neighbor Embedding (t-SNE)
    1. Association rule learning
        1. Apriori
        1. Eclat

### Challenges

1. Insufficient quantity of training data
1. Non-representative training data
1. Poor-quality data
1. Irrelevant features
1. Overfitting/underfitting the training data

## Jupyter Notebook

To run code on this repository, it is recommended to use Jupyter Notebook and, in particular, from a pre-built Docker image that supports the machine learning library TensorFlow.

To pull the `jupyter/tensorflow-notebook` image into the Docker host machine:
```bash
docker pull quay.io/jupyter/tensorflow-notebook
```

Next, run the following `docker run` command from the folder where the project files are:
```bash
docker run -it --rm -p 8888:8888 -v "${PWD}":/home/jovyan/work quay.io/jupyter/tensorflow-notebook
```

This command is also in the script `jupyter_run.sh` included in this repository.

For more details, go to [Jupyter Docker Stacks] documentation and [jupyter/tensorflow-notebook] source on GitHub.

Files on the host's current directory (i.e. from where the container was started) will be mapped into the container as `/home/jovyan/work`.

To access the Jupyter server from a web browser, go to this URL:
```
http://localhost:8888/lab?token=[token]
```

Note that `[token]` must be replaced by the access token that is generated after the Docker container is run (shown after `docker run` command is executed).

This server can also be accessed from another host:
```
http://[hostname or IP address]:8888/lab?token=[token]
```

## References

- Aurelien Geron: "Hands-On Machine Learning with Scikit-Learn, Keras and TensorFlow" (O'Reilly) - 2nd. Edition
- [Registry of Open Data on AWS]: open datasets available via AWS resources.
- [jupyter/tensorflow-notebook] source on GitHub
- [Jupyter Docker Stacks] documentation

[Registry of Open Data on AWS]: https://registry.opendata.aws/

[jupyter/tensorflow-notebook]: https://github.com/jupyter/docker-stacks/blob/main/images/tensorflow-notebook

[Jupyter Docker Stacks]: https://jupyter-docker-stacks.readthedocs.io/en/latest/index.html
