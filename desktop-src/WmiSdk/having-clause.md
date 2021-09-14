---
description: La cláusula HAVING se usa para filtrar los eventos que se reciben durante el intervalo de agrupación especificado en la cláusula WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: HAVING (Cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967172"
---
# <a name="having-clause"></a>HAVING (Cláusula)

La cláusula HAVING se usa para filtrar los eventos que se reciben durante el intervalo de agrupación especificado en la [cláusula WITHIN](within-clause.md). Por ejemplo, se podría construir una instrucción SELECT para que no devuelva nada a menos que haya habido al menos 5 eventos en los últimos 30 segundos INTERVAL.

La cláusula WITHIN sigue inmediatamente a la [instrucción SELECT después](select-statement-for-event-queries.md) de la cláusula [GROUP.](group-clause.md) La cláusula HAVING funciona en la **propiedad NumberOfEvents** de la clase del sistema [**\_ \_ AggregateEvent,**](--aggregateevent.md) de la que es miembro el grupo creado por la cláusula GROUP. La cláusula HAVING puede usar todos los operadores relacionales estándar.

La sintaxis es la siguiente:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

El *valor EventClass* es la clase de eventos de la que es miembro el evento y *value* es el valor de la propiedad en la que se requiere la notificación. El intervalo es un entero sin signo que representa el intervalo de agrupación (en segundos) después de recibir el primer evento. La lista de propiedades es una lista delimitada por comas de una o varias propiedades que se incluyen en la clase de eventos. El operador es cualquier operador relacional. El valor constante es cualquier entero de 32 bits sin signo que indica el número de eventos usados para filtrar.

Cuando se usa la cláusula HAVING, las cláusulas WHERE y BY son opcionales.

La siguiente consulta de eventos solicita que las notificaciones de la clase **EmailEvent** se alomenen en un evento 300 segundos después del primer evento que recibe WMI. Además, la consulta solicita que la instancia [**\_ \_ de AggregateEvent**](--aggregateevent.md) solo se entregue si WMI recibe más de cinco eventos de correo electrónico en ese tiempo de 300 segundos.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



En el ejemplo siguiente se agrupan todos los eventos recibidos en 600 segundos (es decir, 10 minutos) por **TargetInstance**. **Propiedad SourceName.** En este ejemplo, los eventos agregados solo se entregan si el número de eventos [**\_ NTLogEvent de Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) recibidos del mismo origen supera los 25. Tenga en cuenta que el operador ISA hace que la propiedad **TargetInstance** de la clase del sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) represente una instancia de la clase **\_ NTLogEvent win32.**


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
