---
title: Manipulaciones
description: En esta sección se explica la manipulación de objetos Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Táctil, manipulaciones
- manipulaciones, acerca de
- manipulaciones, diferencias de gestos
- gestos, diferencias de manipulación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5368b39de1f35cc9a547bc240fc3c984fc1f10f658972b0f845a965e09bb29c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435990"
---
# <a name="manipulations"></a>Manipulaciones

En esta sección se explica la manipulación de objetos Windows Touch.

## <a name="manipulation-overview"></a>Información general sobre la manipulación

Una manera cómoda de pensar en las manipulaciones es considerarlas un superconjunto de gestos. Lo que puede hacer con gestos, puede hacerlo con más flexibilidad y precisión mediante manipulaciones. La diferencia entre manipulaciones y gestos se muestra mejor con un ejemplo sencillo. Puede expandir un objeto y, al mismo tiempo, traducirlo mediante manipulaciones; con gestos, solo se puede hacer de una en una. Esta capacidad de manipular un objeto en tiempo real hace que las aplicaciones sea más intuitivas para los usuarios al permitir una experiencia más realista.

Las API de manipulación se usan para simplificar las operaciones de transformación en objetos para aplicaciones táctiles. Las manipulaciones se realizan en Windows 7 a través del objeto COM manipulaciones. Mediante el uso de manipulaciones, los desarrolladores pueden admitir más fácilmente la inercia (física de objetos) y pueden realizar fácilmente transformaciones en objetos de una manera coherente con otras aplicaciones. En las secciones siguientes se explican varias maneras de realizar manipulaciones.



| Sección                                                                                            | Descripción                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Agregar compatibilidad con la manipulación al código no administrado](adding-manipulation-support-in-unmanaged-code.md) | Explica cómo implementar un receptor de eventos para la [**\_ interfaz IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) y agregar controladores de eventos al código. |
| [Manipulaciones avanzadas](advanced-manipulations.md)                                               | Explica cómo realizar manipulaciones complejas.                                                                                                       |
| [Rotación de un solo dedo](single-finger-rotation.md)                                               | Explica cómo girar un objeto mediante un punto de pivote y el procesador de manipulación.                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones e inercia](manipulation-and-inertia.md)
</dt> </dl>

 

 




