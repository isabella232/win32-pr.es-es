---
description: Esta clase es la clase de tipo de evento para eventos de canal IDE. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: SystemConfig_IDEChannel clase
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
ms.openlocfilehash: 8cf764d266d98199e27b40c8690b36183aa82aa2cfb8ded006087ab55f3ddfca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041605"
---
# <a name="systemconfig_idechannel-class"></a>Clase SystemConfig \_ IDEChannel

Esta clase es la clase de tipo de evento para eventos de canal IDE.

La sintaxis siguiente se simplifica a partir del código MOF.

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

La **clase SystemConfig \_ IDEChannel** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemConfig \_ IDEChannel** tiene estas propiedades.

<dl> <dt>

**DeviceTimingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Format("x")
</dt> </dl>

Modo en el que el IDE podría funcionar. Los posibles valores son los siguientes:

-   PIO \_ MODE0 (0x1)
-   PIO \_ MODE1 (0x2)
-   PIO \_ MODE2 (0x4)
-   PIO \_ MODE3 (0x8)
-   PIO \_ MODE4 (0x10)
-   SWDMA \_ MODE0 (0x20)
-   SWDMA \_ MODE1 (0x40)
-   SWDMA \_ MODE2 (0x80)
-   MODE0 \_ deMWDMA (0x100)
-   MODE2 deMWDMA \_ (0x200)
-   MODE3 deMWDMA \_ (0x400)
-   UDMA \_ MODE0 (0x800)
-   UDMA \_ MODE1 (0x1000)
-   UDMA \_ MODE2 (0x2000)
-   UDMA \_ MODE3 (0x4000)
-   UDMA \_ MODE4 (0x8000)
-   UDMA \_ MODE5 (0x10000)

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Format("x")
</dt> </dl>

Tipo de dispositivo. Los posibles valores son los siguientes:

-   ATA (1)
-   ATAPI (2)

</dd> <dt>

**LocationInformation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Canal IDE (por ejemplo, Canal principal, Canal secundario, y así sucesivamente).

</dd> <dt>

**LocationInformationLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

Longitud de la **cadena LocationInformation.**

</dd> <dt>

**TargetId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Identificador del disco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




