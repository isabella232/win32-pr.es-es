---
description: Representa la configuración de un sistema virtual que se importará. Usado por el método Dismount de la clase \_ AssignableDeviceService de Msvm.
ms.assetid: 49892e21-3e8d-4644-8cde-72966927f350
title: Msvm_AssignableDeviceDismountSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceDismountSettingData
- Msvm_AssignableDeviceDismountSettingData.DeviceInstancePath
- Msvm_AssignableDeviceDismountSettingData.DeviceLocationPath
- Msvm_AssignableDeviceDismountSettingData.RequireAcsSupport
- Msvm_AssignableDeviceDismountSettingData.RequireDeviceMitigations
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67d2bf61cc317fee3dd04e464384020cfa04be9f601205e44d031c4fe4fa3ff8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693495"
---
# <a name="msvm_assignabledevicedismountsettingdata-class"></a>Clase \_ AssignableDeviceDismountSettingData de Msvm

Representa la configuración de un sistema virtual que se importará. Usado por el [**método Dismount**](msvm-assignabledeviceservice-dismountassignabledevice.md) de la [**clase \_ AssignableDeviceService de Msvm.**](msvm-assignabledeviceservice.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_AssignableDeviceDismountSettingData : CIM_SettingData
{
  string  DeviceInstancePath;
  string  DeviceLocationPath;
  boolean RequireAcsSupport;
  boolean RequireDeviceMitigations;
};
```

## <a name="members"></a>Miembros

La **clase \_ AssignableDeviceDismountSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ AssignableDeviceDismountSettingData** tiene estas propiedades.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Id. de instancia de dispositivo PNP.

</dd> <dt>

**DeviceLocationPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Ruta de acceso de ubicación del dispositivo PNP.

</dd> <dt>

**RequireAcsSupport**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si el soporte técnico de ACS necesario debe estar en su lugar antes de permitir el desmontaje.

</dd> <dt>

**RequireDeviceMitigations**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Indica si las mitigaciones de dispositivos deben estar en su lugar antes de permitir el desmontaje.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




