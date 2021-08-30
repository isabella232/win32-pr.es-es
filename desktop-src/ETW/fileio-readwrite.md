---
description: Esta clase es la clase de tipo de evento para eventos de lectura y escritura de archivos. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: FileIo_ReadWrite clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: d265bd5927f8d8b433c1a489886c6f651a595670e4c61c1073481d47601efc40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041955"
---
# <a name="fileio_readwrite-class"></a>Clase FileIo \_ ReadWrite

Esta clase es la clase de tipo de evento para eventos de lectura y escritura de archivos.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a>Miembros

La **clase FileIo \_ ReadWrite** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase FileIo \_ ReadWrite** tiene estas propiedades.

<dl> <dt>

**FileKey**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(5), Pointer
</dt> </dl>

Para determinar el nombre de archivo, haga coincidir el valor de esta propiedad con la **propiedad FileObject** de un [**evento FileIo \_ Name.**](fileio-name.md)

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Pointer
</dt> </dl>

Identificador que se puede usar para correlacionar las operaciones con la misma instancia de objeto de archivo abierta entre eventos de creación y cierre de archivos.

</dd> <dt>

**IoFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(7)
</dt> </dl>

Marcas de paquetes de solicitud de E/S especificadas para esta operación.

</dd> <dt>

**IoSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(6)
</dt> </dl>

Número de bytes solicitados.

</dd> <dt>

**IrpPtr**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Paquete de solicitud de E/S. Esta propiedad identifica la actividad de E/S.

</dd> <dt>

**Offset**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Desplazamiento de archivo inicial para la operación solicitada.

</dd> <dt>

**TTID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Pointer
</dt> </dl>

Identificador de subproceso del subproceso que realiza la operación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




