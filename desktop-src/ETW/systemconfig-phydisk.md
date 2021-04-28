---
description: 'SystemConfig_PhyDisk clase : esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.'
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106103"
---
# <a name="systemconfig_phydisk-class"></a>Clase SystemConfig \_ PhyDisk

Esta clase es la clase de tipo de evento para los eventos de configuración de disco físico.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a>Miembros

La **clase SystemConfig \_ PhyDisk** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemConfig \_ PhyDisk** tiene estas propiedades.

<dl> <dt>

**BootDriveLetter**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (14), **Max** (3), **Format("s")**
</dt> </dl>

Letra de unidad de la unidad de arranque con el formato " <letter> :".

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Número de bytes en cada sector para la unidad de disco físico.

</dd> <dt>

**Cilindros**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Número total de cilindros en la unidad de disco físico. Nota: El valor de esta propiedad se obtiene a través de funciones extendidas de interrupción del BIOS 13 horas. El valor puede ser inexacto si la unidad usa un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para obtener especificaciones precisas de la unidad.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Número de índice del disco que contiene esta partición.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (10), **Max** (256), **Format("s")**
</dt> </dl>

Nombre del fabricante de la unidad de disco.

</dd> <dt>

**Pad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (13)
</dt> </dl>

No se utiliza.

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (11)
</dt> </dl>

Número de particiones en esta unidad de disco físico que reconoce el sistema operativo.

</dd> <dt>

**SCSILun**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (9)
</dt> </dl>

Número de unidad lógica (LUN) SCSI del adaptador SCSI.

</dd> <dt>

**SCSIPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7)
</dt> </dl>

Número de bus SCSI del adaptador SCSI.

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6)
</dt> </dl>

Número SCSI del adaptador SCSI.

</dd> <dt>

**SCSITarget**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8)
</dt> </dl>

Contiene el número del dispositivo de destino.

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Número de sectores de cada pista para esta unidad de disco físico.

</dd> <dt>

**Repuesto**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (15), **Max** (2), **Format("s")**
</dt> </dl>

No se utiliza.

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Número de pistas de cada cilindro en la unidad de disco físico. Nota: El valor de esta propiedad se obtiene a través de funciones extendidas de interrupción de BIOS de 13 horas. El valor puede ser inexacto si la unidad usa un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para obtener especificaciones precisas de la unidad.

</dd> <dt>

**WriteCacheEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (12)
</dt> </dl>

True si la caché de escritura está habilitada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




