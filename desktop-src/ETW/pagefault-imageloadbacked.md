---
description: Esta clase es la clase de tipo de evento para cargar la imagen en eventos de archivo de paginación. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: PageFault_ImageLoadBacked (clase)
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
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985703"
---
# <a name="pagefault_imageloadbacked-class"></a>Errores \_ ImageLoadBacked (clase)

Esta clase es la clase de tipo de evento para cargar la imagen en eventos de archivo de paginación.

La siguiente sintaxis se simplifica desde el código MOF.

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

La clase **errores \_ ImageLoadBacked** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **errores \_ ImageLoadBacked** tiene estas propiedades.

<dl> <dt>

**DeviceChar**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2), Format ("x")
</dt> </dl>

Reservado.

</dd> <dt>

**FileChar**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3), Format ("x")
</dt> </dl>

Reservado.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1), puntero
</dt> </dl>

Haga coincidir el valor de este puntero con el valor del puntero **FileObject** en un evento de [**\_ nombre FileIo**](fileio-name.md) para determinar el nombre del archivo.

</dd> <dt>

**LoadFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4), formato ("x")
</dt> </dl>

Reservado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El evento se registra durante la creación de una sección de imagen (por ejemplo, una carga de DLL) cuando el administrador de memoria determina que la imagen debe copiarse y ejecutarse desde el archivo de paginación. Normalmente, las imágenes se ejecutan desde el archivo de código fuente, pero el respaldo del archivo de paginación se puede producir cuando el administrador de memoria determina que el archivo de origen puede ser modificado de forma asincrónica por los escritores existentes o cuando el archivo de origen se encuentra en un medio extraíble o en un dispositivo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Errores \_ V2**](pagefault-v2.md)
</dt> </dl>

 

 




