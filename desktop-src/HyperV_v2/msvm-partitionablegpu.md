---
description: Representa una GPU particionable. Cada GPU se puede segmentar en varias particiones de GPU, que se pueden asignar a una máquina virtual como una vGPU.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Msvm_PartitionableGpu clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15ce369a0186ae6309f90a5b37a77a35cce90ae6997e3c8cbc7e968a0a0d0de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148298"
---
# <a name="msvm_partitionablegpu-class"></a>Clase Msvm \_ PartitionableGpu

Representa una GPU particionable. Cada GPU se puede segmentar en varias particiones de GPU, que se pueden asignar a una máquina virtual como una vGPU.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ PartitionableGpu** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ PartitionableGpu** tiene estas propiedades.

<dl> <dt>

**AvailableCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad disponible de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**AvailableDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad disponible de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**AvailableEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad disponible de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**AvailableVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad disponible de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad máxima de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad máxima de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad máxima de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad máxima de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad mínima de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad mínima de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad mínima de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad mínima de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad óptima de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad óptima de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad óptima de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad óptima de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Cantidad de particiones de GPU en las que se segmenta la GPU física.

</dd> <dt>

**TotalCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad total de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**TotalDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad total de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**TotalEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad total de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**TotalVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad total de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**ValidPartitionCounts**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Matriz de opciones de partición de GPU válidas en las que se puede segmentar la GPU física.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> </dl>

 

 




