---
description: Utilice la cláusula WITHIN en las consultas de eventos para especificar un intervalo de sondeo o un intervalo de agrupación.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Cláusula WITHIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155997"
---
# <a name="within-clause"></a>Cláusula WITHIN

Los consumidores de eventos usan la cláusula WITHIN en las consultas de eventos para especificar un *intervalo de sondeo* o un *intervalo de agrupación*.

Un intervalo de sondeo es el intervalo que Instrumental de administración de Windows (WMI) utiliza para sondear el proveedor de datos responsable de la clase para los [eventos intrínsecos](determining-the-type-of-event-to-receive.md), de los que el evento consultado es un miembro. Este intervalo es la cantidad de tiempo máxima que puede transcurrir antes de entregarse la notificación de un evento. Un consumidor utiliza un intervalo de sondeo en una cláusula WITHIN cuando el consumidor requiere la notificación de cambios en una clase y un proveedor de eventos no está disponible. El consumidor se registra para un evento intrínseco e incluye el intervalo de sondeo.

Para especificar un intervalo de sondeo, coloque la cláusula WITHIN inmediatamente antes de la cláusula WHERE, como se muestra a continuación:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass es la clase de eventos intrínseca de la que el evento es un miembro, Interval es el intervalo de sondeo y Value es el valor de la propiedad en la que el consumidor requiere la notificación.

El intervalo de sondeo es un número de punto flotante y puede ser fraccionario para aceptar valores inferiores a 1 segundo. Sin embargo, el intervalo debe representar un número de segundos en lugar de un valor muy pequeño, como 0,001, porque especificar un valor demasiado pequeño puede hacer que WMI rechace la instrucción como no válido, debido a la naturaleza de un uso intensivo de recursos del sondeo. Dado que la mayoría de los consumidores de eventos no requieren una notificación inmediata, se recomienda usar un intervalo que sea superior a 5 minutos.

En el ejemplo de consulta siguiente se solicita que WMI Compruebe cada 10 segundos los cambios que se producen en las instancias de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Si se modifica una instancia de la clase dentro del intervalo de sondeo especificado, se envía un evento de notificación para cada modificación.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Dependiendo de la consulta, un proveedor de eventos y WMI pueden compartir la tarea de proporcionar eventos. Por ejemplo, un proveedor de eventos que admite eventos de las clases del sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) y [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) , y no eventos de la clase del sistema [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) . La siguiente consulta permite al proveedor de eventos generar los eventos de creación y modificación a medida que se producen y que se entregan cuando se crean. La consulta también permite a WMI generar eventos **\_ \_ InstanceDeletionEvent** cada 10 (diez) segundos mediante el mecanismo de sondeo.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



También puede utilizar la cláusula WITHIN para especificar un intervalo de agrupación. Un intervalo de agrupación es un entero de 32 bits sin signo que especifica el período de tiempo, después de recibir un evento inicial, durante el cual WMI debe recopilar eventos similares. Cuando expira este período de tiempo, WMI entrega el evento agregado, compuesto por todos los eventos similares. Para obtener más información, vea [Group (cláusula](group-clause.md)).

Los consumidores de eventos que se registran para eventos que se producen con frecuencia utilizan un intervalo de agrupación con la cláusula WITHIN. Al agregar un grupo en la cláusula WHERE de una consulta de evento, WMI envía un evento agregado en lugar de muchos eventos. El evento Aggregate se representa mediante la clase de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .

Para especificar un intervalo de agrupación, coloque la cláusula WITHIN inmediatamente después de la cláusula GROUP.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass es la clase de eventos de la que el evento es un miembro, Value es el valor de la propiedad en la que el consumidor requiere notificación e Interval es el intervalo de agrupación.

Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).

Los consumidores de eventos permanentes se pueden crear con consultas de sondeo solo si tiene privilegios de administrador.

 

 
