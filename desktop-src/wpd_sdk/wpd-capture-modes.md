---
description: El tipo de \_ enumeración WPD CAPTURE \_ MODES describe el modo de control de tiempo de captura de una captura de imagen fija.
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: WPD_CAPTURE_MODES enumeración (PortableDevice.h)
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
ms.openlocfilehash: c8bc0d667e329db3afccf76497409350d7aa7250b0e6529d0b3f4ddae7a32370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927995"
---
# <a name="wpd_capture_modes-enumeration"></a>Enumeración \_ DE MODOS DE CAPTURA DE WPD \_

El **tipo de \_ enumeración WPD CAPTURE \_ MODES** describe el modo de control de tiempo de captura de una captura de imagen fija.

## <a name="syntax"></a>Syntax


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

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**MODO DE CAPTURA DE WPD \_ \_ SIN \_ DEFINIR**
</dt> <dd>

No se ha definido el modo de captura.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**MODO DE CAPTURA \_ \_ WPD \_ NORMAL**
</dt> <dd>

No se debe usar ningún modo de retraso o ráfaga.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**RÁFAGA DEL MODO \_ DE \_ CAPTURA DE \_ WPD**
</dt> <dd>

Especifica que se debe capturar un número definido de imágenes con un intervalo definido entre ellas. El número de imágenes que se van a capturar y el retraso de tiempo entre ellas se especifican mediante las propiedades [ \_ WPD STILL \_ IMAGE BURST \_ \_ NUMBER](still-image-properties.md) y [WPD STILL IMAGE BURST \_ \_ \_ \_ INTERVAL.](still-image-properties.md)

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**TIMELAPSE EN MODO DE CAPTURA \_ \_ DE \_ WPD**
</dt> <dd>

La captura de imágenes debe usar la fotografía de intervalo de tiempo. El número de imágenes y el intervalo entre ellas se describen mediante las propiedades [ \_ WPD STILL \_ IMAGE \_ TIMELAPSE \_ NUMBER](still-image-properties.md) y [WPD \_ STILL IMAGE \_ \_ TIMELAPSE \_ INTERVAL.](still-image-properties.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la [propiedad STILL IMAGE CAPTURE MODE \_ \_ \_ \_ de WPD.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




