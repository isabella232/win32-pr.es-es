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
# <a name="gpu-accelerated-ml-training"></a>Aprendizaje de ML acelerado de GPU

![Gráfico de Windows ML](images/winml-graphic.png)

En esta documentación se explica lo que actualmente se admite en la versión preliminar de aprendizaje de machine learning Accelerated (ML) de GPU para el [subsistema de Windows para Linux](/windows/wsl/about) (WSL) y Windows nativo.  

Esta versión preliminar es compatible con escenarios profesionales y principiantes. A continuación encontrará punteros a guías paso a paso sobre cómo realizar la configuración del sistema en función de su nivel de especialización en ML, proveedor de GPU y la biblioteca de software que piensa usar. 

> [!NOTE]
> Las siguientes características se encuentran en versión preliminar y están sujetas a cambios.


## <a name="professionals"></a>Informático

Si es un científico de datos profesionales que usa un entorno de Linux nativo diario para el desarrollo y la experimentación de los ML de bucle interno, y tiene una GPU de NVIDIA, se recomienda configurar la [versión preliminar de NVIDIA CUDA en WSL 2.](gpu-cuda-in-wsl.md)

## <a name="students-and-beginners"></a>Estudiantes y principiantes 

Si es un estudiante o un principiante que quiere empezar a crear su conocimiento en el espacio de ML, se recomienda configurar TensorFlow con el paquete de back-end de DirectML. Este paquete acelera actualmente los flujos de trabajo en las GPU AMD e Intel. Próximamente se ofrecerá compatibilidad con las GPU de NVIDIA. 

Para aquellos más familiarizados con un entorno de Linux nativo que se inician con flujos de trabajo de aprendizaje automático, se recomienda ejecutar el [paquete de TensorFlow con DirectML en WSL 2](gpu-tensorflow-wsl.md). 

Para aquellos que estén más familiarizados con las ventanas que se inician con los flujos de trabajo de ML, se recomienda configurar [TensorFlow con el paquete DirectML en Windows nativo](gpu-tensorflow-windows.md). 

## <a name="next-steps"></a>Pasos siguientes

* [Habilite NVIDIA CUDA Preview en WSL 2](gpu-cuda-in-wsl.md).
* [Habilite TensorFlow con el paquete de DirectML en WSL 2](gpu-tensorflow-wsl.md).
* [Habilite TensorFlow con el paquete DirectML en ventanas nativas](gpu-tensorflow-windows.md).