---
description: ACE para controlar el acceso a las propiedades de los objetos
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE para controlar el acceso a las propiedades de los objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276498"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACE para controlar el acceso a las propiedades de un objeto

La [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto de servicio de directorio (DS) puede contener una jerarquía de [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE), como se indica a continuación:

1.  ACE que protegen el propio objeto
2.  [ACE específicas del objeto](object-specific-aces.md) que protegen un conjunto de propiedades especificado en el objeto.
3.  ACE específicas del objeto que protegen una propiedad especificada en el objeto.

Dentro de esta jerarquía, los derechos concedidos o denegados en un nivel superior se aplican también a los niveles inferiores. Por ejemplo, si una ACE específica del objeto en un conjunto de propiedades permite que un administrador de confianza sea el derecho \_ \_ DS \_ Read \_ prop Right, el administrador de confianza tendrá acceso de lectura implícito a todas las propiedades de ese conjunto de propiedades. Del mismo modo, una ACE en el propio objeto que permite \_ a ADS tener el derecho de \_ \_ lectura de DS read \_ prop proporciona acceso de lectura a todas las propiedades del objeto.

En la ilustración siguiente se muestra el árbol de un objeto DS hipotético y sus propiedades y conjuntos de propiedades.

![jerarquía de objetos del servicio de directorio](images/accctrl2.png)

Supongamos que desea permitir el siguiente acceso a las propiedades de este objeto DS:

-   Permitir al grupo un permiso de lectura y escritura para todas las propiedades del objeto
-   Permitir a todos los demás permisos de lectura y escritura para todas las propiedades excepto la propiedad D

Para ello, establezca las ACE en la DACL del objeto como se muestra en la tabla siguiente.



| Confianza  | GUID del objeto    | Tipo de ACE                  | Derechos de acceso                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Grupo A  | None           | ACE de acceso permitido        | ADS \_ right \_ DS \_ leer \_ prop \| ADS \_ right \_ DS \_ Write \_ prop |
| Todos | Conjunto de propiedades 1 | ACE de objeto con permiso de acceso | ADS \_ right \_ DS \_ leer \_ prop \| ADS \_ right \_ DS \_ Write \_ prop |
| Todos | Propiedad C     | ACE de objeto con permiso de acceso | ADS \_ right \_ DS \_ leer \_ prop \| ADS \_ right \_ DS \_ Write \_ prop |



 

La ACE del grupo A no tiene un GUID de objeto, lo que significa que permite el acceso a todas las propiedades del objeto. La ACE específica del objeto para el conjunto de propiedades 1 permite que todos los usuarios tengan acceso a las propiedades a y B. La otra ACE específica del objeto permite que todos los usuarios tengan acceso a la propiedad C. tenga en cuenta que aunque esta DACL no tiene ninguna ACE de acceso denegado, deniega implícitamente el acceso de la propiedad D a todos los usuarios excepto el grupo A.

Cuando un usuario intenta tener acceso a la propiedad de un objeto, el sistema comprueba las ACE, en orden, hasta que el acceso solicitado se concede, se deniega explícitamente o no hay más ACE, en cuyo caso se deniega implícitamente el acceso.

El sistema evalúa:

-   ACE que se aplican al propio objeto
-   ACE específicas del objeto que se aplican al conjunto de propiedades que contiene la propiedad a la que se obtiene acceso.
-   ACE específicas del objeto que se aplican a la propiedad a la que se obtiene acceso.

El sistema omite las ACE específicas del objeto que se aplican a otros conjuntos de propiedades o propiedades.

 

 
