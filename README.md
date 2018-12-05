# tensorflow_inceptionv3_for_android
tensorflow inceptionv3 for android



# 代码
```
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
```

# 去mybinder上试验
https://mybinder.org/v2/gh/sanfooh/tensorflow_inceptionv3_for_android.git/master