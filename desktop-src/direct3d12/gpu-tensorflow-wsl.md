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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="441ef-103">Habilitación de TensorFlow con DirectML en WSL 2</span><span class="sxs-lookup"><span data-stu-id="441ef-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="441ef-104">Esta vista previa proporciona a los estudiantes y principiantes una manera de empezar a generar información en el espacio de ML en el hardware existente mediante el paquete TensorFlow con DirectML.</span><span class="sxs-lookup"><span data-stu-id="441ef-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="441ef-105">Una vez configurado, los usuarios pueden comenzar con los [modelos de tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o con nuestros ejemplos de [DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="441ef-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="441ef-106">Las siguientes características están disponibles en versiones preliminares de Windows 10 y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="441ef-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="441ef-107">Instalación de la compilación más reciente del canal de desarrollo de Windows Insider</span><span class="sxs-lookup"><span data-stu-id="441ef-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="441ef-108">Para usar esta versión preliminar, deberá [registrarse para el programa Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="441ef-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="441ef-109">Una vez hecho esto, siga [estas instrucciones](https://insider.windows.com/getting-started/#install) para instalar la versión más reciente de Insider.</span><span class="sxs-lookup"><span data-stu-id="441ef-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="441ef-110">Al elegir la configuración, asegúrese de seleccionar el [canal de desarrollo](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="441ef-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="441ef-111">Para esta versión preliminar, necesita la compilación 20150 o posterior.</span><span class="sxs-lookup"><span data-stu-id="441ef-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="441ef-112">Puede comprobar el número de versión de compilación ejecutando `winver` mediante el comando **Ejecutar** (tecla del logotipo de Windows + R).</span><span class="sxs-lookup"><span data-stu-id="441ef-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="441ef-113">Instalación del controlador de GPU de versión preliminar</span><span class="sxs-lookup"><span data-stu-id="441ef-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="441ef-114">Antes de instalar el paquete de TensorFlow con DirectML en WSL 2, debe instalar los controladores de su proveedor de hardware de GPU.</span><span class="sxs-lookup"><span data-stu-id="441ef-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="441ef-115">Estos controladores permiten que la GPU de Windows funcione con WSL 2.</span><span class="sxs-lookup"><span data-stu-id="441ef-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="441ef-116">AMD</span><span class="sxs-lookup"><span data-stu-id="441ef-116">AMD</span></span> 

<span data-ttu-id="441ef-117">[Descargue e instale el controlador de vista previa de AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) desde su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="441ef-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="441ef-118">Este controlador de vista previa es compatible con el siguiente hardware:</span><span class="sxs-lookup"><span data-stu-id="441ef-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="441ef-119">Gráficos AMD Radeon™ series RX y Radeon™ VII.</span><span class="sxs-lookup"><span data-stu-id="441ef-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="441ef-120">Gráficos de la serie Pro de AMD Radeon™.</span><span class="sxs-lookup"><span data-stu-id="441ef-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="441ef-121">™ AMD Ryzen y Ryzen™ PRO con gráficos Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="441ef-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="441ef-122">Procesadores de™ de AMD Ryzen y Ryzen™ PRO con gráficos Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="441ef-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="441ef-123">Para obtener una lista completa de los productos de AMD compatibles, consulte las notas de la versión de AMD.</span><span class="sxs-lookup"><span data-stu-id="441ef-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="441ef-124">Intel</span><span class="sxs-lookup"><span data-stu-id="441ef-124">Intel</span></span> 

<span data-ttu-id="441ef-125">[Descargue e instale el controlador de vista previa de Intel](https://downloadcenter.intel.com/download/29526) para usarlo con DirectML desde su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="441ef-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="441ef-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="441ef-126">NVIDIA</span></span> 

<span data-ttu-id="441ef-127">[Descargue e instale el controlador de vista previa de NVIDIA](https://developer.nvidia.com/cuda/wsl/download) para usarlo con DirectML desde su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="441ef-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="441ef-128">Para obtener más información, consulte la página de [la GPU de NVIDIA en el subsistema de Windows para Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .</span><span class="sxs-lookup"><span data-stu-id="441ef-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="441ef-129">Configuración de TensorFlow con DirectML Preview</span><span class="sxs-lookup"><span data-stu-id="441ef-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="441ef-130">Instalación de WSL 2</span><span class="sxs-lookup"><span data-stu-id="441ef-130">Install WSL 2</span></span> 

<span data-ttu-id="441ef-131">Una vez instalado el controlador anterior, asegúrese de [Habilitar WSL 2](/windows/wsl/install-win10) e [instalar una distribución basada en glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu o Debian).</span><span class="sxs-lookup"><span data-stu-id="441ef-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="441ef-132">Para nuestras pruebas, hemos usado Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="441ef-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="441ef-133">Asegúrese de que tiene el kernel más reciente seleccionando **Buscar actualizaciones** en la sección **Windows Update** de la aplicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="441ef-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="441ef-134">Asegúrese de que tiene las **actualizaciones de recepción para otros productos de Microsoft al actualizar Windows** habilitado.</span><span class="sxs-lookup"><span data-stu-id="441ef-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="441ef-135">Puede encontrarlo en **Opciones avanzadas** dentro de la sección **Windows Update** de la aplicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="441ef-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="441ef-136">Para esta versión preliminar, necesita una versión de kernel de 4.19.121 o posterior.</span><span class="sxs-lookup"><span data-stu-id="441ef-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="441ef-137">Puede comprobar el número de versión ejecutando el siguiente comando en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="441ef-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="441ef-138">Configurar el entorno de Python</span><span class="sxs-lookup"><span data-stu-id="441ef-138">Set up Python environment</span></span> 

<span data-ttu-id="441ef-139">Se recomienda configurar un entorno de Python virtual dentro de la instancia de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="441ef-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="441ef-140">Hay muchas herramientas que puede usar para configurar un entorno de Python virtual: para estas instrucciones, usaremos [Miniconda de Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="441ef-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="441ef-141">En el resto de esta configuración se supone que usa un entorno de miniconda.</span><span class="sxs-lookup"><span data-stu-id="441ef-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="441ef-142">Instale Miniconda siguiendo las instrucciones que se indican [en el sitio de Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)o mediante la ejecución de los siguientes comandos en WSL.</span><span class="sxs-lookup"><span data-stu-id="441ef-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="441ef-143">Una vez que Miniconda se instala en WSL, cree un entorno con Python denominado "directml" y actívelo a través de los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="441ef-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="441ef-144">En los siguientes comandos, usamos Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="441ef-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="441ef-145">Sin embargo, el paquete tensorflow-directml funciona en un entorno de Python 3,5, 3,6 o 3,7.</span><span class="sxs-lookup"><span data-stu-id="441ef-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="441ef-146">Instalación de Tensorflow con el paquete DirectML</span><span class="sxs-lookup"><span data-stu-id="441ef-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="441ef-147">Instale el paquete de TensorFlow con un back-end de DirectML mediante PIP mediante la ejecución del siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="441ef-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="441ef-148">El paquete tensorflow-directml solo admite TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="441ef-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="441ef-149">Una vez que haya instalado el paquete tensorflow-directml, puede comprobar que se ejecuta correctamente agregando dos.</span><span class="sxs-lookup"><span data-stu-id="441ef-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="441ef-150">Copie las líneas siguientes en una sesión interactiva de Python.</span><span class="sxs-lookup"><span data-stu-id="441ef-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="441ef-151">Debería ver una salida similar a la siguiente, con el operador Add colocado en el dispositivo DML.</span><span class="sxs-lookup"><span data-stu-id="441ef-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="441ef-152">Tensorflow con comentarios y ejemplos de DirectML</span><span class="sxs-lookup"><span data-stu-id="441ef-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="441ef-153">Ya está listo para empezar a aprender más sobre aprendizaje de ML.</span><span class="sxs-lookup"><span data-stu-id="441ef-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="441ef-154">Consulte los [tutoriales de TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) o [nuestros ejemplos](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="441ef-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="441ef-155">Usamos este contenido como validación para este paquete de vista previa inicial de TensorFlow con DirectML.</span><span class="sxs-lookup"><span data-stu-id="441ef-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="441ef-156">Si tiene problemas o tiene comentarios sobre el paquete de TensorFlow con DirectML, póngase en [contacto con nuestro equipo aquí](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="441ef-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
