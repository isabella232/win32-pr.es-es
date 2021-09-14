---
description: Notifica un evento de creación de instancia, que es un tipo de evento intrínseco que se genera cuando se agrega una nueva instancia al espacio de nombres .
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174905"
---
# <a name="__instancecreationevent-class"></a>\_\_Clase InstanceCreationEvent

La clase del sistema **\_ \_ InstanceCreationEvent** notifica un evento [](determining-the-type-of-event-to-receive.md) de creación de instancia, que es un tipo de evento intrínseco que se genera cuando se agrega una nueva instancia al espacio de nombres .

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

## <a name="members"></a>Members

La **\_ \_ clase InstanceCreationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase InstanceCreationEvent** tiene estas propiedades.

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

Copia de la instancia que se creó. Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent.**](--instanceoperationevent.md)

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

La **\_ \_ clase InstanceCreationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Creación de un recurso: \_ \_ InstanceCreationEvent**

Supongamos que está interesado en recibir una notificación si Bloc de notas se ejecuta en un equipo determinado. Cuando Bloc de notas se ejecuta, se crea un proceso correspondiente. Los procesos se pueden administrar mediante WMI y se representan mediante la clase Process \_ de Win32. Cuando Bloc de notas se inicia la ejecución, una instancia correspondiente de la clase Process de Win32 pasa a \_ estar disponible a través de WMI. Si ha registrado su interés en este evento (mediante la emisión de la consulta de notificación de eventos adecuada), la disponibilidad de esta instancia da como resultado la creación de una instancia de la clase **\_ \_ InstanceCreationEvent.**

Las consultas de notificación que solicitan la notificación de la creación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

Para obtener una explicación más amplia del uso de **\_ \_ InstanceCreationEvent** como una manera de supervisar sistemas de archivos, vea [WMI y supervisión](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) del sistema de archivos en CodeProject.

## <a name="examples"></a>Ejemplos

El [ejemplo Crear](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) registro de eventos WMI permanentes para supervisar archivos de PowerShell en la Galería de TechNet usa **\_ \_ InstanceCreationEvent** como parte de un script complejo para configurar un registro de eventos WMI permanente.

El [ejemplo de PowerShell eventos permanentes WMI](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) de PowerShell en la Galería de TechNet usa **\_ \_ InstanceCreationEvent** como parte de un script de demostración para configurar un registro de eventos permanente.

El [ejemplo de VBScript](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) del evento de creación del proceso de supervisión en TechNet usa **\_ \_ InstanceCreationEvent** para supervisar el primer evento de creación de instancias wmi para [**el proceso de Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process)

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

 

