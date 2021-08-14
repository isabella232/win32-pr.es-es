---
title: Buscar objetos por nombre
description: La mayoría de los Active Directory Domain Services usan la propiedad cn como atributo de nomenclatura.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, buscar, por nombre
- object AD , buscando por nombre
- Buscar objetos por nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60624c62e9d28d35805af3c98f551a19f44edf9e27369cf7ded9e87621491cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189185"
---
# <a name="finding-objects-by-name"></a>Buscar objetos por nombre

La mayoría de los Active Directory Domain Services usan la **propiedad cn** como atributo de nomenclatura. Sin embargo, algunos objetos usan un atributo de nomenclatura distinto de **cn**. Por ejemplo, un controlador de dominio usa la propiedad **domainDNS** para el atributo de nomenclatura y una unidad organizativa usa la propiedad **organizationalUnit** para el atributo de nomenclatura. Para evitar tener que usar un atributo de nomenclatura diferente para distintos tipos de objeto, la propiedad **name,** que contiene el nombre distintivo relativo del objeto, debe usarse para buscar objetos por nombre.

## <a name="examples"></a>Ejemplos

En los ejemplos de código siguientes se muestran diferentes cadenas de consulta que se pueden usar para buscar objetos por nombre.

La siguiente cadena de consulta busca todos los objetos con un nombre que comienza por "Jeff".


```C++
(name=Jeff*)
```



La siguiente cadena de consulta busca todos los objetos de equipo con un nombre que comienza por "leased" o "corp".


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



La siguiente cadena de consulta busca todos los usuarios y con un nombre que comienza por "Jeff" o "Jeff".


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




