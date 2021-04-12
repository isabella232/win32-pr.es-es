---
title: Manipulaciones
description: En esta sección se explica la manipulación de objetos para Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch, manipulaciones
- manipulaciones, acerca de
- manipulaciones, diferencias de gestos
- gestos, diferencias de manipulación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356757"
---
# <a name="manipulations"></a>Manipulaciones

En esta sección se explica la manipulación de objetos para Windows Touch.

## <a name="manipulation-overview"></a>Información general sobre la manipulación

Una manera cómoda de pensar en las manipulaciones es considerarlas un superconjunto de gestos. Lo que puede hacer con los gestos, puede hacerlo con más flexibilidad y con una precisión más precisa mediante el uso de manipulaciones. La diferencia entre las manipulaciones y los gestos se demuestra mejor con un ejemplo sencillo. Puede expandir un objeto y, al mismo tiempo, convertirlo mediante manipulaciones; con los gestos, solo puede realizar una vez. Esta capacidad de manipular un objeto en tiempo real hace que las aplicaciones sean más intuitivas para los usuarios al habilitar una experiencia más realista.

Las API de manipulación se utilizan para simplificar las operaciones de transformación en objetos para aplicaciones habilitadas para toque. Las manipulaciones se realizan en Windows 7 a través del objeto COM Manipulations. Mediante el uso de manipulaciones, los desarrolladores pueden admitir con mayor facilidad la inercia (física de objetos) y pueden realizar transformaciones con facilidad en objetos de una manera coherente con otras aplicaciones. En las secciones siguientes se explican varias maneras en las que puede realizar manipulaciones.



| Sección                                                                                            | Descripción                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agregar compatibilidad de manipulación a código no administrado](adding-manipulation-support-in-unmanaged-code.md) | Explica cómo implementar un receptor de eventos para la interfaz [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) y agregar controladores de eventos al código. |
| [Manipulaciones avanzadas](advanced-manipulations.md)                                               | Explica cómo realizar manipulaciones complejas.                                                                                                       |
| [Rotación de un solo dedo](single-finger-rotation.md)                                               | Explica cómo girar un objeto utilizando un punto de pivote y el procesador de manipulación.                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones e inercia](manipulation-and-inertia.md)
</dt> </dl>

 

 




