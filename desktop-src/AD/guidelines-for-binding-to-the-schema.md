---
title: Instrucciones para enlazar con el esquema
description: Hay dos maneras de enlazar con el esquema Active Directory enlazar directamente con el contenedor de esquema o con un objeto classSchema o attributeSchema en el contenedor de esquemas.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Directrices para enlazar con el esquema AD
- Esquema AD, enlace a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf246a4ea1ded5c7d80c52abb8ac9192182b3b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904495"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Instrucciones para enlazar con el esquema

Hay dos maneras de enlazar al esquema de Active Directory:

-   Enlazar directamente con el contenedor de esquema o con un objeto **ClassSchema** o **attributeSchema** en el contenedor de esquemas. Los objetos **ClassSchema** o **attributeSchema** contienen definiciones completas y formales de cada clase y atributo que pueden existir en un bosque de dominio de Active Directory. Para obtener más información, vea [leer objetos attributeSchema y ClassSchema](reading-attributeschema-and-classschema-objects.md).
-   Enlazar al esquema abstracto o a una entrada de clase o atributo en el esquema abstracto. El esquema abstracto solo contiene un subconjunto de los datos sobre cada clase y atributo, pero los datos están en un formato fácil de recuperar y usar. Para obtener más información, vea [el esquema abstracto](the-abstract-schema.md) y [la lectura del esquema abstracto](reading-the-abstract-schema.md).

Para modificar o extender el esquema, enlace directamente con el contenedor de esquemas. Para leer las definiciones de clase y atributo, normalmente es más fácil leer el esquema abstracto.

Es más fácil leer el esquema abstracto por los siguientes motivos:

-   ADSI proporciona técnicas de enlace especiales y un conjunto de interfaces para leer el esquema abstracto.
-   Las interfaces ADSI que funcionan con el esquema abstracto devuelven datos en un formato adecuado para su uso en otras interfaces ADSI. Por ejemplo, [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) y [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) normalmente usan cadenas **lDAPDisplayName** para informar de los nombres de atributo y de clase, aunque estos datos se almacenan en el directorio en forma de identificadores de objeto (OID). El formato **lDAPDisplayName** es práctico porque otras interfaces ADSI lo utilizan para hacer referencia a clases y atributos en los filtros de búsqueda y en cualquier otro lugar.
-   La entrada de esquema Abstract para una clase de objeto contiene datos recopilados de varios objetos **ClassSchema** . Por ejemplo, los posibles elementos primarios, los atributos obligatorios y los atributos opcionales de una clase de objeto son la Unión de estos atributos de las superclases de la clase y las clases auxiliares. Si lee el contenedor de esquemas real, debe recopilar datos de los distintos objetos **ClassSchema** de los que se deriva la clase. Si lee el esquema abstracto, los datos están en un solo lugar.

Debe enlazar directamente con el contenedor de esquemas en lugar de usar el esquema abstracto en los casos siguientes:

-   Para obtener atributos específicos que no se exponen en el esquema abstracto. Por ejemplo, **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** y otros atributos no se exponen en el esquema abstracto.
-   Para consultar los objetos **attributeSchema** y **ClassSchema** . Para buscar las clases o atributos que coinciden con un filtro especificado, enlace con el contenedor de esquema y realice una búsqueda de un solo nivel.
-   Para agregar o modificar atributos o clases. El esquema abstracto es de solo lectura; no se puede utilizar para modificar o extender el esquema. Tenga en cuenta que las modificaciones deben realizarse en el controlador de dominio que es el maestro de esquema. Para obtener más información, consulte [requisitos previos para la instalación de una extensión de esquema](prerequisites-for-installing-a-schema-extension.md).

 

 