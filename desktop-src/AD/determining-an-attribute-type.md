---
title: Determinar un tipo de atributo
description: El atributo systemFlags de un objeto attributeSchema contiene un conjunto de marcas que indican varias cualidades del objeto de atributo, como, por ejemplo, si el atributo está construido o no replicado.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Determinar un tipo de atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077530"
---
# <a name="determining-an-attribute-type"></a>Determinar un tipo de atributo

El atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) de un objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contiene un conjunto de marcas que indican varias cualidades del objeto de atributo, como, por ejemplo, si el atributo está construido o no replicado. En la tabla siguiente se enumeran las marcas del atributo **systemFlags** que afectan al tipo de almacenamiento del atributo. 

| Valor de marca | Descripción                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | Si esta marca está presente en el atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , el atributo no se replica. |
| 0x00000004 | Si esta marca está presente en el atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , se construye el atributo.    |



 

Es posible construir una cadena de consulta que se puede usar para consultar atributos construidos o no replicados. Por ejemplo, la siguiente cadena de consulta busca todos los objetos [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) no replicados. Tenga en cuenta que la cadena de consulta requiere el equivalente decimal del valor, no el equivalente hexadecimal del valor. Para obtener más información sobre el OID de la regla de coincidencia que usa esta cadena de consulta, vea [Cómo especificar valores de comparación](how-to-specify-comparison-values.md).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



El atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) del objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define si un atributo está indizado; un atributo indexado tiene un valor de 1, un atributo no indizado tiene un valor de 0. Por ejemplo, la siguiente cadena de consulta busca los objetos **attributeSchema** que representan atributos indexados.


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



El atributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) del objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define si un atributo se replica en el catálogo global. Este atributo tiene un valor **true** si el atributo es un miembro del catálogo global o **false** si los atributos no están en el catálogo global. Por ejemplo, la siguiente cadena de consulta busca los objetos **attributeSchema** que se replican en el catálogo global.


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 