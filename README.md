# tensorflow_inceptionv3_for_android
tensorflow inceptionv3 for android



# 运行命令
```
//利用inceptionv3进行训练自己的模型
ROOT_PATH=/home/jovyan/
python retrain.py \
--image_dir=images \
--output_graph=${ROOT_PATH}output_graph.pb \
--output_labels=${ROOT_PATH}output_graph.txt \
--random_crop=20 \
--random_scale=20 \
--random_brightness=20 \
--how_many_training_steps=500 \
--architecture=inception_v3


//对生成的模型进行裁剪
python /srv/conda/lib/python3.6/site-packages/tensorflow/python/tools/strip_unused.py \
  --input_graph=${ROOT_PATH}output_graph.pb \
  --output_graph=${ROOT_PATH}strip_inception_v3.pb \
  --input_node_names=Mul \
  --output_node_names=final_result \
  --input_binary=true



```

# 去mybinder上试验
https://mybinder.org/v2/gh/sanfooh/tensorflow_inceptionv3_for_android.git/master