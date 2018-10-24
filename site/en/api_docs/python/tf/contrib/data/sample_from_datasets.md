

page_type: reference
<style> table img { max-width: 100%; } </style>


<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.data.sample_from_datasets

``` python
tf.contrib.data.sample_from_datasets(
    datasets,
    weights=None,
    seed=None
)
```



Defined in [`tensorflow/contrib/data/python/ops/interleave_ops.py`](https://www.github.com/tensorflow/tensorflow/blob/r1.9/tensorflow/contrib/data/python/ops/interleave_ops.py).

Samples elements at random from the datasets in `datasets`.

#### Args:

* <b>`datasets`</b>: A list of <a href="../../../tf/data/Dataset"><code>tf.data.Dataset</code></a> objects with compatible structure.
* <b>`weights`</b>: (Optional.) A list of `len(datasets)` floating-point values where
    `weights[i]` represents the probability with which an element should be
    sampled from `datasets[i]`, or a <a href="../../../tf/data/Dataset"><code>tf.data.Dataset</code></a> object where each
    element is such a list. Defaults to a uniform distribution across
    `datasets`.
* <b>`seed`</b>: (Optional.) A <a href="../../../tf/int64"><code>tf.int64</code></a> scalar <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>, representing the
    random seed that will be used to create the distribution. See
    <a href="../../../tf/set_random_seed"><code>tf.set_random_seed</code></a> for behavior.


#### Returns:

A dataset that interleaves elements from `datasets` at random, according to
`weights` if provided, otherwise with uniform probability.


#### Raises:

* <b>`TypeError`</b>: If the `datasets` or `weights` arguments have the wrong type.
* <b>`ValueError`</b>: If the `weights` argument is specified and does not match the
    length of the `datasets` element.