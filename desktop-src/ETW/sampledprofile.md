---
description: Esta clase es la clase de tipo de evento para eventos de perfil muestreados. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: SampledProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 52b0eeeff1c0640455b935cf1140ab285d937f35db02d098def39a60a06571a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041635"
---
# <a name="sampledprofile-class"></a>SampledProfile (clase)

Esta clase es la clase de tipo de evento para eventos de perfil muestreados.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a>Miembros

La **clase SampledProfile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SampledProfile** tiene estas propiedades.

<dl> <dt>

**Recuento**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

No se usa.

</dd> <dt>

**InstructionPointer**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección de la imagen que se estaba ejecutando en el momento en que se muestreó el procesador.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Identificador de subproceso del subproceso que se estaba ejecutando en el momento en que se muestreó el procesador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Estos eventos proporcionan un perfil de ejecución muestreado. El evento registra lo que se ejecutaba en el procesador. Puede usar los eventos Image para identificar el módulo binario que contiene esa instrucción. A continuación, puede usar esta información para generar un perfil de ejecución mientras dure el seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




