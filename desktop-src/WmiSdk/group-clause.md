---
description: La cláusula GROUP hace que WMI genere una notificación única para representar un grupo de eventos.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: GROUP (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707216"
---
# <a name="group-clause"></a>GROUP (cláusula)

La cláusula GROUP hace que WMI genere una notificación única para representar un grupo de eventos. La notificación representativa es una instancia de la clase del sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) . La clase del sistema **\_ \_ AggregateEvent** contiene dos propiedades: **representator** y **NumberOfEvents**. La propiedad **representativa** es un objeto incrustado que contiene una de las instancias recibidas durante el intervalo de agrupación especificado en la [cláusula Within](within-clause.md). Por ejemplo, si se genera un evento agregado para notificar los eventos de modificación de instancia, el **representador** contiene una instancia de la clase [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) . La propiedad **NumberOfEvents** contiene el número de eventos recibidos durante el intervalo de agrupación. El intervalo de agrupación especifica el período de tiempo, después de recibir un evento inicial, durante el cual WMI debe recopilar eventos similares.

La cláusula GROUP debe contener una cláusula WITHIN para especificar el intervalo de agrupación y puede contener la palabra clave BY o HAVING, o ambas. La cláusula GROUP se coloca después de la cláusula WHERE, como se muestra a continuación:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

El valor de *EventClass* es la clase de eventos de la que el evento es un miembro y *Value* es el valor de la propiedad en la que se requiere la notificación. El intervalo es un entero sin signo que representa el intervalo de agrupación después de recibir el primer evento. El entero sin signo es un número de segundos. La lista de propiedades es una lista delimitada por comas de una o varias propiedades que se incluyen en la clase de eventos; *Operator* es cualquier operador relacional; y *entero* es un entero de 32 bits sin signo que indica un número de eventos.

Cuando se usa la cláusula GROUP, las cláusulas WHERE, BY y HAVING son opcionales.

Un uso básico de la cláusula GROUP podría solicitar una agrupación de eventos dentro de un intervalo de tiempo que se inicia cuando se recibe el primer evento. Por ejemplo, la consulta siguiente agrupa todos los eventos de correo electrónico enviados en 5 minutos. En lugar de paginar a un usuario cada vez que se recibe un mensaje de correo electrónico nuevo, el consumidor permanente podría usar esta consulta para informar al usuario solo si se ha recibido un nuevo correo electrónico en los últimos 5 minutos.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Si se requiere información más detallada, los eventos se pueden agrupar por una o más propiedades de la clase de evento. La consulta siguiente solicita que los eventos de correo electrónico se combinen con otros eventos que tienen el mismo valor en la propiedad **Sender** :


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



Se puede lograr un nivel de detalle todavía mayor agregando una cláusula WHERE. Por ejemplo, la siguiente consulta notifica a un usuario de un mensaje de correo electrónico nuevo de un remitente determinado que ha llegado en los últimos 10 minutos, junto con otros eventos que tienen el mismo valor en la propiedad **importance** :


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



