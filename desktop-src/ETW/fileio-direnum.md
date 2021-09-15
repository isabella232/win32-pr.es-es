---
description: Esta clase es la clase de tipo de evento para los eventos de notificación de directorio y directorio enumerados. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: FileIo_DirEnum clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476921"
---
# <a name="fileio_direnum-class"></a>Clase FileIo \_ DirEnum

Esta clase es la clase de tipo de evento para los eventos de notificación de directorio y directorio enumerados.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a>Members

La **clase FileIo \_ DirEnum** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase FileIo \_ DirEnum** tiene estas propiedades.

<dl> <dt>

**FileIndex**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7)
</dt> </dl>

Índice de archivo desde el que se va a continuar la enumeración de directorios.

</dd> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Pointer
</dt> </dl>

Para determinar el nombre del directorio, haga coincidir el valor de esta propiedad con la **propiedad FileObject** de un [**evento FileIo \_ Name.**](fileio-name.md)

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(8), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Patrón especificado para la enumeración de directorios.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Pointer
</dt> </dl>

Identificador que se puede usar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre eventos de creación y cierre de archivos.

</dd> <dt>

**InfoClass**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6), Pointer
</dt> </dl>

Clase de información de enumeración de directorios solicitada.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Paquete de solicitud de E/S. Esta propiedad identifica la actividad de E/S.

</dd> <dt>

**Duración**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5)
</dt> </dl>

Tamaño del búfer de consulta, en bytes.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Identificador de subproceso del subproceso que realiza la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los eventos de enumeración de directorios y notificación de directorio se registran cuando se enumera un directorio o se envía una notificación de cambio de directorio a los agentes de escucha registrados, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




