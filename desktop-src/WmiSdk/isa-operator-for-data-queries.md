---
description: Use el operador ISA en la cláusula WHERE de una consulta de datos para solicitar objetos incrustados en una jerarquía de clases.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operador ISA para consultas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070454"
---
# <a name="isa-operator-for-data-queries"></a>Operador ISA para consultas de datos

Use el operador ISA en la cláusula WHERE de una consulta de datos para solicitar objetos incrustados en una jerarquía de clases.

En el ejemplo siguiente se muestra la sintaxis para solicitar objetos incrustados en una jerarquía de clases.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



El resultado incluye instancias de **Class que** tienen objetos incrustados que se derivan de **ParentClass** en la **propiedad EmbeddedProp.** No todas las instancias del **objeto Class** se derivan de **ParentClass**, pero el resultado devuelve los objetos incrustados que se derivan de **ParentClass**.

Por ejemplo, en la consulta siguiente, **ClassA** incluye la propiedad **EmbeddedObj** débilmente con tipo. La **clase ClassA** tiene diez instancias. Cinco de esas instancias tienen objetos incrustados con un tipo derivado de **ClassZ.** Los otros cinco tienen objetos incrustados de otros tipos.

En el ejemplo siguiente se muestra la consulta que devuelve las cinco instancias de , que incluyen los objetos derivados de **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



