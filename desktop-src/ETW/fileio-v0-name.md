---
description: La \_ \_ clase de nombre FileIo V0 es una versión anterior de la clase de tipo de evento para los eventos de e/s de archivo. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: FileIo_V0_Name (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816259"
---
# <a name="fileio_v0_name-class"></a>\_Clase de \_ nombre V0 FileIo

La clase de **\_ \_ nombre FileIo V0** es una versión anterior de la clase de tipo de evento para los eventos de e/s de archivo.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Miembros

La clase de **\_ \_ nombre FileIo V0** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ \_ nombre FileIo V0** tiene estas propiedades.

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

**Windows Server 2003:** Para recuperar la letra de unidad de la ruta de acceso del nombre de archivo, use el valor de la propiedad **FileObject** para asignar al evento [**\_ TypeGroup1 de desmontaje**](diskio-typegroup1.md) correspondiente. En el **evento \_ desmontaje TypeGroup1** , use los valores de las propiedades **númerodedisco corresponde** y **byteoffset (** para asignar al evento [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) correspondiente. La propiedad **DriveLetterString** contiene la letra de unidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo \_ v0**](fileio-v0.md)
</dt> </dl>

 

 




