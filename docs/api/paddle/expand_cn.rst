.. _cn_api_paddle_expand:

expand
-------------------------------

.. py:function:: paddle.expand(x, shape, name=None)

根据 ``shape`` 指定的形状扩展 ``x``，扩展后，``x`` 的形状和 ``shape`` 指定的形状一致。

``x`` 的维数和 ``shape`` 的元素数应小于等于 6，并且 ``shape`` 中的元素数应该大于等于 ``x`` 的维数。扩展的维度的维度值应该为 1。

下图展示了一个 expand 的情形——一个形状为[1,2,3]的，值为[[1, 2, 5], [3, 0, 4]]的三维张量通过 expand 操作转变为形状为[2,2,3]的三维张量。通过比较，可以清晰地看到张量形状变化前后各元素的对应关系。

.. image:: ../../images/api_legend/expand.png
   :width: 600
   :alt: 图例

参数
:::::::::
    - **x** (Tensor) - 输入的 Tensor，数据类型为：bool、float16、float32、float64、int32、int64、uint8 或 uint16。
    - **shape** (tuple|list|Tensor) - 给定输入 ``x`` 扩展后的形状，若 ``shape`` 为 list 或者 tuple，则其中的元素值应该为整数或者是形状为 1-D 或 0-D 的 Tensor，若 ``shape`` 类型为 Tensor，则其应该为 1-D Tensor。值为-1 表示保持相应维度的形状不变。
    - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

返回
:::::::::
``N-D Tensor``，数据类型与 ``x`` 相同。

代码示例
:::::::::

COPY-FROM: paddle.expand
