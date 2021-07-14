rst语法规范
~~~~~~~~~~~~~~~~~~~

图片
---------------------------------
文档引用的图片存储在文档源码目录下的media文件夹中，按部分、章节及文档分目录存储。

图片要直接使用如下形式,方便居中：

.. code-block:: rst
   :linenos:

    .. figure:: media/rst_spec/none.png
        :alt: error
        :align: center

        图 1 none

小图片穿插于文字中使用，其中第三行代码写于整个rst文件末尾

.. code-block:: rst
   :linenos:

   |none|

   .. |none| image:: media/rst_spec/none.png

rst格式检查
--------------------------
使用vscode的rst插件在编写时就会有格式检查。编写文档时应尽量满足该格式检查的规范。
对于docx转rst后的不规范文档，做到见一个改一个。

make html时，编译会有提示输出，尽量让它不输出的warning。


文档编码和回车
----------------
文档编码统一用“utf-8”， 回车使用“LF”，不要使用“CRLF”，文档编码和回车可在VS-Code的右下角设置。


代码引用
---------------------------------

超过3行的代码要加上行号、并用caption名指明代码片段的名，对于引用的代码文件，使用caption指明引用的路径名。

我们一般不使用caption属性，用以下格式即可。

.. code-block:: rst
   :linenos:

    .. code-block:: rst
        :linenos:

表格
----------

.. code-block:: rst
   :linenos:

    .. list-table:: Frozen Delights!
        :widths: 15 10 30
        :header-rows: 1

        * - Treat
          - Quantity
          - Description
        * - Albatross
          - 2.99
          - On a stick!
        * - Crunchy Frog
          - 1.49
          - If we took the bones out, it wouldn't be
            crunchy, now would it?
        * - Gannet Ripple
          - 1.99
          - On a stick!

widths属性根据需求决定表格宽度；header-rows统一值为1。