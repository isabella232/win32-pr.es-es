---
description: 'SystemConfig_V0_LogDisk clase : esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.'
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb0ad959d637a38a03b77bd8d7a812ff608ddc04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105983"
---
# <a name="systemconfig_v0_logdisk-class"></a>Clase LogDisk SystemConfig \_ V0 \_

Esta clase es la clase de tipo de evento para los eventos de configuración de disco lógico.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ LogDisk SystemConfig V0** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ LogDisk SystemConfig V0** tiene estas propiedades.

<dl> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10)
</dt> </dl>

Número de bytes en cada sector para la unidad de disco físico.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Número de índice del disco que contiene esta partición.

</dd> <dt>

**DriveLetterString**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **Max** (4)
</dt> </dl>

Letra de unidad del disco con el formato " <letter> :".

</dd> <dt>

**DriveType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Tipo de unidad de disco. Los valores posibles son:



| Valor                                                                        | Significado                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>1</dt> </dl> | Partition<br/>                            |
| <dl> <dt>2</dt> </dl> | Volumen<br/>                               |
| <dl> <dt>3</dt> </dl> | Partición extendida en varios discos<br/> |



 

</dd> <dt>

**Filesystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13), **Max** (16)
</dt> </dl>

Sistema de archivos en el disco lógico, por ejemplo, NTFS.

</dd> <dt>

**NumberOfFreeClusters**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Número de clústeres libres en el volumen especificado.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Reservado.

</dd> <dt>

**PartitionNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8)
</dt> </dl>

Número de índice de la partición.

</dd> <dt>

**PartitionSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Tamaño total de la partición, en bytes.

</dd> <dt>

**SectorsPerCluster**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Número de sectores del volumen.

</dd> <dt>

**Tamaño**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Tamaño de la unidad de disco, en bytes.

</dd> <dt>

**StartOffset**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Desplazamiento inicial (en bytes) de la partición desde el principio del disco.

</dd> <dt>

**TotalNumberOfClusters**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12)
</dt> </dl>

Número de clústeres usados y libres en el volumen.

</dd> <dt>

**VolumeExt**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14)
</dt> </dl>

Reservado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




