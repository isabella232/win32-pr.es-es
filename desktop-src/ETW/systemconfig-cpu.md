---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de la CPU.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: SystemConfig_CPU (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985695"
---
# <a name="systemconfig_cpu-class"></a>\_Clase de CPU SystemConfig

Esta clase es la clase de tipo de evento para los eventos de configuración de la CPU.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a>Miembros

La clase de **\_ CPU SystemConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ CPU SystemConfig** tiene estas propiedades.

<dl> <dt>

**AllocationGranularity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5)
</dt> </dl>

Granularidad con la que se asigna la memoria virtual.

</dd> <dt>

**nombreDeEquipo**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **Max** (256), **Format ("s")**
</dt> </dl>

Nombre del equipo.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **char16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (7), **Max** (132), **Format ("s")**
</dt> </dl>

Nombre del dominio al que pertenece el equipo.

</dd> <dt>

**HyperThreadingFlag**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (8), puntero
</dt> </dl>

Indica si la opción de Hyper-Threading está activada o desactivada para un procesador. Cada bit refleja el estado de Hyper-Threading de una CPU del equipo.

</dd> <dt>

**MemSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3)
</dt> </dl>

Cantidad total de memoria física disponible para el sistema operativo.

</dd> <dt>

**MHz**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1)
</dt> </dl>

Velocidad máxima del procesador, en megahercios.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2)
</dt> </dl>

Número de procesadores del equipo.

</dd> <dt>

**PageSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4)
</dt> </dl>

Tamaño de una página de intercambio, en bytes.

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

 

 




