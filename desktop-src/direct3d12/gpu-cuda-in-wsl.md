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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>Habilitación de NVIDIA CUDA en WSL 2

El SDK de Windows Insider admite la ejecución de las herramientas de aprendizaje automático, las bibliotecas y los marcos de trabajo populares existentes que usan NVIDIA CUDA para la aceleración de hardware de GPU dentro de una instancia de WSL 2. Esto incluye PyTorch y TensorFlow, así como toda la compatibilidad con el kit de herramientas de contenedor de Docker y NVIDIA disponible en un entorno de Linux nativo. 

> [!NOTE]
> Las siguientes características están disponibles en versiones preliminares de Windows 10 y están sujetas a cambios.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Instalación de la compilación más reciente del canal de desarrollo de Windows Insider 

Para usar esta versión preliminar, deberá [registrarse para el programa Windows Insider](https://insider.windows.com/getting-started/#register). Una vez hecho esto, siga [estas instrucciones](https://insider.windows.com/getting-started/#install) para instalar la versión más reciente de Insider. Al elegir la configuración, asegúrese de seleccionar el [canal de desarrollo](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Para esta versión preliminar, necesita la compilación 20150 o posterior. Puede comprobar el número de versión de compilación ejecutando `winver` mediante el comando **Ejecutar** (tecla del logotipo de Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Instalación del controlador de GPU de versión preliminar 

Descargue e instale el [controlador compatible con NVIDIA CUDA para WSL](https://developer.nvidia.com/cuda/wsl) para usarlo con los flujos de trabajo de CUDA ml existentes. 

## <a name="set-up-wsl-2-for-the-preview"></a>Configuración de WSL 2 para la versión preliminar 

Una vez instalado el controlador anterior, asegúrese de [Habilitar WSL 2](/windows/wsl/install-win10) e [instalar una distribución basada en glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu o Debian). Asegúrese de que tiene el kernel más reciente seleccionando **Buscar actualizaciones** en la sección **Windows Update** de la aplicación de configuración. 

> [!NOTE]
> Asegúrese **de recibir actualizaciones de otros productos de Microsoft al actualizar Windows** habilitado. Puede encontrarlo en **Opciones avanzadas** dentro de la sección **Windows Update** de la aplicación de configuración. 

Para esta versión preliminar, necesita una versión de kernel de 4.19.121 o posterior. Puede comprobar el número de versión ejecutando el siguiente comando en PowerShell. 

```powershell
wsl cat /proc/version
```

Ahora puede empezar a usar los flujos de trabajo de Linux existentes a través de [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)o mediante la instalación de [PyTorch](https://pytorch.org/get-started/locally/) o [TensorFlow](https://www.tensorflow.org/install/gpu) en WSL 2. En [la guía de usuario de CUDA en WSL](https://docs.nvidia.com/cuda/wsl-user-guide/index.html), se captura más información sobre cómo configurar.

Comparta sus comentarios sobre la compatibilidad de NVIDIA a través de su [Foro de la comunidad para CUDA en WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).
