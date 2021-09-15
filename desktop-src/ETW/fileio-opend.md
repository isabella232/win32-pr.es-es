---
description: Esta clase es la clase de tipo de evento para los eventos de finalización de la operación de archivo. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476917"
---
# <a name="fileio_opend-class"></a>Clase FileIo \_ OpEnd

Esta clase es la clase de tipo de evento para los eventos de finalización de la operación de archivo.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a>Members

La **clase FileIo \_ OpEnd** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase FileIo \_ OpEnd** tiene estas propiedades.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Información adicional devuelta por el sistema de archivos para la operación. Por ejemplo, para una solicitud de lectura, el número real de bytes que se leyeron.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Paquete de solicitud de E/S. Esta propiedad identifica la actividad de E/S que está finalizando.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Valor devuelto de la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**Los eventos FileIo**](fileio.md) se registran al principio de la operación. Los eventos OpEnd se pueden habilitar por separado para indicar el final de esas operaciones. Irp se puede usar para correlacionar los eventos de inicio y finalización.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




