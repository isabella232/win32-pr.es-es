---
description: Esta clase es la clase de tipo de evento para los eventos de carga de la imagen. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984219"
---
# <a name="image_v1_load-class"></a>Clase de carga de la imagen \_ v1 \_

Esta clase es la clase de tipo de evento para los eventos de carga de la imagen.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>Miembros

La clase de **\_ \_ carga de la imagen v1** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ \_ carga de la imagen v1** tiene estas propiedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nombre de archivo y extensión del archivo DLL o la imagen ejecutable que se va a cargar.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección base de la aplicación en la que se carga la imagen.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), puntero
</dt> </dl>

Tamaño de la imagen que se está cargando.

Al utilizar esta propiedad, el tamaño del tipo de datos de esta propiedad es realmente \_ t. El calificador de puntero se usa para determinar si el tamaño \_ t es de 4 bytes o de 8 bytes.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

Identifica el proceso en el que se carga la imagen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Imagen \_ v1**](image-v1.md)
</dt> </dl>

 

 




