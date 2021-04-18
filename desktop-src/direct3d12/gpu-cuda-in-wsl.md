---
title: Habilitación de NVIDIA CUDA en WSL 2
description: Habilitación de la versión preliminar de NVIDIA CUDA en el subsistema de Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/03/2020
ms.locfileid: "105720180"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="8b8c0-103">Habilitación de NVIDIA CUDA en WSL 2</span><span class="sxs-lookup"><span data-stu-id="8b8c0-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="8b8c0-104">El SDK de Windows Insider admite la ejecución de las herramientas de aprendizaje automático, las bibliotecas y los marcos de trabajo populares existentes que usan NVIDIA CUDA para la aceleración de hardware de GPU dentro de una instancia de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="8b8c0-105">Esto incluye PyTorch y TensorFlow, así como toda la compatibilidad con el kit de herramientas de contenedor de Docker y NVIDIA disponible en un entorno de Linux nativo.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b8c0-106">Las siguientes características están disponibles en versiones preliminares de Windows 10 y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="8b8c0-107">Instalación de la compilación más reciente del canal de desarrollo de Windows Insider</span><span class="sxs-lookup"><span data-stu-id="8b8c0-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="8b8c0-108">Para usar esta versión preliminar, deberá [registrarse para el programa Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="8b8c0-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="8b8c0-109">Una vez hecho esto, siga [estas instrucciones](https://insider.windows.com/getting-started/#install) para instalar la versión más reciente de Insider.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="8b8c0-110">Al elegir la configuración, asegúrese de seleccionar el [canal de desarrollo](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="8b8c0-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="8b8c0-111">Para esta versión preliminar, necesita la compilación 20150 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="8b8c0-112">Puede comprobar el número de versión de compilación ejecutando `winver` mediante el comando **Ejecutar** (tecla del logotipo de Windows + R).</span><span class="sxs-lookup"><span data-stu-id="8b8c0-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="8b8c0-113">Instalación del controlador de GPU de versión preliminar</span><span class="sxs-lookup"><span data-stu-id="8b8c0-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="8b8c0-114">Descargue e instale el [controlador compatible con NVIDIA CUDA para WSL](https://developer.nvidia.com/cuda/wsl) para usarlo con los flujos de trabajo de CUDA ml existentes.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="8b8c0-115">Configuración de WSL 2 para la versión preliminar</span><span class="sxs-lookup"><span data-stu-id="8b8c0-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="8b8c0-116">Una vez instalado el controlador anterior, asegúrese de [Habilitar WSL 2](/windows/wsl/install-win10) e [instalar una distribución basada en glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu o Debian).</span><span class="sxs-lookup"><span data-stu-id="8b8c0-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="8b8c0-117">Asegúrese de que tiene el kernel más reciente seleccionando **Buscar actualizaciones** en la sección **Windows Update** de la aplicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b8c0-118">Asegúrese **de recibir actualizaciones de otros productos de Microsoft al actualizar Windows** habilitado.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="8b8c0-119">Puede encontrarlo en **Opciones avanzadas** dentro de la sección **Windows Update** de la aplicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="8b8c0-120">Para esta versión preliminar, necesita una versión de kernel de 4.19.121 o posterior.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="8b8c0-121">Puede comprobar el número de versión ejecutando el siguiente comando en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="8b8c0-122">Ahora puede empezar a usar los flujos de trabajo de Linux existentes a través de [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)o mediante la instalación de [PyTorch](https://pytorch.org/get-started/locally/) o [TensorFlow](https://www.tensorflow.org/install/gpu) en WSL 2.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="8b8c0-123">En [la guía de usuario de CUDA en WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html), se captura más información sobre cómo configurar.</span><span class="sxs-lookup"><span data-stu-id="8b8c0-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="8b8c0-124">Comparta sus comentarios sobre la compatibilidad de NVIDIA a través de su [Foro de la comunidad para CUDA en WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span><span class="sxs-lookup"><span data-stu-id="8b8c0-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
