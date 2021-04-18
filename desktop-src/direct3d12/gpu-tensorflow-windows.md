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
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="1b778-103">Habilitación de TensorFlow con DirectML en Windows</span><span class="sxs-lookup"><span data-stu-id="1b778-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="1b778-104">Esta vista previa proporciona a los estudiantes y principiantes una manera de empezar a crear sus conocimientos en el espacio de ML en el hardware existente mediante el paquete TensorFlow con DirectML.</span><span class="sxs-lookup"><span data-stu-id="1b778-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="1b778-105">Una vez configurado, los usuarios pueden comenzar con los [modelos de tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o con [nuestros ejemplos de DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="1b778-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="1b778-106">La siguiente característica está en versión preliminar y está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="1b778-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="1b778-107">Comprobar la versión de Windows</span><span class="sxs-lookup"><span data-stu-id="1b778-107">Check your version of Windows</span></span> 

<span data-ttu-id="1b778-108">El paquete TensorFlow con DirectML en Windows nativo funciona a partir de la versión 1709 de Windows 10 (compilación 16299 o posterior).</span><span class="sxs-lookup"><span data-stu-id="1b778-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="1b778-109">Puede comprobar el número de versión de compilación ejecutando `winver` mediante el comando **Ejecutar** (tecla del logotipo de Windows + R).</span><span class="sxs-lookup"><span data-stu-id="1b778-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="1b778-110">Comprobar las actualizaciones del controlador de GPU</span><span class="sxs-lookup"><span data-stu-id="1b778-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="1b778-111">Asegúrese de que tiene instalado el controlador de GPU más reciente.</span><span class="sxs-lookup"><span data-stu-id="1b778-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="1b778-112">Seleccione **Buscar actualizaciones** en la sección **Windows Update** de la aplicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="1b778-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="1b778-113">Configuración de TensorFlow con DirectML Preview</span><span class="sxs-lookup"><span data-stu-id="1b778-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="1b778-114">Se recomienda configurar un entorno de Python virtual dentro de Windows.</span><span class="sxs-lookup"><span data-stu-id="1b778-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="1b778-115">Hay muchas herramientas que puede usar para configurar un entorno de Python virtual: para estas instrucciones, usaremos [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="1b778-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="1b778-116">En el resto de esta configuración se supone que usa un entorno de miniconda.</span><span class="sxs-lookup"><span data-stu-id="1b778-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="1b778-117">Configurar el entorno de Python</span><span class="sxs-lookup"><span data-stu-id="1b778-117">Set up Python environment</span></span> 

<span data-ttu-id="1b778-118">Descargue e instale [Miniconda Windows Installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) en el sistema.</span><span class="sxs-lookup"><span data-stu-id="1b778-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="1b778-119">Hay [orientación adicional para la configuración](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) en el sitio de anaconda.</span><span class="sxs-lookup"><span data-stu-id="1b778-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="1b778-120">Una vez instalado Miniconda, cree un entorno con Python denominado **directml** y actívelo a través de los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="1b778-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="1b778-121">En los siguientes comandos, usamos Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="1b778-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="1b778-122">Sin embargo, el paquete tensorflow-directml funciona en un entorno de Python 3,5, 3,6 o 3,7.</span><span class="sxs-lookup"><span data-stu-id="1b778-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="1b778-123">Instalación de Tensorflow con el paquete DirectML</span><span class="sxs-lookup"><span data-stu-id="1b778-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="1b778-124">Instale el paquete de TensorFlow con un back-end de DirectML mediante PIP mediante la ejecución del siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="1b778-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="1b778-125">El paquete tensorflow-directml solo admite TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="1b778-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="1b778-126">Una vez que haya instalado el paquete tensorflow-directml, puede comprobar que se ejecuta correctamente agregando dos.</span><span class="sxs-lookup"><span data-stu-id="1b778-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="1b778-127">Copie las líneas siguientes en una sesión interactiva de Python.</span><span class="sxs-lookup"><span data-stu-id="1b778-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="1b778-128">Debería ver una salida similar a la siguiente, con el operador Add colocado en el dispositivo DML.</span><span class="sxs-lookup"><span data-stu-id="1b778-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="1b778-129">Tensorflow con comentarios y ejemplos de DirectML</span><span class="sxs-lookup"><span data-stu-id="1b778-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="1b778-130">Ya está listo para empezar a aprender más sobre aprendizaje de ML.</span><span class="sxs-lookup"><span data-stu-id="1b778-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="1b778-131">Consulte los [tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o [nuestros ejemplos](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="1b778-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="1b778-132">Usamos este contenido como validación para este paquete de vista previa inicial de TensorFlow con un back-end de DirectML.</span><span class="sxs-lookup"><span data-stu-id="1b778-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="1b778-133">Si tiene problemas o tiene comentarios sobre el paquete de TensorFlow con DirectML, póngase en [contacto con nuestro equipo aquí](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="1b778-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
