---
description: Esta clase es la clase de tipo de evento para los eventos de carga de la imagen. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Image_V0_Load (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984222"
---
# <a name="image_v0_load-class"></a>Image \_ V0 \_ Load (clase)

Esta clase es la clase de tipo de evento para los eventos de carga de la imagen.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a>Miembros

La clase **Image \_ V0 \_ Load** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **Image \_ V0 \_ Load** tiene estas propiedades.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Dirección base de la aplicación en la que se carga la imagen.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nombre de archivo y extensión del archivo DLL o la imagen ejecutable que se va a cargar.

</dd> <dt>

Módulos
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Tamaño de la imagen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Imagen \_ v0**](image-v0.md)
</dt> </dl>

 

 




