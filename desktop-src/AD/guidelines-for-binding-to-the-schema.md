---
title: Directrices para enlazar al esquema
description: Hay dos maneras de enlazar al Active Directory enlace directamente al contenedor de esquema o a un objeto classSchema o attributeSchema en el contenedor de esquema.
ms.assetid: 8c10415e-136c-476c-993c-b6dc459b5bf4
ms.tgt_platform: multiple
keywords:
- Directrices para el enlace al ad de esquema
- Schema AD , Enlace a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1492814bbce4b359a16c10f1d92340ae06d0f3c58177cd125a0b0c861f32f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188689"
---
# <a name="guidelines-for-binding-to-the-schema"></a>Directrices para enlazar al esquema

Hay dos maneras de enlazar al Active Directory esquema:

-   Enlace directamente al contenedor de esquema o a un **objeto classSchema** **o attributeSchema** en el contenedor de esquema. Los **objetos classSchema** **o attributeSchema** contienen definiciones completas y formales de cada clase y atributo que pueden existir en un Dominio de Active Directory bosque. Para obtener más información, vea [Lectura de attributeSchema y classSchema Objects](reading-attributeschema-and-classschema-objects.md).
-   Enlace al esquema abstracto o a una entrada de clase o atributo en el esquema abstracto. El esquema abstracto contiene solo un subconjunto de los datos sobre cada clase y atributo, pero los datos están en un formato que es fácil de recuperar y usar. Para obtener más información, [vea El esquema abstracto y](the-abstract-schema.md) Leer el esquema [abstracto](reading-the-abstract-schema.md).

Para modificar o ampliar el esquema, enlace directamente al contenedor de esquema. Para leer las definiciones de clase y atributo, suele ser más fácil leer desde el esquema abstracto.

Es más fácil leer del esquema abstracto por los siguientes motivos:

-   ADSI proporciona técnicas de enlace especiales y un conjunto de interfaces para leer el esquema abstracto.
-   Las interfaces ADSI que funcionan con el esquema abstracto devuelven datos en un formato adecuado para su uso en otras interfaces ADSI. Por ejemplo, [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) e [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) suelen usar cadenas **lDAPDisplayName** para notificar nombres de clase y atributo, aunque estos datos se almacenen en el directorio en forma de identificadores de objeto (ID). El **formato lDAPDisplayName** es práctico porque otras interfaces ADSI lo usan para hacer referencia a clases y atributos en filtros de búsqueda y en otras partes.
-   La entrada de esquema abstracto de una clase de objeto contiene datos recopilados de varios **objetos classSchema.** Por ejemplo, los posibles elementos primarios, los atributos obligatorios y los atributos opcionales para una clase de objeto son la unión de estos atributos de las superclases y clases auxiliares de la clase. Si lee desde el contenedor de esquema real, debe recopilar datos de los distintos **objetos classSchema** de los que se derivó la clase. Si lee desde el esquema abstracto, los datos están en un solo lugar.

Debe enlazar directamente al contenedor de esquemas en lugar de usar el esquema abstracto en los casos siguientes:

-   Para obtener atributos específicos que no se exponen en el esquema abstracto. Por ejemplo, **oMSyntax**, **attributeSchema**, **defaultSecurityDescriptor** y otros atributos no se exponen en el esquema abstracto.
-   Para consultar objetos **attributeSchema** **y classSchema.** Para buscar clases o atributos que coincidan con un filtro especificado, enlace al contenedor de esquema y realice una búsqueda de un nivel.
-   Para agregar o modificar atributos o clases. El esquema abstracto es de solo lectura; no se puede usar para modificar o ampliar el esquema. Tenga en cuenta que se deben realizar modificaciones en el controlador de dominio que es el maestro de esquema. Para obtener más información, vea [Requisitos previos para instalar una extensión de esquema.](prerequisites-for-installing-a-schema-extension.md)

 

 