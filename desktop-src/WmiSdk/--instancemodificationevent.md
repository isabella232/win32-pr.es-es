---
description: Notifica un evento de modificación de instancia, que es un tipo de evento intrínseco generado cuando una instancia cambia en el espacio de nombres .
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174902"
---
# <a name="__instancemodificationevent-class"></a>\_\_InstanceModificationEvent (clase)

La clase del sistema **\_ \_ InstanceModificationEvent** notifica un evento [](determining-the-type-of-event-to-receive.md) de modificación de instancia, que es un tipo de evento intrínseco generado cuando una instancia cambia en el espacio de nombres .

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ clase InstanceModificationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase InstanceModificationEvent** tiene estas propiedades.

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de la instancia antes de la modificación.

</dd> <dt>

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

Nueva versión de la instancia modificada. Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent.**](--instanceoperationevent.md)

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

La **\_ \_ clase InstanceModificationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

**Modificación de un recurso: \_ \_ InstanceModificationEvent**

Supongamos que sospecha que una aplicación de administración que usa está cambiando erróneamente el tipo de inicio de un servicio en uno de los servidores. Quiere escribir un script WMI para supervisar las modificaciones realizadas en la configuración del servicio. En cuanto se realiza una modificación en un servicio, su TargetInstance correspondiente refleja la modificación.

Si registra su interés en este evento, una modificación en la configuración del servicio da como resultado la creación de una instancia de la **\_ \_ clase InstanceModificationEvent.**

Las consultas de notificación que solicitan la notificación de la modificación de un recurso y usan eventos intrínsecos usan una sintaxis similar a la siguiente:

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Ejemplos

El [ejemplo de](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript del evento de modificación del proceso de supervisión en la Galería de TechNet usa **\_ \_ InstanceModificationEvent** para supervisar la primera aparición de un evento de modificación de instancia wmi para el proceso de [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-process)

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

 

