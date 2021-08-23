---
description: Desmonta el dispositivo PCI especificado para que se pueda asignar.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Método DismountAssignableDevice de la Msvm_AssignableDeviceService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c9b602a26f789b0d7ccded487bafe8c0295133f6e4dd9457d51ce33ee24a8d0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693485"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Método DismountAssignableDevice de la clase AssignableDeviceService de Msvm \_

Desmonta el dispositivo PCI especificado para que se pueda asignar.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DismountSettingData* \[ En\]
</dt> <dd>

Instancia insertada de un objeto de datos de configuración que especifica el dispositivo PCI que se desmonta.

</dd> <dt>

*DismountedDeviceInstancePath* \[ out\]
</dt> <dd>

Cadena que contiene la ruta de acceso de la instancia del dispositivo al dispositivo desmontado.

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

 

 




