---
description: Representa la clase de tipo de evento para los eventos de tipo de objeto relacionados con el principio y el final de la recopilación de datos.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Clase ObTypeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3659d89baa94da0c3161f7bcd6c9ff94d27efef467af8caafa70adfe1c4a7b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070061"
---
# <a name="obtypeevent-class"></a>Clase ObTypeEvent

Representa la clase de tipo de evento para los eventos de tipo de objeto relacionados con el principio y el final de la recopilación de datos. Este evento implica la asignación de los valores de índice de tipo a los nombres de tipo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a>Miembros

La **clase ObTypeEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase ObTypeEvent** tiene estas propiedades.

<dl> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Tipo del objeto.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Reservado.

</dd> <dt>

**TypeName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Nombre del tipo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |



 

 




