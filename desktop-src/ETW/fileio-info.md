---
description: Esta clase es la clase de tipo de evento para el evento de información de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: FileIo_Info (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985846"
---
# <a name="fileio_info-class"></a>\_Clase de información FileIo

Esta clase es la clase de tipo de evento para el evento de información de archivo.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a>Miembros

La clase de **\_ información FileIo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ información FileIo** tiene estas propiedades.

<dl> <dt>

**ExtraInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5), puntero
</dt> </dl>

En el caso de las solicitudes FileDispositionInformation, este campo contiene la disposición solicitada. En el caso de las solicitudes FileEndOfFileInformation y FileAllocationInformation, este campo contiene el tamaño de archivo especificado.

</dd> <dt>

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

**InfoClass**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6)
</dt> </dl>

Clase de información de archivo solicitada.

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

Establecer información y eventos de información de consulta indica que los atributos de archivo se han establecido o consultado. Cuando se emite un comando FSCTL, se registra un evento de control del sistema de archivos (FSControl).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




