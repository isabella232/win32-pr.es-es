---
description: La clase WMI abstracta DeviceChangeEvent de Win32 representa los eventos de cambio de dispositivo resultantes de la adición, eliminación o modificación de dispositivos \_ en el sistema informático.
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Win32_DeviceChangeEvent clase
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
ms.openlocfilehash: 3599661e1801c65b0cfc3b8a1cae0f9e3e820ce0b2cdb6aab9266e8e67f70338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816636"
---
# <a name="win32_devicechangeevent-class"></a>Clase DeviceChangeEvent de Win32 \_

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstracta **\_ DeviceChangeEvent de Win32** representa los eventos de cambio de dispositivo resultantes de la adición, eliminación o modificación de dispositivos en el sistema informático. Esto incluye cambios en la configuración de hardware (acoplamiento y desacoplamiento), el estado de hardware o los dispositivos recién asignados (asignación de una unidad de red). Por ejemplo, un dispositivo ha cambiado cuando se envía un mensaje \_ DEVICECHANGE de WM.

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

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Tipo de notificación de cambio de evento que se ha producido.

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configuración modificada** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Llegada del** dispositivo (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Eliminación de** dispositivos (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Acoplamiento** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad wmi](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC).

Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentarios

**Win32 \_ DeviceChangeEvent** es una clase abstracta derivada de [**\_ \_ ExtrinsicEvent.**](/windows/desktop/WmiSdk/--extrinsicevent)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

