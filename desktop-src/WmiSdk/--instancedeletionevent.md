---
description: Notifica un evento de eliminación de instancia, que es un tipo de evento intrínseco generado cuando se elimina una instancia del espacio de nombres .
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: __InstanceDeletionEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a210f67e7e71d9980a3eeb88ae54fad7fee3ec62597b81ae7253a2893a437a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320889"
---
# <a name="__instancedeletionevent-class"></a>\_\_InstanceDeletionEvent (clase)

La clase del sistema **\_ \_ InstanceDeletionEvent** notifica un evento [](determining-the-type-of-event-to-receive.md) de eliminación de instancia, que es un tipo de evento intrínseco generado cuando se elimina una instancia del espacio de nombres .

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase InstanceDeletionEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase InstanceDeletionEvent** tiene estas propiedades.

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

Copia de la instancia que se eliminó. Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent.**](--instanceoperationevent.md)

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase InstanceDeletionEvent** se deriva de [**\_ \_ InstanceOperationEvent.**](--instanceoperationevent.md)

**Eliminación de un recurso: \_ \_ InstanceDeletionEvent**

Si desea asegurarse de que un programa de escáner antivirus determinado continúa en ejecución en un equipo, puede escribir un script que supervisa los procesos en el equipo para determinar si alguno de ellos se detiene.

Las consultas de notificación que solicitan la notificación de la eliminación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a>Ejemplos

El [ejemplo de](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) código VBScript del evento de eliminación del proceso de supervisión en la Galería de TechNet usa **\_ \_ InstanceDeletionEvent** para supervisar la primera aparición de un evento de eliminación de instancia WMI para el proceso de [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

