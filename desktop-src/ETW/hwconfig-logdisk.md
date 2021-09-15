---
description: La clase HWConfig \_ LogDisk es la clase de tipo de evento para los eventos de configuración de disco lógico. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: HWConfig_LogDisk clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476899"
---
# <a name="hwconfig_logdisk-class"></a>HWConfig \_ LogDisk (clase)

La **clase HWConfig \_ LogDisk** es la clase de tipo de evento para los eventos de configuración de disco lógico.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a>Members

La **clase HWConfig \_ LogDisk** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase HWConfig \_ LogDisk** tiene estas propiedades.

<dl> <dt>

DiskNumber
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Número de índice del disco que contiene esta partición.

</dd> <dt>

Pad
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Reservado.

</dd> <dt>

PartitionSize
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Tamaño total de la partición, en bytes.

</dd> <dt>

StartOffset
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Desplazamiento inicial (en bytes) de la partición desde el principio del disco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




