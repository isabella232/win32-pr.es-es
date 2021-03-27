---
description: Esta clase es la clase de tipo de evento para los eventos de e/s de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082943"
---
# <a name="fileio_v1_name-class"></a>\_Clase de \_ nombre FileIo v1

Esta clase es la clase de tipo de evento para los eventos de e/s de archivo.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Miembros

La clase de **\_ \_ nombre FileIo v1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ \_ nombre FileIo v1** tiene estas propiedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Ruta de acceso completa al archivo, sin incluir la letra de unidad.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento [**desmontaje \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de e/s.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Windows Server 2003:** Para recuperar la letra de unidad de la ruta de acceso del nombre de archivo, use el valor de la propiedad **FileObject** para asignar al evento [ \_ TypeGroup1 de desmontaje](diskio-typegroup1.md) correspondiente. En el \_ evento desmontaje TypeGroup1, use los valores de las propiedades **Númerodedisco corresponde** y **byteoffset (** para asignar al evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondiente (**byteoffset (** se asigna a **StartOffset**). La propiedad **DriveLetterString** contiene la letra de unidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




