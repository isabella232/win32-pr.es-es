---
description: Esta clase es la clase de tipo de evento para los eventos de la rutina de servicio de interrupción (ISR). La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985598"
---
# <a name="isr-class"></a>ISR (clase)

Esta clase es la clase de tipo de evento para los eventos de la rutina de servicio de interrupción (ISR).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a>Miembros

La clase **ISR** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **ISR** tiene estas propiedades.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), extensión ("WmiTime")
</dt> </dl>

Hora de entrada de ISR.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5), puntero
</dt> </dl>

Reservado.

</dd> <dt>

**ReturnValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Valor booleano que indica si se ha reclamado la interrupción (es true si se ha reclamado la interrupción).

</dd> <dt>

**Rutina**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Dirección de la rutina de ISR. Use la dirección con los eventos de imagen para buscar la imagen que se ha iniciado.

</dd> <dt>

**Vector**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Vector de la tabla de descriptores de interrupción a la que se asigna la rutina de ISR.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




