---
title: Definir un nuevo atributo
description: En este tema se muestra cómo definir un nuevo atributo al extender el Active Directory esquema.
ms.assetid: b8ac69ba-3b75-4e55-bf80-dabf2e80288a
ms.tgt_platform: multiple
keywords:
- Definición de un nuevo atributo de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd143917844e071a1b54d0c5f4d22e2d0dce8bcc2b24c163d50babf18eb40a56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019859"
---
# <a name="defining-a-new-attribute"></a>Definir un nuevo atributo

En este tema se muestra cómo definir un nuevo atributo al extender el Active Directory esquema.

Tenga en cuenta lo siguiente al definir un nuevo atributo:

-   Use atributos existentes cuando sea posible.
-   Use siempre la **propiedad cn** ("nombre común") como atributo de nomenclatura (nombre distintivo relativo). Este es el valor predeterminado para la mayoría de las clases, incluidas las derivadas directamente de Top. La **propiedad cn** es una propiedad indizada y hará que la búsqueda de objetos por nombre sea más eficaz.
-   Los atributos multivalor grandes son costosos de almacenar y recuperar, y se deben evitar. Active Directory Domain Services una extensión LDAP para habilitar la lectura incremental de propiedades grandes con varios valores, pero no todos los clientes LDAP reconocerán esta extensión.
-   Recuerde que los atributos son planos, es decir, no hay ninguna subestructura implícita para un atributo. Todos los atributos de una clase determinada deben relacionarse directamente con las instancias de esa clase.

## <a name="creating-a-new-attribute"></a>Crear un nuevo atributo

Para crear un nuevo atributo:

-   Elija un nombre para el atributo. El nombre se incluirá en los **atributos cn** y **lDAPDisplayName.** Para obtener más información sobre cómo crear un nombre para un nuevo atributo, vea Asignar nombres a [atributos y clases.](naming-attributes-and-classes.md)
-   Obtenga un identificador de objeto (OID) para el atributo. Para obtener más información, [vea Obtener un identificador de objeto raíz](obtaining-an-object-identifier.md).
-   Elija una sintaxis para el atributo. La sintaxis viene determinada por la combinación de los **atributos oMSyntax** **y oMObjectClass.** Para obtener más información, vea [Elegir una sintaxis.](choosing-a-syntax.md)
-   Decida si el atributo es de uno o varios valores. El **atributo isSingleValued** determina si el atributo es único o multivalor.
-   Decida si el atributo se debe indexar de forma predeterminada. Para obtener más información, vea [Atributos indizados.](indexed-attributes.md)
-   Decida si el atributo debe estar en el catálogo global de forma predeterminada. Para obtener más información, vea [Atributos incluidos en el catálogo global.](attributes-included-in-the-global-catalog.md)
-   Si el atributo es un entero o una cadena, decida si se requiere un límite de intervalo. Los **atributos rangeLower** **y rangeUpper** se usan para especificar el límite de intervalo.
-   Si el atributo tiene valores DN, decida si el atributo debe vincularse a otro atributo. Si es así, [**el atributo linkID**](/windows/desktop/ADSchema/a-linkid) debe establecerse correctamente en cada atributo; un atributo debe ser un vínculo hacia delante y el otro un vínculo hacia atrás. Para obtener más información sobre los atributos vinculados, vea [Atributos vinculados.](linked-attributes.md)
-   Cree un nuevo **objeto attributeSchema** en el contenedor de esquemas y establezca los atributos adecuados para el objeto. Hay un gran número de atributos que se pueden establecer para un objeto **attributeSchema,** pero los atributos enumerados en la tabla siguiente son fundamentales para la definición de un nuevo atributo. Los valores de estos atributos están determinados por los pasos anteriores. Para obtener más información sobre estos atributos, vea [Características de los atributos](characteristics-of-attributes.md).

    | Atributo                                    | Comentario                                              |
    |----------------------------------------------|------------------------------------------------------|
    | **Cn**<br/>                            | Obligatorio.<br/>                                 |
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
    | **linkID**<br/>                        | Opcional. Se requiere para los atributos vinculados.<br/> |
    | **description**<br/>                   | Opcional.<br/>                                 |

    

     

-   Confirme el nuevo **objeto attributeSchema** en el contenedor de esquemas.
-   Actualice la caché del esquema, si es necesario. Para obtener más información, vea [Actualización de la caché de esquemas.](updating-the-schema-cache.md)

 

