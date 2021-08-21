---
title: Consulta de objetos de esquema de categoría 1 o 2
description: El atributo systemFlags de los objetos attributeSchema y classSchema es una máscara de bits de enteros que contiene marcas que indican calidades del sistema adicionales del atributo o la clase.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Consultar objetos de esquema ad de categoría 1 o 2
- objeto AD, consultando objetos de esquema de categoría 1 o 2
- schema AD , consultando objetos de esquema de categoría 1 o 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f934ba0401c7d782706e1e853819ba935c1315a267c668614878ec41045f63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025353"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Consulta de objetos de esquema de categoría 1 o 2

El **atributo systemFlags** de los objetos **attributeSchema** y **classSchema** es una máscara de bits de enteros que contiene marcas que indican calidades del sistema adicionales del atributo o la clase. La [**\_ enumeración SYSTEMFLAG \_ ENUM de ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contiene valores que corresponden a los bits que se pueden establecer en el atributo **systemFlags.** Hay bits **systemFlags** adicionales que no se pueden establecer, como el bit 0x10 que indica si el atributo o la clase es de categoría 1 o categoría 2. El 0x10 se establece para objetos de categoría 1, que son las clases y atributos incluidos en el esquema base incluido con el sistema. El bit no se establece para clases y atributos de categoría 2, que son extensiones del esquema. Si no **existe ninguna propiedad systemFlags** en un **objeto attributeSchema** o **classSchema,** es la categoría 2.

La regla de coincidencia BIT AND de **LDAP \_ MATCHING \_ RULE \_ \_** se puede usar para buscar objetos que tengan la marca 0x10 establecida en el **atributo systemFlags.** Para obtener más información, vea [Sintaxis de filtro de búsqueda.](/windows/desktop/ADSI/search-filter-syntax)

## <a name="querying-for-category-1"></a>Consulta de la categoría 1

La siguiente cadena de consulta busca atributos de categoría 1 **(objetos attributeSchema** con el 0x10 de bits establecido en **la propiedad systemFlags).**


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Tenga en cuenta que, en el ejemplo anterior, la sintaxis de consulta LDAP requiere valores decimales; por lo tanto, el valor hexadecimal de la marca debe convertirse en decimal. En este caso, la categoría 1 bit 0x10, por lo que el valor del filtro debe especificarse como 16.

## <a name="querying-for-category-2"></a>Consulta de la categoría 2

La siguiente cadena de consulta busca atributos de categoría 2 **(objetos attributeSchema** que no tienen el valor de 0x10 bit establecido en la **propiedad systemFlags).**


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Tenga en cuenta que esta consulta también devuelve objetos **attributeSchema** que no tienen una propiedad **systemFlags** y, por lo tanto, implícitamente no tienen establecida la marca especificada.

 

 