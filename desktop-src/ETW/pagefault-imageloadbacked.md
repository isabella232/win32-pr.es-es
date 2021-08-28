---
description: Esta clase es la clase de tipo de evento para la carga de imágenes en eventos de archivo de página. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75104fcf923ed59bfcc99e214e66a235549b7059ca0e36c41b6f90d308a3efff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811775"
---
# <a name="pagefault_imageloadbacked-class"></a>PageFault \_ ImageLoadBacked (clase)

Esta clase es la clase de tipo de evento para la carga de imágenes en eventos de archivo de página.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>Miembros

La **clase PageFault \_ ImageLoadBacked** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase PageFault \_ ImageLoadBacked** tiene estas propiedades.

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2), Format("x")
</dt> </dl>

Reservado.

</dd> <dt>

**FileChar**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3), Format("x")
</dt> </dl>

Reservado.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1), Pointer
</dt> </dl>

Coincide con el valor de este puntero con el valor del puntero **FileObject** en un [**evento FileIo \_ Name**](fileio-name.md) para determinar el nombre del archivo.

</dd> <dt>

**LoadFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4), Format("x")
</dt> </dl>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El evento se registra durante la creación de una sección de imagen (por ejemplo, una carga dll) cuando el administrador de memoria determina que la imagen debe copiarse y ejecutarse desde el archivo de página. Normalmente, las imágenes se ejecutan desde el archivo de origen, pero la copia de seguridad de archivos de página puede producirse cuando el administrador de memoria determina que los escritores existentes pueden modificar el archivo de origen de forma asincrónica o cuando el archivo de origen está en un medio extraíble o un dispositivo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PageFault \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




