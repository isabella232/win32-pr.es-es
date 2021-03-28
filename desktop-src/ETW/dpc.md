---
description: Esta clase es la clase de tipo de evento para los eventos de llamada a procedimiento diferido (DPC) del dispositivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Clase DPC
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
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907710"
---
# <a name="dpc-class"></a>Clase DPC

Esta clase es la clase de tipo de evento para los eventos de llamada a procedimiento diferido (DPC) del dispositivo.

La siguiente sintaxis se simplifica desde el código MOF.

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

La clase **DPC** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **DPC** tiene estas propiedades.

<dl> <dt>

**InitialTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), extensión ("WmiTime")
</dt> </dl>

Hora de entrada de DPC.

</dd> <dt>

**Rutina**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Dirección de la rutina de DPC. Use la dirección con los eventos de imagen para buscar la imagen que se ha iniciado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos eventos se registran cuando se introduce un DPC. Estos eventos se usan para supervisar y comprobar el comportamiento de los controladores y los componentes de modo kernel. Por ejemplo, puede usar los eventos DPC, ISR y imagen para determinar los componentes que emplean demasiado tiempo en los niveles de interrupción altos. Los eventos de DPC y ISR tienen una marca de tiempo de entrada que se utiliza para calcular la duración de las rutinas. Los eventos de imagen se leen para construir las regiones de memoria que se asignan a determinados módulos. Puede usar la asignación para buscar el módulo que contiene la rutina de interrupción.

El evento TimerDPC se registra cuando un DPC se desencadena como resultado de una expiración del temporizador y el evento ThreadDPC se registra cuando se ejecuta un DPC enlazado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




