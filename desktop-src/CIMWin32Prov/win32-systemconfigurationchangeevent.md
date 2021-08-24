---
description: El evento \_ SystemConfigurationChangeEvent de Win32&\# 8194; La clase WMI indica que se ha actualizado la lista de dispositivos del sistema (se ha agregado o quitado un dispositivo o se ha cambiado la configuración).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 63a0708f2e081ffc8c5fb359be1e57aacd1cd62bd1db1daee2063e66e2fb55c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751305"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>Clase \_ SystemConfigurationChangeEvent de Win32

La clase  [WMI](../wmisdk/retrieving-a-class.md) **\_ SystemConfigurationChangeEvent de Win32** indica que se ha actualizado la lista de dispositivos del sistema (se ha agregado o quitado un dispositivo o se ha cambiado la configuración). Se desencadena un evento y se crea una instancia de esta clase cuando  se envía el mensaje "DevMgrRefreshOn<NombreDeEquipo>". El cambio exacto en la lista de dispositivos no está incluido en el mensaje, por lo que se requiere una actualización del dispositivo para obtener la configuración actual del sistema. Algunos ejemplos de cambios de configuración afectados son la configuración de IRQ, los puertos COM y las versiones de BIOS.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemConfigurationChangeEvent de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemConfigurationChangeEvent de Win32** tiene estas propiedades.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API Mensajes de administración de \| dispositivos WM \_ DEVICECHANGE \| wParam", "Win32API Mensajes de administración \| de dispositivos WM \_ SETTINGCHANGE")
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

**\_DESCRIPTOR DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento. Esta propiedad se hereda del [**\_ \_ evento**](../wmisdk/--event.md). Para obtener más información sobre las constantes usadas para establecer este descriptor de seguridad, vea [Constantes de seguridad WMI](../wmisdk/wmi-security-constants.md).

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

## <a name="remarks"></a>Comentarios

La **clase \_ SystemConfigurationChangeEvent de Win32** se deriva de [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md).

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

[**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
