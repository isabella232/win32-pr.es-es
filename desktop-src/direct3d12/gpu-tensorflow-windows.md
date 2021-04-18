---
title: Tensorflow con DirectML en Windows
description: Habilitación de TensorFlow con DirectML directamente en Windows
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/22/2020
ms.locfileid: "105720140"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a>Habilitación de TensorFlow con DirectML en Windows

Esta vista previa proporciona a los estudiantes y principiantes una manera de empezar a crear sus conocimientos en el espacio de ML en el hardware existente mediante el paquete TensorFlow con DirectML. Una vez configurado, los usuarios pueden comenzar con los [modelos de tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o con [nuestros ejemplos de DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> La siguiente característica está en versión preliminar y está sujeta a cambios.

## <a name="check-your-version-of-windows"></a>Comprobar la versión de Windows 

El paquete TensorFlow con DirectML en Windows nativo funciona a partir de la versión 1709 de Windows 10 (compilación 16299 o posterior). Puede comprobar el número de versión de compilación ejecutando `winver` mediante el comando **Ejecutar** (tecla del logotipo de Windows + R).

## <a name="check-for-gpu-driver-updates"></a>Comprobar las actualizaciones del controlador de GPU 

Asegúrese de que tiene instalado el controlador de GPU más reciente. Seleccione **Buscar actualizaciones** en la sección **Windows Update** de la aplicación de configuración.

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configuración de TensorFlow con DirectML Preview 

Se recomienda configurar un entorno de Python virtual dentro de Windows. Hay muchas herramientas que puede usar para configurar un entorno de Python virtual: para estas instrucciones, usaremos [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html). En el resto de esta configuración se supone que usa un entorno de miniconda. 

### <a name="set-up-python-environment"></a>Configurar el entorno de Python 

Descargue e instale [Miniconda Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) en el sistema. Hay [orientación adicional para la configuración](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) en el sitio de anaconda. Una vez instalado Miniconda, cree un entorno con Python denominado **directml** y actívelo a través de los siguientes comandos. 

> [!NOTE]
> En los siguientes comandos, usamos Python 3,6. Sin embargo, el paquete tensorflow-directml funciona en un entorno de Python 3,5, 3,6 o 3,7. 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>Instalación de Tensorflow con el paquete DirectML 

Instale el paquete de TensorFlow con un back-end de DirectML mediante PIP mediante la ejecución del siguiente comando.

> [!NOTE]
> El paquete tensorflow-directml solo admite TensorFlow 1,15. 

```
pip install tensorflow-directml
```

Una vez que haya instalado el paquete tensorflow-directml, puede comprobar que se ejecuta correctamente agregando dos. Copie las líneas siguientes en una sesión interactiva de Python. 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

Debería ver una salida similar a la siguiente, con el operador Add colocado en el dispositivo DML. 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow con comentarios y ejemplos de DirectML 

Ya está listo para empezar a aprender más sobre aprendizaje de ML. Consulte los [tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o [nuestros ejemplos](https://github.com/microsoft/DirectML). Usamos este contenido como validación para este paquete de vista previa inicial de TensorFlow con un back-end de DirectML. 

Si tiene problemas o tiene comentarios sobre el paquete de TensorFlow con DirectML, póngase en [contacto con nuestro equipo aquí](https://github.com/microsoft/DirectML/issues). 
