---
title: Clase de objeto y categoría de objeto
description: Cada instancia de una clase de objeto tiene una propiedad objectClass con varios valores que identifica la clase de la que el objeto es una instancia, así como todas las superclases estructurales o abstractas de las que se deriva esa clase.
ms.assetid: b3c5f9ee-98e0-42dd-9b61-3731e14b9cd4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74941b4f32cc197d3dbbf3aa0dc3179b4098ee8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995067"
---
# <a name="object-class-and-object-category"></a>Clase de objeto y categoría de objeto

Cada instancia de una clase de objeto tiene una propiedad [**objectClass**](/windows/desktop/ADSchema/a-objectclass) con varios valores que identifica la clase de la que el objeto es una instancia, así como todas las superclases estructurales o abstractas de las que se deriva esa clase. Por lo tanto, la propiedad **objectClass** de un objeto User identificaría las clases [**Top**](/windows/desktop/ADSchema/c-top), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)y [**User**](/windows/desktop/ADSchema/c-user) . La propiedad **objectClass** no incluye las clases auxiliares en la lista. El sistema establece el valor de **objectClass** cuando se crea la instancia de objeto y no se puede cambiar.

Cada instancia de una clase de objeto también tiene una propiedad [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , que es una propiedad de un solo valor que contiene el nombre distintivo de la clase de la que el objeto es una instancia o de una de sus superclases. Cuando se crea un objeto, el sistema establece su propiedad **objectCategory** en el valor especificado por la propiedad [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de su clase de objeto. No se puede cambiar la propiedad **objectCategory** de un objeto.

Para obtener más información y un ejemplo de código que recupera la propiedad [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de un objeto, vea [recuperar el atributo objectClass](retrieving-the-objectclass-property.md).

> [!IMPORTANT]
> Antes de Windows Server 2008, el atributo [**objectClass**](/windows/desktop/ADSchema/a-objectclass) no está indizado. Esto se debe a que tiene varios valores y es muy no único; es decir, cada instancia del atributo **objectClass** incluye la clase [**Top**](/windows/desktop/ADSchema/c-top) . Esto significa que un índice sería muy grande e ineficaz. Para buscar objetos de una clase determinada, use el atributo [**objectCategory**](/windows/desktop/ADSchema/a-objectcategory) , que tiene un solo valor e indexado. Para obtener más información sobre el uso de estas propiedades en los filtros de búsqueda, consulte [decidir qué buscar](deciding-what-to-find.md).

 

Para la mayoría de las clases, [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) es el nombre distintivo del objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) de la clase. Por ejemplo, el **defaultObjectCategory** de la clase [**ORGANIZATIONALUNIT**](/windows/desktop/ADSchema/c-organizationalunit) es "CN = Organization-Unit, CN = Schema, cn = Configuration, <DC = forestroot>". Sin embargo, algunas clases hacen referencia a otra clase como **defaultObjectCategory**. Esto permite que una consulta encuentre fácilmente grupos de objetos relacionados, incluso si son de clases diferentes. Por ejemplo, las clases [**User**](/windows/desktop/ADSchema/c-user), [**Person**](/windows/desktop/ADSchema/c-person), [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson)y [**Contact**](/windows/desktop/ADSchema/c-contact) identifican la clase **Person** en sus propiedades **defaultObjectCategory** . Esto permite que los filtros de búsqueda como (objectCategory = person) busquen instancias de todas estas clases con una sola consulta. Las consultas para personas son muy comunes, por lo que se trata de una optimización simple.

Si crea una subclase a partir de una clase estructural, el procedimiento recomendado consiste en establecer el valor [**defaultObjectCategory**](/windows/desktop/ADSchema/a-defaultobjectcategory) de la nueva clase en el mismo nombre distintivo de la superclase. Esto permite a la interfaz de usuario estándar "Buscar" la subclase.

 

 