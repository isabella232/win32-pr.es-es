---
description: Esta clase es la clase de tipo de evento para eventos del canal IDE. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541867"
---
# <a name="systemconfig_idechannel-class"></a>SystemConfig \_ IDEChannel (clase)

Esta clase es la clase de tipo de evento para eventos del canal IDE.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a>Miembros

La clase **SystemConfig \_ IDEChannel** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SystemConfig \_ IDEChannel** tiene estas propiedades.

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3), Format ("x")
</dt> </dl>

Modo en el que el IDE podría funcionar. Los posibles valores son los siguientes:

-   PIO \_ MODE0 (0x1)
-   PIO \_ MODE1 (0X2)
-   PIO \_ Mode2 (0x4)
-   PIO \_ MODE3 (0x8)
-   PIO \_ MODE4 (0x10)
-   SWDMA \_ MODE0 (0x20)
-   SWDMA \_ MODE1 (0x40)
-   SWDMA \_ Mode2 (0x80)
-   MWDMA \_ MODE0 (0x100)
-   MWDMA \_ Mode2 (0x200)
-   MWDMA \_ MODE3 (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ MODE1 (0x1000)
-   UDMA \_ Mode2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0x8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), Format ("x")
</dt> </dl>

El tipo de dispositivo. Los posibles valores son los siguientes:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Canal IDE (por ejemplo, canal principal, canal secundario, etc.).

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Longitud de la cadena **LocationInformation** .

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1)
</dt> </dl>

Identificador del disco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




