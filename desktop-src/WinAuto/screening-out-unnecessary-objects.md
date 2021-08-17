---
title: Filtrado de objetos innecesarios
description: Si usa Inspeccionar para examinar un control simple, como un botón de inserción Aceptar en el accesorio de Microsoft WordPad, puede ver que estos objetos de ventana primarios también contienen varios objetos secundarios invisibles.
ms.assetid: 30884e11-cc73-4bb8-9d9e-b9f1b53c4193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c52dc54f2c32be3aff3e535427668943cf1ee21423636e3be8c018f6e3257b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745304"
---
# <a name="screening-out-unnecessary-objects"></a>Filtrado de objetos innecesarios

Si usa [Inspeccionar para](inspect-objects.md) examinar un control simple, como un botón de inserción Aceptar en el accesorio de Microsoft WordPad, puede ver que estos objetos de ventana primarios también contienen varios objetos secundarios invisibles. Estos objetos invisibles tienen el mismo nombre de clase de ventana que el control y tienen la [propiedad State](state-property.md) de STATE [**SYSTEM \_ \_ INVISIBLE.**](object-state-constants.md) En la tabla siguiente se enumeran los objetos secundarios invisibles Microsoft Active Accessibility crea para el control .



| Nombre          | Role                                                                  | ChildCount |
|---------------|-----------------------------------------------------------------------|------------|
| "System"      | [**BARRA \_ DE \_ MENÚS DEL SISTEMA DE ROLES**](object-roles.md)     | 0          |
| None          | [**ROLE \_ SYSTEM \_ TITLEBAR**](object-roles.md)   | 5          |
| "Aplicación" | [**BARRA \_ DE \_ MENÚS DEL SISTEMA DE ROLES**](object-roles.md)     | 0          |
| "Vertical"    | [**BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL**](object-roles.md) | 5          |
| "Horizontal"  | [**BARRA DE \_ DESPLAZAMIENTO DEL SISTEMA DE \_ ROL**](object-roles.md) | 5          |
| "Size Box"    | [**CONTROL \_ DEL SISTEMA DE \_ ROL**](object-roles.md)           | 0          |



 

Los desarrolladores de cliente deben identificar y filtrar estos objetos de ventana primarios y objetos secundarios invisibles porque no proporcionan información significativa a los usuarios finales.

 

 




