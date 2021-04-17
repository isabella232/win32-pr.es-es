---
description: Representa el estado de la partición de GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Msvm_GpuPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686955"
---
# <a name="msvm_gpupartition-class"></a>MSVM \_ GpuPartition (clase)

Representa el estado de la partición de GPU.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ GpuPartition** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ GpuPartition** tiene estas propiedades.

<dl> <dt>

**DeviceInstancePath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que contiene la ruta de acceso de la instancia del dispositivo que identifica el dispositivo de partición GPU.

</dd> <dt>

**PartitionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El ID. de partición del dispositivo de partición GPU.

</dd> <dt>

**PartitionVfLuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

LUID de la función virtual, que representa una partición de GPU.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> </dl>

 

 




