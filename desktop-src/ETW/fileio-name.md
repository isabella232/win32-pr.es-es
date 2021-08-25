---
description: 'FileIo_Name clase : esta clase es la clase de tipo de evento para eventos de E/S de archivo. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: FileIo_Name clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 147e7fd2cb28f7245d8366dc66d7b3859f37586f1bd7c9c0b96d2d7ef57e35d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829717"
---
# <a name="fileio_name-class"></a>FileIo \_ Name (clase)

Esta clase es la clase de tipo de evento para eventos de E/S de archivo.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Miembros

La **clase FileIo \_ Name** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase FileIo \_ Name** tiene estas propiedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Ruta de acceso completa al archivo, sin incluir la letra de unidad.

</dd> <dt>

FileObject
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Coincide con el valor de este puntero con el valor de puntero **FileObject** de un [**evento DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar el tipo de operación de E/S.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**Windows Server 2003:** Para recuperar la letra de unidad de la ruta de acceso del nombre de archivo, use el valor de la propiedad **FileObject** para asignar al evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) correspondiente. En el evento DiskIo TypeGroup1, use los valores de propiedad \_ **DiskNumber** y **ByteOffset** para asignar al evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondiente (**ByteOffset** se asigna a **StartOffset**). La **propiedad DriveLetterString** contiene la letra de unidad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




