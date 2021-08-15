---
title: Clase de objeto y categoría de objeto
description: Cada instancia de una clase de objeto tiene una propiedad objectClass de varios valores que identifica la clase de la que el objeto es una instancia, así como todas las superclases estructurales o abstractas de las que se deriva esa clase.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35e7f461caa27e8668cfc47cd94852bf53b291658b828ea017e3dc00a19d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185702"
---
# <a name="object-class-and-object-category"></a>Clase de objeto y categoría de objeto

Cada instancia de una clase de objeto tiene una propiedad [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de varios valores que identifica la clase de la que el objeto es una instancia, así como todas las superclases estructurales o abstractas de las que se deriva esa clase. Por lo tanto, **la propiedad objectClass** de un objeto de usuario identificaría las clases [**de**](/windows/desktop/ADSchema/c-top)usuario , [**person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)y [**superiores.**](/windows/desktop/ADSchema/c-user) La **propiedad objectClass** no incluye clases auxiliares en la lista. El sistema establece el **valor objectClass** cuando se crea la instancia de objeto y no se puede cambiar.

Cada instancia de una clase de objeto también tiene una propiedad [**objectCategory,**](/windows/desktop/ADSchema/a-objectcategory) que es una propiedad de un solo valor que contiene el nombre distintivo de la clase de la que el objeto es una instancia o una de sus superclases. Cuando se crea un objeto , el sistema establece su **propiedad objectCategory** en el valor especificado por la [**propiedad defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de su clase de objeto. No se puede cambiar **la propiedad objectCategory de** un objeto.

Para obtener más información y un ejemplo de código que recupera la propiedad [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de un objeto, vea [Recuperar el atributo objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> Antes de Windows Server 2008, el [**atributo objectClass**](/windows/desktop/ADSchema/a-objectclass) no se indexa. Esto se debe a que tiene varios valores y es muy no único; es decir, cada instancia del atributo **objectClass** incluye la [**clase**](/windows/desktop/ADSchema/c-top) superior. Esto significa que un índice sería muy grande e ineficaz. Para buscar objetos de una clase determinada, use el atributo [**objectCategory,**](/windows/desktop/ADSchema/a-objectcategory) que es de un solo valor e indexado. Para obtener más información sobre el uso de estas propiedades en los filtros de búsqueda, vea [Decidir qué buscar.](deciding-what-to-find.md)

 

Para la mayoría de las clases, [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) es el nombre distintivo del objeto [**classSchema de la**](/windows/desktop/ADSchema/c-classschema) clase. Por ejemplo, **defaultObjectCategory** para la clase [**organizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit) es "CN=Organizational-Unit,CN=Schema,CN=Configuration,<DC=forestroot>". Sin embargo, algunas clases hacen referencia a otra clase como **defaultObjectCategory**. Esto permite que una consulta encuentre fácilmente grupos de objetos relacionados, incluso si son de clases diferentes. Por ejemplo, las clases [**de**](/windows/desktop/ADSchema/c-user)usuario , [**person**](/windows/desktop/ADSchema/c-person), [**organizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)y [**contact**](/windows/desktop/ADSchema/c-contact) identifican la **clase person** en sus **propiedades defaultObjectCategory.** Esto permite que filtros de búsqueda como (objectCategory=person) busquen instancias de todas estas clases con una sola consulta. Las consultas para personas son muy comunes, por lo que se trata de una optimización sencilla.

Si crea una subclase a partir de una clase estructural, el procedimiento recomendado es establecer el valor [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de la nueva clase en el mismo nombre distintivo de la superclase. Esto permite que la interfaz de usuario estándar "busque" la subclase.

 

 