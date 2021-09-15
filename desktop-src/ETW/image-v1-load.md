---
description: 'Image_V1_Load clase : esta clase es la clase de tipo de evento para los eventos de carga de imágenes. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Image_V1_Load clase
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
ms.openlocfilehash: 2e8a8c31cee7e45311887c16a1d10545e6a38e41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476882"
---
# <a name="image_v1_load-class"></a>Image \_ V1 \_ Load (clase)

Esta clase es la clase de tipo de evento para los eventos de carga de imágenes.

La sintaxis siguiente se simplifica a partir del código MOF.

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

## <a name="members"></a>Members

La **clase Image \_ V1 \_ Load** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Load de Image \_ V1 \_** tiene estas propiedades.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), StringTermination("NullTerminated"), Format("w")
</dt> </dl>

Nombre de archivo y extensión del archivo DLL o la imagen ejecutable que se cargará.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Dirección base de la aplicación en la que se carga la imagen.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Pointer
</dt> </dl>

Tamaño de la imagen que se está cargando.

Al consumir esta propiedad, el tipo de datos de esta propiedad es realmente de \_ tamaño t. El calificador Pointer se usa para determinar si el tamaño \_ t es de 4 bytes o 8 bytes.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Identifica el proceso en el que se carga la imagen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Imagen \_ V1**](image-v1.md)
</dt> </dl>

 

 




