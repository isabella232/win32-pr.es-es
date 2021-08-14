---
description: Esta clase es la clase de tipo de evento para eventos de llamada a procedimiento diferido (DPC) de dispositivo. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: DPC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: ef1f0c43d8b91aec1de266176aaef254360c73c99db163280b7bb2d1cbde4832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395169"
---
# <a name="dpc-class"></a>DPC (clase)

Esta clase es la clase de tipo de evento para eventos de llamada a procedimiento diferido (DPC) de dispositivo.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a>Miembros

La **clase DPC** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DPC** tiene estas propiedades.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Extension("WmiTime")
</dt> </dl>

Hora de entrada de DPC.

</dd> <dt>

**Rutina**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Dirección de la rutina DPC. Use la dirección con los eventos Image para buscar qué imagen se inició.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Estos eventos se registran cuando se introduce un DPC. Estos eventos se usan para supervisar y comprobar el comportamiento de los controladores y los componentes en modo kernel. Por ejemplo, puede usar eventos DPC, ISR e Image para determinar los componentes que pasan demasiado tiempo en niveles de interrupción altos. Los eventos DPC e ISR tienen una marca de tiempo de entrada que se usa para calcular la duración de las rutinas. Los eventos de imagen se leen para construir las regiones de memoria que se asignan a determinados módulos. Puede usar la asignación para buscar el módulo que contiene la rutina de interrupción.

El evento TimerDPC registra cuándo se produce una activación de DPC como resultado de una expiración del temporizador y el evento ThreadDPC registra cuando se ejecuta un DPC en subproceso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




