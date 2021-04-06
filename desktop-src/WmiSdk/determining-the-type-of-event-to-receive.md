---
description: 'Antes de registrarse para recibir un evento, debe determinar los tipos de eventos que se van a recibir: intrínseco o extrínseco.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Determinar el tipo de evento que se va a recibir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477f3d10536e5b0622e1e64b6cec9abdf4183c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815715"
---
# <a name="determining-the-type-of-event-to-receive"></a>Determinar el tipo de evento que se va a recibir

Antes de registrarse para recibir un evento, debe determinar los tipos de eventos que se van a recibir: [intrínseco](#intrinsic-events) o [extrínseco](#extrinsic-events). Para obtener más información acerca de cómo recibir eventos, consulte [recibir un evento WMI](receiving-a-wmi-event.md). Para obtener más información acerca de cómo proporcionar eventos, consulte [desarrollo de un proveedor de WMI](developing-a-wmi-provider.md) y [escritura de un proveedor de eventos](writing-an-event-provider.md). Para obtener más información acerca de los problemas de seguridad para recibir y proporcionar eventos, consulte [protección de eventos WMI.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Eventos intrínsecos

Un evento intrínseco es un evento que se produce en respuesta a un cambio en el modelo de datos WMI estándar. Cada clase de evento intrínseco representa un tipo específico de cambio y aparece cuando WMI o un proveedor crea, elimina o modifica un espacio de nombres, una clase o una instancia de clase. Por ejemplo, la creación de una instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) daría como resultado una instancia de [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) .

WMI crea eventos intrínsecos para objetos almacenados en el repositorio WMI. Un proveedor genera eventos intrínsecos para las clases dinámicas, pero WMI puede crear una instancia para una clase dinámica si no hay ningún proveedor disponible. WMI usa el sondeo para detectar los cambios. En la tabla siguiente se enumeran las clases del sistema que WMI utiliza para informar a los eventos intrínsecos.



| System (clase)                                                           | Descripción                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Notifica a un consumidor cuando se crea una clase.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Notifica a un consumidor cuando se elimina una clase.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Notifica a un consumidor cuando se modifica una clase.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Notifica a un consumidor cuando se crea una instancia de clase.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Notifica a un consumidor cuando se produce cualquier evento de instancia, como creación, eliminación o modificación de la instancia. Puede usar esta clase en consultas para obtener todos los tipos de eventos asociados a una instancia. |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Notifica a un consumidor cuando se elimina una instancia.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Notifica a un consumidor cuando se modifica una instancia.                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Notifica a un consumidor cuando se crea un espacio de nombres.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Notifica a un consumidor cuando se elimina un espacio de nombres.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Notifica a un consumidor cuando se modifica un espacio de nombres.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Notifica a un consumidor cuando se quita algún otro evento debido a un error en la parte de un consumidor de eventos.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Notifica a un consumidor cuando se quita algún otro evento en lugar de entregarlo al consumidor de eventos que lo solicita.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Notifica a un consumidor cuando se quita un evento como resultado de un desbordamiento de la cola de entrega.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Notifica a un consumidor cuando se produce un evento de llamada al método.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Eventos extrínsecos

Un evento extrínseco es una repetición predefinida que no se puede vincular directamente a los cambios en el modelo de datos WMI. Por lo tanto, WMI permite a un proveedor de eventos definir una clase de eventos que describe el evento. Por ejemplo, un evento que describe un equipo que cambia a modo de espera es un evento extrínseco. Un proveedor deriva un evento extrínseco de la clase del sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) , que es una subclase de la clase del sistema de [**\_ \_ eventos**](--event.md) . El [registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) y los proveedores [SNMP](snmp-provider.md) definen las clases de eventos extrínsecos, como **RegistryKeyChangeEvent**, que notifica a un consumidor cuando se cambia una clave del registro. Para obtener más información, vea [registrar eventos del registro del sistema](registering-for-system-registry-events.md) y [escribir un proveedor de eventos](writing-an-event-provider.md).

En el ejemplo siguiente, un proveedor de eventos informa de las infracciones de seguridad a uno o más edificios. Se puede definir la siguiente clase para el evento extrínseco que representa una infracción de seguridad.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Para recibir las notificaciones de infracción de seguridad, un consumidor se registra para el tipo de evento SecurityViolationEvent. A menos que se especifique lo contrario, un consumidor recibe una notificación de todas las infracciones de seguridad durante todos los períodos de tiempo y en todos los edificios. La clase de eventos también contiene información que los consumidores pueden usar para solicitar eventos más específicos.

En el ejemplo siguiente, la consulta registra el consumidor de eventos de infracción de seguridad solo en la compilación 24.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
