---
description: Representa el estado configurado de un dispositivo de partición GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001254"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>MSVM \_ GpuPartitionSettingData (clase)

Representa el estado configurado de un dispositivo de partición GPU.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ GpuPartitionSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ GpuPartitionSettingData** tiene estas propiedades.

<dl> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad máxima de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad máxima de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad máxima de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Cantidad máxima de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad mínima de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad mínima de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad mínima de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad mínima de VRAM que aparecerá en la partición de GPU.

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad óptima de motores de proceso que aparecerán en la partición de GPU.

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad óptima de motores de descodificación que aparecerán en la partición de GPU.

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

La cantidad óptima de motores de codificación que aparecerán en la partición de GPU.

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Cantidad óptima de VRAM que aparecerá en la partición de GPU.

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




