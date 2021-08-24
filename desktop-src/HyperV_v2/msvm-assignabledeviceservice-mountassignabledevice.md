---
description: Monta el dispositivo PCI especificado para que pueda ser utilizado por el sistema del equipo host.
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Método MountAssignableDevice de la Msvm_AssignableDeviceService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af7848306a289703717919f6e3407218774a8eba96814677cad9d7bf6f694aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790315"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Método MountAssignableDevice de la clase \_ Msvm AssignableDeviceService

Monta el dispositivo PCI especificado para que pueda ser utilizado por el sistema del equipo host.

## <a name="syntax"></a>Sintaxis


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DeviceInstancePath* \[ En\]
</dt> <dd>

Cadena que contiene la ruta de acceso de la instancia de dispositivo a un dispositivo.

</dd> <dt>

*DeviceLocationPath* \[ En\]
</dt> <dd>

Cadena que contiene la ruta de acceso de ubicación del dispositivo a un dispositivo.

</dd> <dt>

*MountedDeviceInstancePath* \[ out\]
</dt> <dd>

Cadena que contiene la ruta de acceso de la instancia del dispositivo al dispositivo montado.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia al trabajo (puede ser NULL si se completa la tarea).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo para aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




