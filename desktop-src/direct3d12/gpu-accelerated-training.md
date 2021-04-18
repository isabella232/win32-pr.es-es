---
title: Aceleración de GPU en WSL
description: Direct Machine Learning (DirectML) impulsa GPU-Accelleration en el subsistema de Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720174"
---
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="ff680-103">Aprendizaje de ML acelerado de GPU</span><span class="sxs-lookup"><span data-stu-id="ff680-103">GPU accelerated ML training</span></span>

![Gráfico de Windows ML](images/winml-graphic.png)

<span data-ttu-id="ff680-105">En esta documentación se explica lo que actualmente se admite en la versión preliminar de aprendizaje de machine learning Accelerated (ML) de GPU para el [subsistema de Windows para Linux](/windows/wsl/about) (WSL) y Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="ff680-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="ff680-106">Esta versión preliminar es compatible con escenarios profesionales y principiantes.</span><span class="sxs-lookup"><span data-stu-id="ff680-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="ff680-107">A continuación encontrará punteros a guías paso a paso sobre cómo realizar la configuración del sistema en función de su nivel de especialización en ML, proveedor de GPU y la biblioteca de software que piensa usar.</span><span class="sxs-lookup"><span data-stu-id="ff680-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="ff680-108">Las siguientes características se encuentran en versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff680-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="ff680-109">Informático</span><span class="sxs-lookup"><span data-stu-id="ff680-109">Professionals</span></span>

<span data-ttu-id="ff680-110">Si es un científico de datos profesionales que usa un entorno de Linux nativo diario para el desarrollo y la experimentación de los ML de bucle interno, y tiene una GPU de NVIDIA, se recomienda configurar la [versión preliminar de NVIDIA CUDA en WSL 2.](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="ff680-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="ff680-111">Estudiantes y principiantes</span><span class="sxs-lookup"><span data-stu-id="ff680-111">Students and beginners</span></span> 

<span data-ttu-id="ff680-112">Si es un estudiante o un principiante que quiere empezar a crear su conocimiento en el espacio de ML, se recomienda configurar TensorFlow con el paquete de back-end de DirectML.</span><span class="sxs-lookup"><span data-stu-id="ff680-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="ff680-113">Este paquete acelera actualmente los flujos de trabajo en las GPU AMD e Intel.</span><span class="sxs-lookup"><span data-stu-id="ff680-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="ff680-114">Próximamente se ofrecerá compatibilidad con las GPU de NVIDIA.</span><span class="sxs-lookup"><span data-stu-id="ff680-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="ff680-115">Para aquellos más familiarizados con un entorno de Linux nativo que se inician con flujos de trabajo de aprendizaje automático, se recomienda ejecutar el [paquete de TensorFlow con DirectML en WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="ff680-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="ff680-116">Para aquellos que estén más familiarizados con las ventanas que se inician con los flujos de trabajo de ML, se recomienda configurar [TensorFlow con el paquete DirectML en Windows nativo](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="ff680-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="ff680-117">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="ff680-117">Next steps</span></span>

* <span data-ttu-id="ff680-118">[Habilite NVIDIA CUDA Preview en WSL 2](gpu-cuda-in-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="ff680-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="ff680-119">[Habilite TensorFlow con el paquete de DirectML en WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="ff680-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="ff680-120">[Habilite TensorFlow con el paquete DirectML en ventanas nativas](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="ff680-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>