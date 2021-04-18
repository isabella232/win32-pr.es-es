---
title: Tensorflow con DirectML en WSL 2
description: Habilitación de TensorFlow con DirectML en el subsistema de Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105720184"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>Habilitación de TensorFlow con DirectML en WSL 2

Esta vista previa proporciona a los estudiantes y principiantes una manera de empezar a generar información en el espacio de ML en el hardware existente mediante el paquete TensorFlow con DirectML. Una vez configurado, los usuarios pueden comenzar con los [modelos de tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o con nuestros ejemplos de [DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> Las siguientes características están disponibles en versiones preliminares de Windows 10 y están sujetas a cambios.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Instalación de la compilación más reciente del canal de desarrollo de Windows Insider 

Para usar esta versión preliminar, deberá [registrarse para el programa Windows Insider](https://insider.windows.com/getting-started/#register). Una vez hecho esto, siga [estas instrucciones](https://insider.windows.com/getting-started/#install) para instalar la versión más reciente de Insider. Al elegir la configuración, asegúrese de seleccionar el [canal de desarrollo](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Para esta versión preliminar, necesita la compilación 20150 o posterior. Puede comprobar el número de versión de compilación ejecutando `winver` mediante el comando **Ejecutar** (tecla del logotipo de Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Instalación del controlador de GPU de versión preliminar 

Antes de instalar el paquete de TensorFlow con DirectML en WSL 2, debe instalar los controladores de su proveedor de hardware de GPU. Estos controladores permiten que la GPU de Windows funcione con WSL 2.

### <a name="amd"></a>AMD 

[Descargue e instale el controlador de vista previa de AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) desde su sitio Web. Este controlador de vista previa es compatible con el siguiente hardware: 

* Gráficos AMD Radeon™ series RX y Radeon™ VII. 
* Gráficos de la serie Pro de AMD Radeon™. 
* ™ AMD Ryzen y Ryzen™ PRO con gráficos Radeon™ Vega. 
* Procesadores de™ de AMD Ryzen y Ryzen™ PRO con gráficos Radeon™ Vega. 

Para obtener una lista completa de los productos de AMD compatibles, consulte las notas de la versión de AMD. 

### <a name="intel"></a>Intel 

[Descargue e instale el controlador de vista previa de Intel](https://downloadcenter.intel.com/download/29526) para usarlo con DirectML desde su sitio Web. 

### <a name="nvidia"></a>NVIDIA 

[Descargue e instale el controlador de vista previa de NVIDIA](https://developer.nvidia.com/cuda/wsl/download) para usarlo con DirectML desde su sitio Web. Para obtener más información, consulte la página de [la GPU de NVIDIA en el subsistema de Windows para Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configuración de TensorFlow con DirectML Preview 

### <a name="install-wsl-2"></a>Instalación de WSL 2 

Una vez instalado el controlador anterior, asegúrese de [Habilitar WSL 2](/windows/wsl/install-win10) e [instalar una distribución basada en glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu o Debian). Para nuestras pruebas, hemos usado Ubuntu. Asegúrese de que tiene el kernel más reciente seleccionando **Buscar actualizaciones** en la sección **Windows Update** de la aplicación de configuración. 

> [!NOTE]
> Asegúrese de que tiene las **actualizaciones de recepción para otros productos de Microsoft al actualizar Windows** habilitado. Puede encontrarlo en **Opciones avanzadas** dentro de la sección **Windows Update** de la aplicación de configuración. 

Para esta versión preliminar, necesita una versión de kernel de 4.19.121 o posterior. Puede comprobar el número de versión ejecutando el siguiente comando en PowerShell. 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>Configurar el entorno de Python 

Se recomienda configurar un entorno de Python virtual dentro de la instancia de WSL 2. Hay muchas herramientas que puede usar para configurar un entorno de Python virtual: para estas instrucciones, usaremos [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html). En el resto de esta configuración se supone que usa un entorno de miniconda. 

Instale Miniconda siguiendo las instrucciones que se indican [en el sitio de Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)o mediante la ejecución de los siguientes comandos en WSL. 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

Una vez que Miniconda se instala en WSL, cree un entorno con Python denominado "directml" y actívelo a través de los siguientes comandos. 

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

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow con comentarios y ejemplos de DirectML 

Ya está listo para empezar a aprender más sobre aprendizaje de ML. Consulte los [tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o [nuestros ejemplos](https://github.com/microsoft/DirectML). Usamos este contenido como validación para este paquete de vista previa inicial de TensorFlow con DirectML. 

Si tiene problemas o tiene comentarios sobre el paquete de TensorFlow con DirectML, póngase en [contacto con nuestro equipo aquí](https://github.com/microsoft/DirectML/issues).
