---
description: 'Antes de registrarse para recibir un evento, debe determinar los tipos de eventos que se recibirán: intrínsecos o extrínsecos.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Determinar el tipo de evento que se recibirá
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477f3d10536e5b0622e1e64b6cec9abdf4183c7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270359"
---
# <a name="determining-the-type-of-event-to-receive"></a>Determinar el tipo de evento que se recibirá

Antes de registrarse para recibir un evento, debe determinar los tipos de eventos que se [recibirán:](#intrinsic-events) [intrínsecos o extrínsecos.](#extrinsic-events) Para obtener más información sobre cómo recibir eventos, vea [Recibir un evento WMI](receiving-a-wmi-event.md). Para obtener más información sobre cómo proporcionar eventos, vea [Desarrollar un proveedor WMI y](developing-a-wmi-provider.md) Escribir un proveedor de [eventos](writing-an-event-provider.md). Para obtener más información sobre los problemas de seguridad para recibir y proporcionar eventos, vea [Securing WMI Events.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Eventos intrínsecos

Un evento intrínseco es un evento que se produce en respuesta a un cambio en el modelo de datos WMI estándar. Cada clase de evento intrínseco representa un tipo específico de cambio y aparece cuando WMI o un proveedor crea, elimina o modifica un espacio de nombres, una clase o una instancia de clase. Por ejemplo, la creación de una [**instancia de \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) daría lugar a una [**\_ \_ instancia instanceCreationEvent.**](--instancecreationevent.md)

WMI crea eventos intrínsecos para los objetos almacenados en el repositorio WMI. Un proveedor genera eventos intrínsecos para las clases dinámicas, pero WMI puede crear una instancia para una clase dinámica si no hay ningún proveedor disponible. WMI usa el sondeo para detectar los cambios. En la tabla siguiente se enumeran las clases del sistema que WMI usa para notificar eventos intrínsecos.



| Clase system                                                           | Descripción                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Notifica a un consumidor cuando se crea una clase.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Notifica a un consumidor cuando se elimina una clase.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Notifica a un consumidor cuando se modifica una clase.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Notifica a un consumidor cuando se crea una instancia de clase.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Notifica a un consumidor cuando se produce cualquier evento de instancia, como la creación, eliminación o modificación de la instancia. Puede usar esta clase en las consultas para obtener todos los eventos de tipos asociados a una instancia de . |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Notifica a un consumidor cuándo se elimina una instancia.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Notifica a un consumidor cuando se modifica una instancia de .                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Notifica a un consumidor cuando se crea un espacio de nombres.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Notifica a un consumidor cuándo se elimina un espacio de nombres.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Notifica a un consumidor cuándo se modifica un espacio de nombres.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Notifica a un consumidor cuando se descarta algún otro evento debido a un error por parte de un consumidor de eventos.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Notifica a un consumidor cuando se descarta algún otro evento en lugar de entregarse al consumidor de eventos solicitante.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Notifica a un consumidor cuando se descarta un evento como resultado de un desbordamiento de cola de entrega.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Notifica a un consumidor cuando se produce un evento de llamada de método.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Eventos extrínsecos

Un evento extrínsico es una repetición predefinida que no se puede vincular directamente a los cambios en el modelo de datos WMI. Por lo tanto, WMI permite a un proveedor de eventos definir una clase de eventos que describe el evento. Por ejemplo, un evento que describe un equipo que cambia al modo de espera es un evento extrínsico. Un proveedor deriva un evento extrínsico de la clase del sistema [**\_ \_ ExtrinsicEvent,**](--extrinsicevent.md) que es una subclase de la [**\_ \_ clase Del**](--event.md) sistema de eventos. Los [proveedores del Registro](/previous-versions/windows/desktop/regprov/system-registry-provider) del sistema y [SNMP](snmp-provider.md) definen clases de eventos extrínsecos, como **RegistryKeyChangeEvent**, que notifica a un consumidor cuándo se cambia una clave del Registro. Para obtener más información, vea [Registrar para eventos del Registro del sistema](registering-for-system-registry-events.md) y Escribir un proveedor de [eventos](writing-an-event-provider.md).

En el ejemplo siguiente, un proveedor de eventos informa de infracciones de seguridad a uno o varios edificios. La clase siguiente podría definirse para el evento extrínsico que representa una infracción de seguridad.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Para recibir las notificaciones de infracción de seguridad, un consumidor se registra para el tipo de evento SecurityViolationEvent. A menos que se especifique lo contrario, un consumidor recibe una notificación de todas las infracciones de seguridad durante todos los períodos de tiempo y en todos los edificios. La clase de eventos también contiene información que los consumidores pueden usar para solicitar eventos más específicos.

En el ejemplo siguiente, la consulta registra el consumidor para los eventos de infracción de seguridad solo en la creación de 24.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
