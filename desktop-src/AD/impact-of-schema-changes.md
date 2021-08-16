---
title: Impacto de los cambios de esquema
description: En este tema se describe cómo afecta una extensión de esquema a Active Directory bosque.
ms.assetid: df604fb4-9256-4028-86d3-4ae1bc680324
ms.tgt_platform: multiple
keywords:
- Impacto de los cambios de esquema de AD
- schema AD , impacto de cambiar el esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa9cc0ee4cdcd0da3581d6bf009837799387949e43dc68989612442352df591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187724"
---
# <a name="impact-of-schema-changes"></a>Impacto de los cambios de esquema

Una extensión de esquema afecta a un bosque de dominio controlado por Active Directory Domain Services de varias maneras:

-   Los cambios de esquema son globales. Hay un único esquema para todo un bosque. El esquema se replica globalmente: existe una copia del esquema en cada controlador de dominio del bosque. Al extender el esquema, se extiende para todo el bosque.
-   Las adiciones de objetos de esquema no se pueden invertir. Cuando se agrega una nueva clase o un objeto de atributo al esquema, no se puede quitar. Se puede deshabilitar un atributo o una clase existentes, pero no quitarse. Para obtener más información, [vea Deshabilitar clases y atributos existentes.](disabling-existing-classes-and-attributes.md) Deshabilitar una clase o atributo no afecta a las instancias existentes de la clase o atributo, pero impide la creación de nuevas instancias. No se puede deshabilitar un atributo si se incluye en cualquier clase que no esté deshabilitada.
-   Los IDENTIFICADORES deben ser únicos. Cuando se agrega un atributo o una clase al esquema, no se puede agregar ningún atributo o clase con el mismo OID. Esto es así incluso si se ha deshabilitado una clase o atributo. Por esta razón, debe usar identificadores ÓID válidos. No sintete un OID y no reutilice un OID existente. Para obtener más información sobre cómo obtener un OID válido, vea [Obtener un identificador de objeto raíz](obtaining-an-object-identifier.md).
-   Se pueden realizar algunos cambios después de la creación:

    -   Para una clase de categoría 1 o categoría 2, puede agregar o quitar valores en el **atributo possSuperiors.** Los **valores possSuperiors** especifican las clases de objeto que pueden contener la clase .
    -   Para una clase de categoría 1 o categoría 2, puede agregar o quitar valores en el **atributo mayContain.** Los **valores mayContain** especifican los atributos opcionales, pero pueden estar presentes en una instancia de la clase .

-   El **valor lDAPDisplayName de** una clase o atributo de categoría 2 se puede cambiar una vez creado. Normalmente, no debe cambiar **lDAPDisplayName**. Sin embargo, hay una razón legítima para cambiar el nombre LDAP y es si ha cometido un error al definir el atributo o la clase y debe crear uno nuevo para reemplazar el antiguo. Para ello, no es necesario cambiar el nombre distintivo relativo (RDN) del atributo o esquema de clase. Cuando se cambia el nombre LDAP, esto le permite evitar un error en lugar de recompilar toda la infraestructura Windows 2000. Para obtener más información, [vea Deshabilitar clases y atributos existentes.](disabling-existing-classes-and-attributes.md)

    No **se puede cambiar lDAPDisplayName** para clases o atributos predefinidos (categoría 1). Para obtener más información sobre los objetos de esquema de categoría 1 y 2, vea [Restricciones en la extensión de esquema](restrictions-on-schema-extension.md).

 

 




