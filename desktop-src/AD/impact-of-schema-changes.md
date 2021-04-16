---
title: Impacto de los cambios de esquema
description: En este tema se describe cómo afecta una extensión de esquema al Active Directory bosque.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Impacto de los cambios de esquema en AD
- esquema AD, impacto de cambiar el esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45aa43ed208b6eca5889220e09c78e8ada4a50a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656229"
---
# <a name="impact-of-schema-changes"></a>Impacto de los cambios de esquema

Una extensión de esquema afecta a un bosque de dominio controlado por Active Directory Domain Services de varias maneras:

-   Los cambios de esquema son globales. Hay un único esquema para todo el bosque. El esquema se replica globalmente: existe una copia del esquema en todos los controladores de dominio del bosque. Al extender el esquema, se extiende para todo el bosque.
-   No se pueden revertir las adiciones de objeto de esquema. Cuando se agrega un nuevo objeto de clase o atributo al esquema, no se puede quitar. Un atributo o clase existente se puede deshabilitar, pero no se puede quitar. Para obtener más información, vea [deshabilitar clases y atributos existentes](disabling-existing-classes-and-attributes.md). Deshabilitar una clase o atributo no afecta a las instancias existentes de la clase o atributo, pero impide la creación de nuevas instancias. No se puede deshabilitar un atributo si está incluido en una clase que no está deshabilitada.
-   Los OID deben ser únicos. Cuando se agrega un atributo o una clase al esquema, no se puede agregar ningún atributo o clase con el mismo OID. Esto es así incluso si se ha deshabilitado una clase o un atributo. Por esta razón, es necesario usar OID válidos. No sintetiza un OID y no reutiliza un OID existente. Para obtener más información sobre cómo obtener un OID válido, vea [obtener un identificador de objeto raíz](obtaining-an-object-identifier.md).
-   Algunos cambios pueden realizarse después de la creación:

    -   En el caso de una clase de categoría 1 o categoría 2, puede Agregar o quitar valores en el atributo **possSuperiors** . Los valores de **possSuperiors** especifican las clases de objeto que pueden contener la clase.
    -   En el caso de una clase de categoría 1 o categoría 2, puede Agregar o quitar valores en el atributo **mayContain** . Los valores de **mayContain** especifican los atributos opcionales, pero pueden estar presentes en una instancia de la clase.

-   El **lDAPDisplayName** de una clase o atributo de categoría 2 se puede cambiar una vez creado. Normalmente, no debe cambiar el **lDAPDisplayName**. Sin embargo, hay una razón legítima para cambiar el nombre de LDAP y es si ha cometido un error al definir el atributo o la clase y debe crear uno nuevo para reemplazar el anterior. No es necesario cambiar el nombre del nombre distintivo relativo (RDN) del esquema de atributo o de clase para hacerlo. Cuando se cambia el nombre de LDAP, esto le permite solucionar un error en lugar de volver a generar toda la infraestructura de Windows 2000. Para obtener más información, vea [deshabilitar clases y atributos existentes](disabling-existing-classes-and-attributes.md).

    No se puede cambiar el **lDAPDisplayName** de las clases o atributos predefinidos (categoría 1). Para obtener más información sobre los objetos de esquema de categoría 1 y 2, consulte [restricciones de la extensión de esquema](restrictions-on-schema-extension.md).

 

 




