---
title: Buscar objetos por nombre
description: La mayoría de los objetos de Active Directory Domain Services usar la propiedad CN como su atributo de nomenclatura.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, buscar por nombre
- objeto AD, buscar por nombre
- Buscar objetos por nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773153"
---
# <a name="finding-objects-by-name"></a>Buscar objetos por nombre

La mayoría de los objetos de Active Directory Domain Services usar la propiedad **CN** como su atributo de nomenclatura. Sin embargo, algunos objetos usan un atributo de nomenclatura distinto de **CN**. Por ejemplo, un controlador de dominio usa la propiedad **domainDNS** para el atributo de asignación de nombres y una unidad organizativa usa la propiedad **organizationalUnit** para el atributo de nomenclatura. Para evitar tener que usar un atributo de asignación de nombres diferente para los distintos tipos de objeto, la propiedad **Name** , que contiene el nombre distintivo relativo del objeto, debe usarse para buscar objetos por su nombre.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos de código se muestran cadenas de consulta diferentes que se pueden usar para buscar objetos por nombre.

La siguiente cadena de consulta busca todos los objetos cuyo nombre comienza por "Jeff".


```C++
(name=Jeff*)
```



La siguiente cadena de consulta busca todos los objetos de equipo cuyo nombre comienza por "concedido" o "Corp".


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



La siguiente cadena de consulta busca todos los usuarios y un nombre que comienza por "Karen" o "Jeff".


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




