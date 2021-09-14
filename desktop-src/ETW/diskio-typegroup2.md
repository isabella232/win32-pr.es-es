---
description: Esta clase es la clase de tipo de evento que marca el principio de los eventos de lectura, escritura y vaciado de E/S de disco. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: DiskIo_TypeGroup2 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063148"
---
# <a name="diskio_typegroup2-class"></a>Clase \_ TypeGroup2 de DiskIo

Esta clase es la clase de tipo de evento que marca el principio de los eventos de lectura, escritura y vaciado de E/S de disco.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a>Members

La **clase \_ TypeGroup2 de DiskIo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase DiskIo \_ TypeGroup2** tiene estas propiedades.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Paquete de solicitud de E/S. Esta propiedad identifica la actividad de E/S.

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Identificador del subproceso emisor.

**Windows Server 2008 R2, Windows Server 2008, Windows 7 y Windows Vista:** Esta propiedad no se admite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




