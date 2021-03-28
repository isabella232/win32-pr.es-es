---
description: Esta clase es la clase de tipo de evento para los eventos de operación de archivo simples. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: FileIo_SimpleOp (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985842"
---
# <a name="fileio_simpleop-class"></a>\_Clase FileIo SimpleOp

Esta clase es la clase de tipo de evento para los eventos de operación de archivo simples.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a>Miembros

La clase **FileIo \_ SimpleOp** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **FileIo \_ SimpleOp** tiene estas propiedades.

<dl> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4), puntero
</dt> </dl>

Para determinar el nombre de archivo, haga coincidir el valor de esta propiedad con la propiedad **FileObject** de un evento de [**\_ nombre FileIo**](fileio-name.md) .

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3), puntero
</dt> </dl>

Identificador que se puede utilizar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre los eventos de creación y cierre de archivo.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Paquete de solicitud de e/s. Esta propiedad identifica la actividad de e/s.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Identificador de subproceso del subproceso que está realizando la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El evento de limpieza se registra cuando se cierra el último identificador del archivo. El evento Close especifica que se va a liberar un objeto de archivo. El evento Flush especifica cuándo se vacían por completo los búferes de archivo en el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




