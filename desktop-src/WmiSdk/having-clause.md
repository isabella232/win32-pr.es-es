---
description: La cláusula HAVING se utiliza para filtrar los eventos que se reciben durante el intervalo de agrupación especificado en la cláusula WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Cláusula HAVING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707213"
---
# <a name="having-clause"></a>Cláusula HAVING

La cláusula HAVING se utiliza para filtrar los eventos que se reciben durante el intervalo de agrupación especificado en la [cláusula Within](within-clause.md). Por ejemplo, una instrucción SELECT podría construirse para que no devuelva nada a menos que haya al menos 5 eventos en el intervalo de los últimos 30 segundos.

La cláusula WITHIN sigue inmediatamente en la [instrucción SELECT](select-statement-for-event-queries.md) después de la cláusula [Group](group-clause.md) . La cláusula HAVING funciona en la propiedad **NumberOfEvents** de la clase del sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) , de la que el grupo creado por la cláusula Group es un miembro. La cláusula HAVING puede utilizar todos los operadores relacionales estándar.

La sintaxis es la siguiente:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

El valor de *EventClass* es la clase de eventos de la que el evento es un miembro y *Value* es el valor de la propiedad en la que se requiere la notificación. El intervalo es un entero sin signo que representa el intervalo de agrupación (en segundos) después de recibir el primer evento. La lista de propiedades es una lista delimitada por comas de una o varias propiedades que se incluyen en la clase de eventos. El operador es cualquier operador relacional. El valor constante es cualquier entero de 32 bits sin signo que indique el número de eventos utilizados para filtrar.

Cuando se usa la cláusula HAVING, las cláusulas WHERE y BY son opcionales.

La siguiente consulta de eventos solicita que las notificaciones de la clase **EmailEvent** se agrupen en un evento 300 segundos después del primer evento que recibe WMI. Además, la consulta solicita que la instancia de [**\_ \_ AggregateEvent**](--aggregateevent.md) se entregue solo si WMI recibe más de cinco eventos de correo electrónico en los 300 segundos.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



En el ejemplo siguiente se agrupan todos los eventos recibidos en 600 segundos (es decir, 10 minutos) por **TargetInstance**. Propiedad **SourceName** . En este ejemplo, los eventos de agregado solo se entregan si el número de eventos [**\_ NTLogEvent de Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) recibidos del mismo origen es superior a 25. Tenga en cuenta que el operador ISA hace que la propiedad **TargetInstance** de la clase del sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) represente una instancia de la clase **\_ NTLogEvent de Win32** .


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
