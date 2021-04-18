---
description: El \_ \_ tipo de enumeración de modos de captura de WPD describe el modo de control de tiempo de captura de una captura de imagen fija.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Enumeración WPD_CAPTURE_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718707"
---
# <a name="wpd_capture_modes-enumeration"></a>\_Enumeración de modos de captura de WPD \_

El tipo de enumeración de **\_ \_ modos de captura de WPD** describe el modo de control de tiempo de captura de una captura de imagen fija.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**modo de captura de WPD \_ \_ \_ sin definir**
</dt> <dd>

No se ha definido el modo de captura.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**modo de captura de WPD \_ \_ \_ normal**
</dt> <dd>

No se debe usar ningún retraso ni modo de ráfaga.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**ráfaga en el modo de captura de WPD \_ \_ \_**
</dt> <dd>

Especifica que se debe capturar un número definido de imágenes con un intervalo definido entre ellas. El número de imágenes que se van a capturar y el tiempo de retardo entre ellas se especifican mediante las propiedades de número de ráfaga de imagen de la [ \_ \_ \_ \_ imagen de WPD](still-image-properties.md) y de [ \_ \_ \_ \_ intervalo de ráfaga de imagen](still-image-properties.md) .

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**modo de captura de WPD \_ \_ \_ TIMELAPSE**
</dt> <dd>

La captura de imagen debe usar la fotografía de lapso de tiempo. El número de imágenes y el intervalo entre ellas se describen en las propiedades del intervalo [ \_ \_ \_ TIMELAPSE \_ ](still-image-properties.md) y de la imagen estática de WPD y de la [ \_ imagen de \_ \_ TIMELAPSE \_ ](still-image-properties.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la propiedad de modo de captura de imagen de la [ \_ \_ imagen \_ \_ de WPD](still-image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




