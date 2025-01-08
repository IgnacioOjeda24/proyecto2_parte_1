# Proyecto_parte_1: 
Instrucción:

Proyecto 1 : Utilizando un api de hugginface de un modelo LLM crea una aplicación donde el usuario pueda realizar preguntas y el modelo le responda, en el readme especifica el modelo usado y los parámetros en la petición junto con un ejemplo de uso.

# Selección del modelo de Hugging Face: 

Este proyecto utiliza un modelo Vision Transformer (ViT) para clasificar las imágenes y tener una predicción con porcentaje de los primeros 7 objetos con más probabilidad, se ejecuta de manera local utilizando Pytorch y los modelos preentrenados disponibles en Hugging Face.

## Requisitos para la Ejecución

### Dependencias

1. **Python 3.8 a 3.10**
2. **Librerías necesarias**:
   - `torch`
   - `transformers`
   - `matplotlib`
   - `easygui`
3. Librerías instaladas en foto.

   
![u1](https://github.com/user-attachments/assets/dd969a8c-3457-4116-b280-07394cc9ec33)

   
4. Antes de correr el programa, instalar los siguientes comandos:
   - `python -m venv nombre_propio_de_entorno virtual, ejemplo python -m venv proyecto_2 `
   - `Para activar el entorno virtual, se ejecuta el comando \proyecto_2\Scripts\activate`
   - `Ejecutar para que el programa funcione bien: pip install torch transformers matplotlib Pillow easygui`
   - `easygui`
5. Hardware: GPU (no obligatorio): Si usted tiene una CPU compatible, la librería PyTorch la utilizará de forma automática para acelerar la ejecución, en el caso de lo contrario el modelo funcionará exitosamente en la CPU, aunque será menos eficiente. Si no tienes una, el modelo funcionará correctamente en la CPU, aunque será más lento.


## Selección del modelo de Hugging Face: 

1. Clonar el proyecto con el siguiente enlace o comando:
2. Verifica si está todo instalado, se haya ejecutado los comandos mencionados anteriormente y tener la api token de hugging face.
3. En el código, por defecto sale que saldrá 7 objetos y la probabilidad con 3 decimales.
4. Para que el programa funcione usted tiene que ejecutar el siguiente comando:
   ```bash
   python .\script_modelo.py
5. Se abrirá la pestaña de importar un archivo del computador que tenga en usuario siempre y cuando que tenga formatos como jpg, png, bmp y jpeg.
6. Luego, realizará la predicción y mostrará las primeras 7 clases probables y sus probabilidades con 3 decimales en la terminal de power shell de visual studio code.
   Ejemplo:

   ![u3](https://github.com/user-attachments/assets/607cea10-1a7f-419c-9244-ac9b39568e49)

   
7. A la vez se mostrá la imagen que importó el usuario desde su computador y su predición principal en una ventana gráfica.

   Ejemplo:

   ![u2](https://github.com/user-attachments/assets/6b14aa9e-3229-417d-a1cd-2389b9731b0a)

8. Para seguir el proceso o terminar el proceso, tiene que presionar el botón x de la ventana.

    ![u6](https://github.com/user-attachments/assets/c3a341ac-b572-4210-a6c8-9a3f13b913d8)

   
9. Si el usuario desea con el proceso poner una s en el caso no continua con n.
    En el caso de sí.
   
    ![u4](https://github.com/user-attachments/assets/71f4848f-632e-4245-ba63-2a1425842cb4)

    En el caso de no.

    ![u5](https://github.com/user-attachments/assets/59f6e2b0-f9b3-47a5-999e-646f10e56ea1)

10. Así sucesivamente sigue la consulta de la imagen.

# Sección sobre Transformers y Ejecución de Modelos en Local: 

## ¿Qué son los Transformers?: 

Los transformers son una arquitectura de modelos de aprendizaje profundo utilizada principalmente en procesamiento de lenguaje natural (NLP), aunque también se ha extendido a otras tareas como visión por computadora. Los modelos como el Vision Transformer (ViT) son versiones adaptadas para trabajar con imágenes.

Un modelo transformer se basa en el mecanismo de autoatención, que permite al modelo aprender a centrarse en diferentes partes de la entrada (en este caso, la imagen) mientras procesa la información. Esto lo convierte en una arquitectura muy eficaz para tareas como la clasificación de imágenes y la traducción de texto.

## Ejecución de Modelos en Local:

Este proyecto utiliza el modelo google/vit-base-patch16-224, un modelo Vision Transformer preentrenado disponible en Hugging Face. La ejecución de modelos transformers en local se hace posible gracias a bibliotecas como transformers y torch, que permiten cargar modelos preentrenados y realizar inferencias de manera eficiente tanto en CPU como en GPU.

#### Ejecución de Modelos en Local:


1. Instalación de dependencias: Instalar las librerías necesarias para interactuar con el modelo.

2. Cargar el modelo preentrenado: Utilizando la librería transformers de Hugging Face, cargamos el modelo ViTForImageClassification junto con su procesador asociado.

3. Procesamiento de la imagen: La imagen se carga y se procesa para que sea compatible con el modelo (es decir, se convierte en un tensor adecuado para la entrada del transformer).

4. Realización de predicción: El modelo realiza una predicción sobre la imagen y devuelve las clases y probabilidades más probables.

5. Visualización de resultados: Se muestran las predicciones y la imagen utilizando matplotlib.


## Lo que Aprendí:

En este proyecto, aprendí a trabajar con modelos preentrenados de transformers para tareas de visión por computadora, como la clasificación de imágenes. El proceso de usar un modelo transformer localmente es bastante directo y eficiente, especialmente cuando se trabaja con GPUs, ya que estos modelos son computacionalmente intensivos.

Además, comprendí mejor cómo el procesamiento de imágenes con modelos transformers es similar a otros tipos de entrada, como texto, pero con ciertas modificaciones, como el uso de patching para dividir las imágenes en pequeñas secciones que el modelo puede procesar de manera más efectiva.
