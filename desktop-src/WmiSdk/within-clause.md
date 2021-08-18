---
description: Use la cláusula WITHIN en las consultas de eventos para especificar un intervalo de sondeo o un intervalo de agrupación.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: WITHIN (cláusula)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee35350a52ef6af1aa22aacf775d22b3c7629fb479967a74aed1408aa5e1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757605"
---
# <a name="within-clause"></a>WITHIN (cláusula)

Los consumidores de eventos usan la cláusula WITHIN en las consultas de eventos para especificar un intervalo *de sondeo* o un intervalo *de agrupación*.

Un intervalo de sondeo es el intervalo que usa Windows Management Instrumentation (WMI) para sondear el proveedor de datos responsable de la clase para eventos intrínsecos [,](determining-the-type-of-event-to-receive.md)del que el evento consultado es miembro. Este intervalo es la cantidad de tiempo máxima que puede transcurrir antes de entregarse la notificación de un evento. Un consumidor usa un intervalo de sondeo en una cláusula WITHIN cuando el consumidor requiere la notificación de cambios en una clase y un proveedor de eventos no está disponible. El consumidor se registra para un evento intrínseco e incluye el intervalo de sondeo.

Para especificar un intervalo de sondeo, coloque la cláusula WITHIN inmediatamente antes de la cláusula WHERE, como se muestra a continuación:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass es la clase de eventos intrínseca de la que el evento es miembro, interval es el intervalo de sondeo y value es el valor de la propiedad en la que el consumidor requiere notificación.

El intervalo de sondeo es un número de punto flotante y puede ser fraccionrio para aceptar valores menores de 1 segundo. Sin embargo, el intervalo debe representar un número de segundos en lugar de un valor extremadamente pequeño, como 0,001, porque la especificación de un valor demasiado pequeño puede hacer que WMI rechace la instrucción como no válida, debido a la naturaleza de sondeo que consume muchos recursos. Dado que la mayoría de los consumidores de eventos no requieren notificación inmediata, se recomienda que usen un intervalo superior a 5 minutos.

En el ejemplo de consulta siguiente se solicita que WMI compruebe cada 10 segundos los cambios que se producen en las instancias de la [**\_ clase LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Si una instancia de la clase se modifica dentro del intervalo de sondeo especificado, se envía un evento de notificación para cada modificación.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



En función de la consulta, un proveedor de eventos y WMI pueden compartir la tarea de proporcionar eventos. Por ejemplo, un proveedor de eventos que admite eventos de las clases del sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) e [**\_ \_ InstanceModificationEvent,**](--instancemodificationevent.md) y no eventos de la clase del sistema [**\_ \_ InstanceDeletionEvent.**](--instancedeletionevent.md) La consulta siguiente permite al proveedor de eventos generar los eventos de creación y modificación a medida que se producen y hacer que se entreguen cuando se crean. La consulta también permite que WMI genere eventos **\_ \_ InstanceDeletionEvent** cada 10 (diez) segundos mediante el mecanismo de sondeo.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



También puede usar la cláusula WITHIN para especificar un intervalo de agrupación. Un intervalo de agrupación es un entero de 32 bits sin signo que especifica el período de tiempo, después de recibir un evento inicial, durante el cual WMI debe recopilar eventos similares. Cuando expira este período de tiempo, WMI entrega el evento agregado, que se conste de todos los eventos similares. Para obtener más información, vea [CLÁUSULA GROUP](group-clause.md).

Los consumidores de eventos que se registran para eventos que se producen con frecuencia usan un intervalo de agrupación con la cláusula WITHIN. Al agregar GROUP WITHIN a la cláusula WHERE en una consulta de eventos, WMI envía un evento agregado en lugar de muchos eventos. La clase del sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) representa el evento de agregado.

Para especificar un intervalo de agrupación, coloque la cláusula WITHIN inmediatamente después de la cláusula GROUP.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass es la clase de eventos de la que el evento es miembro, value es el valor de la propiedad en la que el consumidor requiere notificación e Interval es el intervalo de agrupación.

Para obtener más información, [vea Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

Los consumidores de eventos permanentes solo se pueden crear con consultas de sondeo si tiene privilegios de administrador.

 

 
