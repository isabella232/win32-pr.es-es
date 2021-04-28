---
description: 'SystemConfig_Services clase : esta clase es la clase de tipo de evento para los eventos de configuración del servicio.'
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106063"
---
# <a name="systemconfig_services-class"></a>Clase SystemConfig \_ Services

Esta clase es la clase de tipo de evento para los eventos de configuración del servicio.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>Miembros

La **clase SystemConfig \_ Services** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemConfig \_ Services** tiene estas propiedades.

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Nombre para mostrar del servicio. El nombre se conserva en el Administrador de control de servicios. Sin embargo, las comparaciones de nombres para mostrar siempre se realizan sin distinción entre mayúsculas y minúsculas.

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1), **Format("x")**
</dt> </dl>

Identificador del proceso en el que se ejecuta el servicio.

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Nombre del proceso en el que se ejecuta el servicio.

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**
</dt> </dl>

Identificador único del servicio. El identificador proporciona una indicación de la funcionalidad que proporciona el servicio.

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2), **Format("x")**
</dt> </dl>

Estado actual del servicio. Para ver los valores posibles, vea el **miembro dwCurrentState** de **SERVICE STATUS \_ \_ PROCESS**.

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3), **Format("x")**
</dt> </dl>

Identifica el servicio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




