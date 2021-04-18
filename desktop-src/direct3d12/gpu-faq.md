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
# <a name="faq"></a><span data-ttu-id="34bd0-103">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="34bd0-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="34bd0-104">Cómo habilitar la aceleración DirectML</span><span class="sxs-lookup"><span data-stu-id="34bd0-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="34bd0-105">El dispositivo DirectML está habilitado de forma predeterminada, siempre y cuando tenga disponible una GPU de DirectX 12 adecuada.</span><span class="sxs-lookup"><span data-stu-id="34bd0-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="34bd0-106">Las operaciones de TensorFlow se asignarán automáticamente al dispositivo DirectML si es posible.</span><span class="sxs-lookup"><span data-stu-id="34bd0-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="34bd0-107">Si tiene problemas para determinar si el modelo se está ejecutando con la aceleración de DirectML o no, puede colocarlo `tf.debugging.set_log_device_placement(True)` como la primera instrucción del programa y TensorFlow imprimirá la información de ubicación del dispositivo en la consola.</span><span class="sxs-lookup"><span data-stu-id="34bd0-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="34bd0-108">Cómo controlar la posición del dispositivo de operaciones específicas?</span><span class="sxs-lookup"><span data-stu-id="34bd0-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="34bd0-109">Como con cualquier otro dispositivo (consulte la [Guía de TensorFlow: uso de una GPU](https://www.tensorflow.org/guide/gpu)), puede usar `tf.device()` para controlar el dispositivo en el que se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="34bd0-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="34bd0-110">La cadena del dispositivo DirectML es `'DML'` .</span><span class="sxs-lookup"><span data-stu-id="34bd0-110">The DirectML device string is `'DML'`.</span></span> 


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

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="34bd0-111">Tengo varias GPU.</span><span class="sxs-lookup"><span data-stu-id="34bd0-111">I have multiple GPUs.</span></span> <span data-ttu-id="34bd0-112">Cómo seleccionar cuál se usa en DirectML?</span><span class="sxs-lookup"><span data-stu-id="34bd0-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="34bd0-113">Hay un par de maneras diferentes de hacerlo, en función de si desea controlar el nivel de proceso o por sesión (o ambos).</span><span class="sxs-lookup"><span data-stu-id="34bd0-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="34bd0-114">Si desea controlar qué dispositivos están visibles para todo el proceso de TensorFlow, use la `DML_VISIBLE_DEVICES` variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="34bd0-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="34bd0-115">Si desea controlarlo por sesión, use `tf.GPUOptions.visible_device_list` ...</span><span class="sxs-lookup"><span data-stu-id="34bd0-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="34bd0-116">Cómo usar la `DML_VISIBLE_DEVICES` variable de entorno para controlar las GPU que se usan en DirectML?</span><span class="sxs-lookup"><span data-stu-id="34bd0-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="34bd0-117">TensorFlow con DirectML admite una `DML_VISIBLE_DEVICES` variable de entorno, que toma la forma de una lista separada por comas de identificadores de dispositivo (también conocidos como "índices de adaptador"). Cuando se establece, solo los identificadores de dispositivo de esa lista serán visibles para TensorFlow en todo el proceso.</span><span class="sxs-lookup"><span data-stu-id="34bd0-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="34bd0-118">Los dispositivos excluidos mediante `DML_VISIBLE_DEVICES` no aparecerán en la lista de dispositivos físicos disponibles para TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="34bd0-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="34bd0-119">Este es un ejemplo de salida **sin** `DML_VISIBLE_DEVICES` set:</span><span class="sxs-lookup"><span data-stu-id="34bd0-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="34bd0-120">Con `DML_VISIBLE_DEVICES="1"`:</span><span class="sxs-lookup"><span data-stu-id="34bd0-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="34bd0-121">Tenga en cuenta que al restringir los dispositivos visibles solo al índice 1 (AMD Radeon RX 5700 XT), TensorFlow ahora asigna un identificador de 0 a este dispositivo y lo convierte en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="34bd0-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="34bd0-122">También puede volver a ordenar los dispositivos con esta variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="34bd0-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="34bd0-123">Por ejemplo, establecer `DML_VISIBLE_DEVICES="1,0"` :</span><span class="sxs-lookup"><span data-stu-id="34bd0-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="34bd0-124">Tenga en cuenta que las dos GPU (NVIDIA TITAN V y AMD Radeon RX 5700 XT) ahora han cambiado de lugar.</span><span class="sxs-lookup"><span data-stu-id="34bd0-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="34bd0-125">Para evitar que determinados dispositivos estén visibles, puede proporcionar un identificador no válido (por ejemplo, `-1` ) en la lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="34bd0-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="34bd0-126">Se omiten todos los identificadores de dispositivos después de la entrada no válida.</span><span class="sxs-lookup"><span data-stu-id="34bd0-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="34bd0-127">También puede utilizarlo para deshabilitar completamente la aceleración de DirectML.</span><span class="sxs-lookup"><span data-stu-id="34bd0-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="34bd0-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="34bd0-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="34bd0-129">Cómo usar la `visible_device_list` opción de sesión para controlar qué GPU usa DirectML para ejecutar la sesión</span><span class="sxs-lookup"><span data-stu-id="34bd0-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="34bd0-130">Similar a `DML_VISIBLE_DEVICES` , también puede establecer una cadena similar para controlar los dispositivos visibles en un nivel de sesión.</span><span class="sxs-lookup"><span data-stu-id="34bd0-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="34bd0-131">El `visible_device_list` atributo está disponible en la `GPUOptions` clase cuando se crea la sesión de TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="34bd0-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

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

<span data-ttu-id="34bd0-132">Puede leer la referencia de la [API de TensorFlow GPUOptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="34bd0-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>