---
title: Definir un nuevo atributo
description: En este tema se muestra cómo definir un nuevo atributo al extender el esquema de Active Directory.
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- Definir un nuevo atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da1a0a003d92fe09f27043098cb1abc4387b81e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149183"
---
# <a name="defining-a-new-attribute"></a>Definir un nuevo atributo

En este tema se muestra cómo definir un nuevo atributo al extender el esquema de Active Directory.

Tenga en cuenta lo siguiente al definir un nuevo atributo:

-   Use los atributos existentes siempre que sea posible.
-   Use siempre la propiedad **CN** ("common name") como el atributo naming (nombre distintivo relativo). Este es el valor predeterminado para la mayoría de las clases, incluidas las derivadas directamente de Top. La propiedad **CN** es una propiedad indizada y hará que la búsqueda de objetos por nombre sea más eficaz.
-   Los atributos multivalor de gran tamaño son caros para almacenar y recuperar y deben evitarse. Active Directory Domain Services implementar una extensión LDAP para habilitar la lectura incremental de propiedades grandes con varios valores, pero no todos los clientes LDAP reconocerán esta extensión.
-   Recuerde que los atributos son planos, es decir, que no hay ninguna subestructura implícita a un atributo. Todos los atributos de una clase determinada deberían relacionarse directamente con las instancias de esa clase.

## <a name="creating-a-new-attribute"></a>Crear un nuevo atributo

Para crear un nuevo atributo:

-   Elija un nombre para el atributo. El nombre se incluirá en los atributos **CN** y **lDAPDisplayName** . Para obtener más información sobre cómo crear un nombre para un nuevo atributo, vea [asignar nombres a atributos y clases](naming-attributes-and-classes.md).
-   Obtener un identificador de objeto (OID) para el atributo. Para obtener más información, vea [obtener un identificador de objeto raíz](obtaining-an-object-identifier.md).
-   Elija una sintaxis para el atributo. La sintaxis viene determinada por la combinación de los atributos **oMSyntax** y **oMObjectClass** . Para obtener más información, vea [elegir una sintaxis](choosing-a-syntax.md).
-   Decida si el atributo es de un solo valor o de varios valores. El atributo **isSingleValued** determina si el atributo es de un solo valor o de varios valores.
-   Decida si se debe indizar el atributo de forma predeterminada. Para obtener más información, vea [atributos indexados](indexed-attributes.md).
-   Decida si el atributo debe estar en el catálogo global de forma predeterminada. Para obtener más información, vea [atributos incluidos en el catálogo global](attributes-included-in-the-global-catalog.md).
-   Si el atributo es un entero o una cadena, decida si es necesario un límite de intervalo. Los atributos **rangeLower** y **rangeUpper** se usan para especificar el límite de intervalo.
-   Si el atributo tiene valores DN, decida si el atributo debe vincularse con otro atributo. Si es así, el atributo [**LinkId**](/windows/desktop/ADSchema/a-linkid) debe establecerse correctamente en cada atributo; un atributo debe ser un vínculo hacia delante y el otro vínculo atrás. Para obtener más información sobre los atributos vinculados, vea [atributos vinculados](linked-attributes.md).
-   Cree un nuevo objeto **attributeSchema** en el contenedor de esquemas y establezca los atributos adecuados para el objeto. Hay un gran número de atributos que se pueden establecer para un objeto **attributeSchema** , pero los atributos que se enumeran en la siguiente tabla son fundamentales para la definición de un nuevo atributo. Los valores de estos atributos vienen determinados por los pasos anteriores. Para obtener más información sobre estos atributos, vea [características de los atributos](characteristics-of-attributes.md).

    | Atributo                                    | Comentario                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **CN**<br/>                            | Obligatorio.<br/>                                 |
    | **lDAPDisplayName**<br/>               | Obligatorio.<br/>                                 |
    | **adminDisplayName**<br/>              | Obligatorio.<br/>                                 |
    | **attributeSyntax**<br/>               | Obligatorio.<br/>                                 |
    | **oMSyntax**<br/>                      | Obligatorio.<br/>                                 |
    | **oMObjectClass**<br/>                 | Obligatorio.<br/>                                 |
    | **schemaIDGUID**<br/>                  | Obligatorio.<br/>                                 |
    | **attributeID**<br/>                   | Obligatorio.<br/>                                 |
    | **isSingleValued**<br/>                | Obligatorio.<br/>                                 |
    | **searchFlags**<br/>                   | Obligatorio.<br/>                                 |
    | **isMemberOfPartialAttributeSet**<br/> | Obligatorio.<br/>                                 |
    | **rangeLower**<br/>                    | Opcional.<br/>                                 |
    | **rangeUpper**<br/>                    | Opcional.<br/>                                 |
    | **linkID**<br/>                        | Opcional. Obligatorio para los atributos vinculados.<br/> |
    | **description**<br/>                   | Opcional.<br/>                                 |

    

     

-   Confirme el nuevo objeto **attributeSchema** en el contenedor de esquemas.
-   Actualice la caché de esquema, si es necesario. Para obtener más información, vea [actualizar la caché de esquema](updating-the-schema-cache.md).

 

