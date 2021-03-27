---
description: Esta clase es la clase de tipo de evento para los eventos de finalización de operación de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: FileIo_OpEnd (clase)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816262"
---
# <a name="fileio_opend-class"></a>FileIo ( \_ clase abierta)

Esta clase es la clase de tipo de evento para los eventos de finalización de operación de archivo.

La siguiente sintaxis se simplifica desde el código MOF.

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

## <a name="members"></a>Miembros

La **clase \_ abierta FileIo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ abierta FileIo** tiene estas propiedades.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Información adicional devuelta por el sistema de archivos para la operación. Por ejemplo, para una solicitud de lectura, el número real de bytes leídos.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Paquete de solicitud de e/s. Esta propiedad identifica la actividad de e/s que está finalizando.

</dd> <dt>

**NtStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Valor devuelto de la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los eventos [**FileIo**](fileio.md) se registran al principio de la operación. Los eventos abiertos se pueden habilitar por separado para indicar el final de esas operaciones. IRP se puede usar para poner en correlación los eventos de inicio y fin.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




