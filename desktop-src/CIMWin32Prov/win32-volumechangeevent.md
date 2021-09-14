---
description: El evento VolumeChangeEvent de Win32 representa un evento de unidad local que resulta de la adición de una letra de unidad o una unidad montada \_ en el sistema del equipo.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Win32_VolumeChangeEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974453"
---
# <a name="win32_volumechangeevent-class"></a>Clase VolumeChangeEvent de Win32 \_

La clase  [WMI](../wmisdk/retrieving-a-class.md) **\_ VolumeChangeEvent de Win32** representa un evento de unidad local que resulta de la adición de una letra de unidad o unidad montada en el sistema del equipo. Actualmente no se admiten unidades de red.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a>Members

La **clase \_ VolumeChangeEvent de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VolumeChangeEvent de Win32** tiene estas propiedades.

<dl> <dt>

**DriveName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de unidad (letra) que se ha agregado o quitado del sistema.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Tipo de notificación de cambio de evento que se ha producido.

Esta propiedad se hereda de [**Win32 \_ DeviceChangeEvent.**](win32-devicechangeevent.md)

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configuración cambiada** (1)


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

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Wmi Security Constants](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor único que indica la hora a la que se generó el evento. Se trata de un valor de 64 bits que representa el número de intervalos de 100 nanosegundos después del 1 de enero de 1601. La información está en formato de hora universal coordinada (UTC).

Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ VolumeChangeEvent de Win32** se deriva de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
