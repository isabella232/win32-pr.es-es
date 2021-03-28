---
description: La \_ clase HWConfig PhyDisk es la clase de tipo de evento para los eventos de configuración de disco físico. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: HWConfig_PhyDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984487"
---
# <a name="hwconfig_phydisk-class"></a>HWConfig \_ PhyDisk (clase)

La clase **HWConfig \_ PhyDisk** es la clase de tipo de evento para los eventos de configuración de disco físico.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a>Miembros

La clase **HWConfig \_ PhyDisk** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **HWConfig \_ PhyDisk** tiene estas propiedades.

<dl> <dt>

BytesPerSector
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Número de bytes de cada sector para la unidad de disco físico.

</dd> <dt>

Cilindros
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5)
</dt> </dl>

Número total de cilindros en la unidad de disco físico. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

</dd> <dt>

Númerodedisco corresponde
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1)
</dt> </dl>

Número de índice del disco que contiene esta partición.

</dd> <dt>

Fabricante
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (10), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nombre del fabricante de la unidad de disco.

</dd> <dt>

SCSILun
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (9)
</dt> </dl>

Número de unidad lógica (LUN) SCSI del adaptador SCSI.

</dd> <dt>

SCSIPath
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (7)
</dt> </dl>

Número de bus SCSI del adaptador SCSI.

</dd> <dt>

SCSIPort
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6)
</dt> </dl>

Número SCSI del adaptador SCSI.

</dd> <dt>

SCSITarget
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (8)
</dt> </dl>

Contiene el número del dispositivo de destino.

</dd> <dt>

SectorsPerTrack
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Número de sectores de cada pista para esta unidad de disco físico.

</dd> <dt>

TracksPerCylinder
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Número de pistas en cada cilindro de la unidad de disco físico. Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS. El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad. Consulte al fabricante para conocer las especificaciones de unidad precisas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




