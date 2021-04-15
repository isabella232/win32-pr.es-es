---
description: Esta clase es la clase de tipo de evento para el evento de creación de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: FileIo_Create (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984491"
---
# <a name="fileio_create-class"></a>\_Clase de creación FileIo

Esta clase es la clase de tipo de evento para el evento de creación de archivo.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a>Miembros

La clase **FileIo \_ Create** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **FileIo \_ Create** tiene estas propiedades.

<dl> <dt>

**CreateOptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

Los valores que se pasan en los parámetros *CreateOptions* y *CreateDispositions* a la función [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**FileAttributes**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (5)
</dt> </dl>

Valor pasado en el parámetro *FileAttributes* a la función [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

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

**OpenPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Ruta de acceso al archivo.

</dd> <dt>

**ShareAccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (6)
</dt> </dl>

Valor pasado en el parámetro *ShareAccess* a la función [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Identificador de subproceso del subproceso que está creando el archivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 
