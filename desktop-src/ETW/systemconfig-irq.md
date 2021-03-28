---
description: Esta clase es la clase de tipo de evento para eventos de solicitud de interrupción (IRQ). La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: SystemConfig_IRQ (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984455"
---
# <a name="systemconfig_irq-class"></a>SystemConfig ( \_ clase de IRQ)

Esta clase es la clase de tipo de evento para eventos de solicitud de interrupción (IRQ).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a>Miembros

La **clase \_ IRQ SystemConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ IRQ SystemConfig** tiene estas propiedades.

<dl> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Descripción del dispositivo o software que realiza la solicitud.

</dd> <dt>

**DeviceDescriptionLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Longitud, en caracteres, de la cadena en **DeviceDescription**.

</dd> <dt>

**IRQAffinity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), Format ("x")
</dt> </dl>

Máscara de afinidad de IRQ. La máscara de afinidad identifica los procesadores (o grupos de procesadores) específicos que pueden recibir la IRQ.

</dd> <dt>

**IRQNum**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Número de línea de solicitud de interrupción.

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

 

 




