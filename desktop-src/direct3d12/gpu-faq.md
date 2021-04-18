---
title: 'Preguntas frecuentes de aceleración de GPU en WSL '
description: Preguntas más frecuentes sobre la aceleración de GPU en el subsistema de Windows para Linux
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "105720186"
---
# <a name="faq"></a>Preguntas más frecuentes

### <a name="how-do-i-enable-directml-acceleration"></a>Cómo habilitar la aceleración DirectML 

 
El dispositivo DirectML está habilitado de forma predeterminada, siempre y cuando tenga disponible una GPU de DirectX 12 adecuada. Las operaciones de TensorFlow se asignarán automáticamente al dispositivo DirectML si es posible. 

Si tiene problemas para determinar si el modelo se está ejecutando con la aceleración de DirectML o no, puede colocarlo `tf.debugging.set_log_device_placement(True)` como la primera instrucción del programa y TensorFlow imprimirá la información de ubicación del dispositivo en la consola.

### <a name="how-do-i-control-device-placement-of-specific-operations"></a>Cómo controlar la posición del dispositivo de operaciones específicas? 
 

Como con cualquier otro dispositivo (consulte la [Guía de TensorFlow: uso de una GPU](https://www.tensorflow.org/guide/gpu)), puede usar `tf.device()` para controlar el dispositivo en el que se ejecutará. 
 

La cadena del dispositivo DirectML es `'DML'` . 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a>Tengo varias GPU. Cómo seleccionar cuál se usa en DirectML?

Hay un par de maneras diferentes de hacerlo, en función de si desea controlar el nivel de proceso o por sesión (o ambos).

Si desea controlar qué dispositivos están visibles para todo el proceso de TensorFlow, use la `DML_VISIBLE_DEVICES` variable de entorno. Si desea controlarlo por sesión, use `tf.GPUOptions.visible_device_list` ...

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a>Cómo usar la `DML_VISIBLE_DEVICES` variable de entorno para controlar las GPU que se usan en DirectML?

TensorFlow con DirectML admite una `DML_VISIBLE_DEVICES` variable de entorno, que toma la forma de una lista separada por comas de identificadores de dispositivo (también conocidos como "índices de adaptador"). Cuando se establece, solo los identificadores de dispositivo de esa lista serán visibles para TensorFlow en todo el proceso. Los dispositivos excluidos mediante `DML_VISIBLE_DEVICES` no aparecerán en la lista de dispositivos físicos disponibles para TensorFlow.

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

Este es un ejemplo de salida **sin** `DML_VISIBLE_DEVICES` set:

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Con `DML_VISIBLE_DEVICES="1"`:

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Tenga en cuenta que al restringir los dispositivos visibles solo al índice 1 (AMD Radeon RX 5700 XT), TensorFlow ahora asigna un identificador de 0 a este dispositivo y lo convierte en el valor predeterminado.

También puede volver a ordenar los dispositivos con esta variable de entorno. Por ejemplo, establecer `DML_VISIBLE_DEVICES="1,0"` :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Tenga en cuenta que las dos GPU (NVIDIA TITAN V y AMD Radeon RX 5700 XT) ahora han cambiado de lugar.

Para evitar que determinados dispositivos estén visibles, puede proporcionar un identificador no válido (por ejemplo, `-1` ) en la lista separada por comas. Se omiten todos los identificadores de dispositivos después de la entrada no válida. También puede utilizarlo para deshabilitar completamente la aceleración de DirectML.

`DML_VISIBLE_DEVICES="-1"`:

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a>Cómo usar la `visible_device_list` opción de sesión para controlar qué GPU usa DirectML para ejecutar la sesión

Similar a `DML_VISIBLE_DEVICES` , también puede establecer una cadena similar para controlar los dispositivos visibles en un nivel de sesión. El `visible_device_list` atributo está disponible en la `GPUOptions` clase cuando se crea la sesión de TensorFlow.

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

Puede leer la referencia de la [API de TensorFlow GPUOptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) para obtener más detalles.