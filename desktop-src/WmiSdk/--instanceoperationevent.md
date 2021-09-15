---
description: Actúa como una clase base para todos los eventos intrínsecos relacionados con una instancia de .
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466119"
---
# <a name="__instanceoperationevent-class"></a>\_\_Clase InstanceOperationEvent

La **\_ \_ clase del sistema InstanceOperationEvent** actúa como una clase base para todos los eventos intrínsecos relacionados con una instancia de .

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ clase InstanceOperationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase InstanceOperationEvent** tiene estas propiedades.

<dl> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia afectada por el evento. Para los eventos de creación, se trata de la instancia recién creada. En el caso de los eventos de modificación, esta es la nueva versión de la instancia modificada. En el caso de los eventos de eliminación, se trata de la instancia eliminada.

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\_ \_ clase InstanceOperationEvent** se deriva de [**\_ \_ Event**](--event.md).

No se crean **\_ \_ instancias de InstanceOperationEvent;** solo se crean instancias de sus subclases. Las clases siguientes derivan de **\_ \_ InstanceOperationEvent**:

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Información general**

Al igual que hay una clase WMI que representa cada tipo de recurso del sistema que se puede administrar mediante WMI, hay una clase WMI que representa cada tipo de evento WMI. Cuando se produce un evento que WMI puede supervisar, se crea una instancia de la clase de eventos WMI correspondiente. Se produce un evento WMI cuando se crea esa instancia.

Hay tres tipos principales de clases de eventos WMI, todas las cuales se derivan de la clase [**\_ \_ WMI**](--event.md) de eventos: Eventos intrínsecos, Eventos extrínsecos y Eventos de temporizador. Los eventos intrínsecos, a su vez, se representan mediante tres clases distintas derivadas de la clase **\_ \_ Event:** [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md), **\_ \_ InstanceOperationEvent** y [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

Eventos intrínsecos

Los eventos intrínsecos se usan para supervisar un recurso representado por una clase en el repositorio CIM. Cada recurso se representa mediante una instancia de una clase . Esto significa que la supervisión de un recurso mediante WMI implica realmente la supervisión de las instancias que corresponden al recurso.

Los eventos intrínsecos también se pueden usar para supervisar los cambios en un espacio de nombres o una clase del repositorio. Sin embargo, la supervisión de los cambios en espacios de nombres o clases tiene un valor limitado para los administradores del sistema.

Un evento intrínseco se representa mediante una instancia de una clase derivada de \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent o \_ \_ ClassOperationEvent. Los cambios en las instancias de WMI se representan mediante la clase InstanceOperationEvent y las clases derivadas de \_ \_ ella: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent e \_ \_ InstanceDeletionEvent.

La supervisión de recursos mediante WMI implica la supervisión de instancias y todos los cambios en las instancias se representan mediante InstanceOperationEvent y las \_ \_ clases derivadas de él. Esto significa que la supervisión de recursos implica en última instancia la supervisión de instancias de \_ \_ clases derivadas de InstanceOperationEvent.

Para registrar el interés en instancias de una de estas clases, emita una consulta de notificación expresada en WQL. La consulta usa una sintaxis similar a la siguiente:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Para obtener una explicación más larga del uso de los eventos de instancia de WMI para supervisar la actividad del equipo, vea [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Ejemplos

El [ejemplo de código](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript del evento de proceso monitor en la Galería de TechNet usa **\_ \_ InstanceOperationEvent** para supervisar el primer evento de instancia wmi para el proceso de [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_Evento**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinar el tipo de evento que se recibirá](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

