---
title: Consulta de objetos de esquema de categoría 1 o 2
description: El atributo systemFlags de los objetos attributeSchema y classSchema es una máscara de máscara de entero que contiene marcas que indican cualidades del sistema adicionales del atributo o la clase.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Consulta de la categoría 1 o 2 objetos de esquema AD
- objeto AD, consulta de objetos de esquema de categoría 1 o 2
- esquema AD, consulta de objetos de esquema de categoría 1 o 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358802"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Consulta de objetos de esquema de categoría 1 o 2

El atributo **systemFlags** de los objetos **attributeSchema** y **ClassSchema** es una máscara de máscara de entero que contiene marcas que indican cualidades del sistema adicionales del atributo o la clase. La enumeración de [**\_ \_ enumeración SYSTEMFLAG de ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contiene valores que se corresponden con los bits que se pueden establecer en el atributo **systemFlags** . Hay bits de **systemFlags** adicionales que no se pueden establecer, como el bit 0x10, que indica si el atributo o la clase es la categoría 1 o la categoría 2. El bit 0x10 se establece para objetos de categoría 1, que son las clases y los atributos incluidos en el esquema base incluido con el sistema. El bit no está establecido para los atributos y las clases de la categoría 2, que son extensiones del esquema. Si no existe ninguna propiedad **systemFlags** en un objeto **attributeSchema** o **ClassSchema** , es la categoría 2.

El **bit de la \_ regla de coincidencia LDAP \_ \_ \_ y** la regla de coincidencia se pueden usar para buscar objetos que tengan la marca 0x10 establecida en el atributo **systemFlags** . Para obtener más información, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).

## <a name="querying-for-category-1"></a>Consulta de categoría 1

La siguiente cadena de consulta busca atributos de categoría 1 (objetos **attributeSchema** con el bit 0x10 establecido en la propiedad **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Tenga en cuenta que, en el ejemplo anterior, la sintaxis de consulta LDAP requiere valores decimales; por lo tanto, el valor hexadecimal de la marca se debe convertir a decimal. En este caso, la categoría 1 bit es 0x10, por lo que el valor de filtro debe especificarse como 16.

## <a name="querying-for-category-2"></a>Consulta de la categoría 2

La siguiente cadena de consulta busca los atributos de categoría 2 (objetos **attributeSchema** que no tienen el bit 0x10 establecido en la propiedad **systemFlags** ).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Tenga en cuenta que esta consulta también devuelve objetos **attributeSchema** que no tienen una propiedad **systemFlags** y, por lo tanto, no tienen el marcador especificado establecido implícitamente.

 

 