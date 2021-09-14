---
title: Filtrado de objetos innecesarios
description: Si usa Inspeccionar para examinar un control simple, como un botón de inserción Aceptar en el accesorios de Microsoft WordPad, puede ver que estos objetos de ventana primarios también contienen varios objetos secundarios invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb341881ee2ea503b1f74643723a1f90c8e5d1d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070638"
---
# <a name="screening-out-unnecessary-objects"></a>Filtrado de objetos innecesarios

Si usa [Inspeccionar para](inspect-objects.md) examinar un control simple, como un botón de inserción Aceptar en el accesorios de Microsoft WordPad, puede ver que estos objetos de ventana primarios también contienen varios objetos secundarios invisibles. Estos objetos invisibles tienen el mismo nombre de clase de ventana que el control y tienen la propiedad [State](state-property.md) de [**STATE SYSTEM \_ \_ INVISIBLE.**](object-state-constants.md) En la tabla siguiente se enumeran los objetos secundarios invisibles Microsoft Active Accessibility crea para el control .



| Nombre          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| "System"      | [**BARRA \_ DE \_ MENÚS DEL SISTEMA DE ROLES**](object-roles.md)     | 0          |
| None          | [**BARRA \_ DE TÍTULO DEL SISTEMA DE \_ ROLES**](object-roles.md)   | 5          |
| "Aplicación" | [**BARRA \_ DE \_ MENÚS DEL SISTEMA DE ROLES**](object-roles.md)     | 0          |
| "Vertical"    | [**BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL**](object-roles.md) | 5          |
| "Horizontal"  | [**BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL**](object-roles.md) | 5          |
| "Cuadro de tamaño"    | [**CONTROL \_ DEL SISTEMA DE \_ ROL**](object-roles.md)           | 0          |



 

Los desarrolladores de cliente deben identificar y filtrar estos objetos de ventana primarios y objetos secundarios invisibles porque no proporcionan información significativa a los usuarios finales.

 

 




