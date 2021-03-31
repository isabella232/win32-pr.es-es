---
description: Informa de un evento de creación de instancia, que es un tipo de evento intrínseco que se genera cuando se agrega una nueva instancia al espacio de nombres.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278781"
---
# <a name="__instancecreationevent-class"></a>\_\_Clase InstanceCreationEvent

La clase del sistema **\_ \_ InstanceCreationEvent** informa de un evento de creación de instancia, que es un tipo de [evento intrínseco](determining-the-type-of-event-to-receive.md) que se genera cuando se agrega una nueva instancia al espacio de nombres.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ InstanceCreationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ InstanceCreationEvent** tiene estas propiedades.

<dl> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
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

Copia de la instancia de que se creó. Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información tiene el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ InstanceCreationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Creación de un recurso: \_ \_ InstanceCreationEvent**

Supongamos que está interesado en recibir una notificación si el Bloc de notas se ejecuta en un equipo determinado. Cuando se ejecuta el Bloc de notas, se crea un proceso correspondiente. Los procesos se pueden administrar mediante WMI y se representan mediante la clase de proceso de Win32 \_ . Cuando el Bloc de notas comienza a ejecutarse, una instancia correspondiente de la clase de proceso de Win32 \_ pasa a estar disponible a través de WMI. Si ha registrado su interés en este evento (emitiendo la consulta de notificación de eventos adecuada), la disponibilidad de esta instancia da como resultado la creación de una instancia de la clase **\_ \_ InstanceCreationEvent** .

Las consultas de notificación que solicitan la notificación de la creación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

Para obtener una explicación más amplia del uso de **\_ \_ InstanceCreationEvent** como una manera de supervisar sistemas de archivos, consulte [WMI y supervisión del sistema de archivos](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) en CodeProject.

## <a name="examples"></a>Ejemplos

El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **\_ \_ InstanceCreationEvent** como parte de un script complejo para configurar un registro de eventos de WMI permanente.

El ejemplo de PowerShell de [eventos permanentes de WMI de PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) en la galería de TechNet usa **\_ \_ InstanceCreationEvent** como parte de un script de demostración para configurar un registro de eventos permanente.

En el ejemplo de VBScript del [evento de creación de procesos de supervisión](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) en TechNet se usa **\_ \_ InstanceCreationEvent** para supervisar el primer evento de creación de instancia de WMI para el [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

