# Cargar el modelo entrenado
model = tf.keras.models.load_model("modelo_senales.h5")

# Convertir a TensorFlow Lite
converter = tf.lite.TFLiteConverter.from_keras_model(model)
tflite_model = converter.convert()

# Guardar modelo convertido
with open("modelo_senales.tflite", "wb") as f:
    f.write(tflite_model)
from google.colab import files
files.download("modelo_senales.tflite")
