---
description: La \_ clase WMI abstracta DeviceChangeEvent de Win32 representa los eventos de cambio de dispositivo que se derivan de la adición, eliminación o modificación de dispositivos en el sistema del equipo.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Win32_DeviceChangeEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807922"
---
# <a name="win32_devicechangeevent-class"></a>\_Clase Win32 DeviceChangeEvent

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ DeviceChangeEvent de Win32** representa los eventos de cambio de dispositivo que se derivan de la adición, eliminación o modificación de dispositivos en el sistema del equipo. Esto incluye los cambios en la configuración de hardware (acoplamiento y desacoplamiento), el estado del hardware o los dispositivos recién asignados (asignación de una unidad de red). Por ejemplo, un dispositivo ha cambiado cuando \_ se envía un mensaje de DEVICECHANGE de WM.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Miembros

La **clase \_ DeviceChangeEvent de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceChangeEvent de Win32** tiene estas propiedades.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Tipo de notificación de cambio de evento que se ha producido.

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configuración modificada** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Llegada del dispositivo** (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Eliminación de dispositivos** (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Acoplamiento** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601. La información está en el formato de hora universal coordinada (UTC).

Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Win32 \_ DeviceChangeEvent** es una clase abstracta que se deriva de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

