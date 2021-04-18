---
description: Use el operador ISA en la cláusula WHERE de una consulta de datos para solicitar objetos incrustados en una jerarquía de clases.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operador ISA para consultas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687989"
---
# <a name="isa-operator-for-data-queries"></a>Operador ISA para consultas de datos

Use el operador ISA en la cláusula WHERE de una consulta de datos para solicitar objetos incrustados en una jerarquía de clases.

En el ejemplo siguiente se muestra la sintaxis para solicitar objetos incrustados en una jerarquía de clases.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



El resultado incluye instancias de **clase** con objetos incrustados que se derivan de **ParentClass** en la propiedad **EmbeddedProp** . No todas las instancias del objeto de **clase** se derivan de **ParentClass**, pero el resultado devuelve los objetos incrustados que se derivan de **ParentClass**.

Por ejemplo, en la siguiente consulta, **ClassA** incluye la propiedad **EmbeddedObj** débilmente tipada. La clase **ClassA** tiene diez instancias. Cinco de esas instancias tienen objetos incrustados con un tipo derivado de **ClassZ**. Los otros cinco tienen objetos incrustados de otros tipos.

En el ejemplo siguiente se muestra la consulta que devuelve las cinco instancias, que incluyen los objetos que se derivan de **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



