### get img from google drive in colab & make it into a batch

```python
import pathlib
img_path = pathlib.Path('/content/drive/MyDrive/[pic path]')

img = keras.preprocessing.image.load_img(
      img_path, target_size=(img_height, img_width)
      )

img_array = keras.preprocessing.image.img_to_array(img)

# single image [height, width, channels] ---> a batch of one image (ex. [1, height, width, channels])
img_array = tf.expand_dims(img_array, 0)
```
