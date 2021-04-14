---
description: Esta clase es la clase de tipo de evento para eventos de perfil muestreados. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Clase SampledProfile
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
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985938"
---
# <a name="sampledprofile-class"></a>Clase SampledProfile

Esta clase es la clase de tipo de evento para eventos de perfil muestreados.

La siguiente sintaxis se simplifica desde el código MOF.

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

La clase **SampledProfile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SampledProfile** tiene estas propiedades.

<dl> <dt>

**Recuento**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

No se utiliza.

</dd> <dt>

**InstructionPointer**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección de la imagen que se estaba ejecutando en el momento en que se muestrea el procesador.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Identificador de subproceso del subproceso que se estaba ejecutando en el momento en que se muestrea el procesador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos eventos proporcionan un perfil de ejecución muestreado. El evento registra lo que se estaba ejecutando en el procesador. Puede usar los eventos de imagen para identificar el módulo binario que contiene esa instrucción. Después, puede usar esta información para generar un perfil de ejecución mientras dure el seguimiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




