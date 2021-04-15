---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de energía. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984394"
---
# <a name="systemconfig_v0_power-class"></a>\_ \_ Clase Power de SystemConfig v0

Esta clase es la clase de tipo de evento para los eventos de configuración de energía.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a>Miembros

La **clase \_ \_ Power de SystemConfig V0** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ \_ Power de SystemConfig V0** tiene estas propiedades.

<dl> <dt>

Pad1
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6)
</dt> </dl>

Reservado.

</dd> <dt>

Pad2
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (7)
</dt> </dl>

Reservado.

</dd> <dt>

Pad3
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (8)
</dt> </dl>

Reservado.

</dd> <dt>

s1
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1)
</dt> </dl>

True indica que el sistema admite el estado de suspensión S1.

</dd> <dt>

s2
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

True indica que el sistema admite el estado de suspensión S2.

</dd> <dt>

s3
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

True indica que el sistema admite el estado de suspensión S3.

</dd> <dt>

S4
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

True indica que el sistema admite el estado de suspensión S4.

</dd> <dt>

S5
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5)
</dt> </dl>

True indica que el sistema admite el estado de suspensión S5.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




