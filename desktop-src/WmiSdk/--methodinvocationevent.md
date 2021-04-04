---
description: La \_ \_ clase del sistema MethodInvocationEvent está definida pero no se implementa.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: __MethodInvocationEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277942"
---
# <a name="__methodinvocationevent-class"></a>\_\_Clase MethodInvocationEvent

La clase del sistema **\_ \_ MethodInvocationEvent** está definida pero no se implementa.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ MethodInvocationEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ MethodInvocationEvent** tiene estas propiedades.

<dl> <dt>

**Método**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Método invocado para desencadenar el evento.

</dd> <dt>

**Parámetros**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ parámetros**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de que representa los parámetros de entrada y salida de la llamada al método.

</dd> <dt>

**Llamada precall**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si es **true**, el evento se genera antes de que se llame al método.

</dd> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](--event.md). Para obtener más información, vea [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Instancia en la que se invoca el método. Esta propiedad se hereda de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se genera un evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información tiene el formato de hora universal coordinada (UTC). Esta propiedad se hereda del [**\_ \_ evento**](--event.md).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ MethodInvocationEvent** se deriva de [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

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

 

