---
description: ACE para controlar el acceso a las propiedades de objetos
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE para controlar el acceso a las propiedades de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073733"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>ACE para controlar el acceso a las propiedades de un objeto

La [*lista de control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) de un objeto de servicio de directorio (DS) puede contener una jerarquía de entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE), como se muestra a continuación:

1.  ACE que protegen el propio objeto
2.  [ACE específicas del objeto](object-specific-aces.md) que protegen un conjunto de propiedades especificado en el objeto
3.  ACE específicas del objeto que protegen una propiedad especificada en el objeto

Dentro de esta jerarquía, los derechos concedidos o denegados en un nivel superior se aplican también a los niveles inferiores. Por ejemplo, si una ACE específica del objeto en un conjunto de propiedades permite a un administrador de confianza el derecho \_ ADS RIGHT DS READ PROP, el administrador de confianza tiene acceso de lectura implícito a todas las propiedades de ese conjunto \_ \_ de \_ propiedades. De forma similar, una ACE en el propio objeto que permite el acceso ADS RIGHT DS READ PROP proporciona al administrador de confianza acceso de lectura a todas las propiedades \_ \_ del \_ \_ objeto.

En la ilustración siguiente se muestra el árbol de un objeto DS hipotético y sus propiedades y conjuntos de propiedades.

![jerarquía de objetos de servicio de directorio](images/accctrl2.png)

Supongamos que desea permitir el acceso siguiente a las propiedades de este objeto DS:

-   Permitir el permiso de lectura y escritura del grupo A para todas las propiedades del objeto
-   Permitir a todos los demás permisos de lectura y escritura para todas las propiedades, excepto la propiedad D

Para ello, establezca las ACE en la DACL del objeto como se muestra en la tabla siguiente.



| Fideicomisario  | GUID de objeto    | Tipo ace                  | Derechos de acceso                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Grupo A  | None           | ACE con acceso permitido        | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| Todos | Conjunto de propiedades 1 | ACE de objeto con acceso permitido | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |
| Todos | Propiedad C     | ACE de objeto con acceso permitido | ADS \_ RIGHT \_ DS \_ READ \_ PROP \| ADS \_ RIGHT \_ DS \_ WRITE \_ PROP |



 

La ACE del grupo A no tiene un GUID de objeto, lo que significa que permite el acceso a todas las propiedades del objeto. La ACE específica del objeto para el conjunto de propiedades 1 permite a todos acceder a las propiedades A y B. La otra ACE específica del objeto permite que todos los usuarios accedan a la propiedad C. Tenga en cuenta que, aunque esta DACL no tiene ninguna ACE con acceso denegado, deniega implícitamente el acceso de la propiedad D a todos los usuarios excepto el grupo A.

Cuando un usuario intenta acceder a la propiedad de un objeto, el sistema comprueba las ACE, en orden, hasta que el acceso solicitado se concede explícitamente, se deniega o no hay más ACE, en cuyo caso el acceso se deniega implícitamente.

El sistema evalúa:

-   ACE que se aplican al propio objeto
-   ACE específicas del objeto que se aplican al conjunto de propiedades que contiene la propiedad a la que se tiene acceso
-   ACE específicas del objeto que se aplican a la propiedad a la que se accede

El sistema omite las ACE específicas del objeto que se aplican a otros conjuntos de propiedades o propiedades.

 

 
