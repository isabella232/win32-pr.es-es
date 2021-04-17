---
title: Detección de objetos innecesarios
description: Si usa inspeccionar para examinar un control simple, como un botón de presionado de aceptar en el accesorio de WordPad de Microsoft, puede ver que estos objetos de ventana primario también contienen varios objetos secundarios invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704587"
---
# <a name="screening-out-unnecessary-objects"></a>Detección de objetos innecesarios

Si usa [inspeccionar](inspect-objects.md) para examinar un control simple, como un botón de presionado de aceptar en el accesorio de WordPad de Microsoft, puede ver que estos objetos de ventana primario también contienen varios objetos secundarios invisibles. Estos objetos invisibles tienen el mismo nombre de clase de ventana que el control y tienen la [propiedad State](state-property.md) de [**State \_ System \_ invisible**](object-state-constants.md). En la tabla siguiente se enumeran los objetos secundarios invisibles que crea Microsoft Active Accessibility para el control.



| Nombre          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| Integrado      | [**\_barra de menús del sistema de roles \_**](object-roles.md)     | 0          |
| None          | [**\_TITLEBAR del sistema de roles \_**](object-roles.md)   | 5          |
| Aplicación | [**\_barra de menús del sistema de roles \_**](object-roles.md)     | 0          |
| Vertical    | [**\_barra de desplazamiento del sistema de roles \_**](object-roles.md) | 5          |
| Horizontal  | [**\_barra de desplazamiento del sistema de roles \_**](object-roles.md) | 5          |
| "Cuadro de tamaño"    | [**\_control del sistema de roles \_**](object-roles.md)           | 0          |



 

Los desarrolladores de cliente deben identificar y filtrar estos objetos de ventana primarios y los objetos secundarios invisibles, ya que no proporcionan información significativa a los usuarios finales.

 

 




