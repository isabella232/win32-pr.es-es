---
description: El tipo de \_ enumeración WPD CAPTURE \_ MODES describe el modo de tiempo de captura de una captura de imagen fija.
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
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572008"
---
# <a name="wpd_capture_modes-enumeration"></a>Enumeración WPD \_ CAPTURE \_ MODES

El **tipo de \_ enumeración WPD CAPTURE \_ MODES** describe el modo de tiempo de captura de una captura de imagen fija.

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

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**MODO DE \_ CAPTURA \_ WPD \_ SIN DEFINIR**
</dt> <dd>

No se ha definido el modo de captura.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**MODO DE \_ CAPTURA \_ WPD \_ NORMAL**
</dt> <dd>

No se debe usar ningún modo de retraso o ráfaga.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**RÁFAGA DEL \_ MODO \_ DE CAPTURA DE WPD \_**
</dt> <dd>

Especifica que se debe capturar un número definido de imágenes con un intervalo definido entre ellas. El número de imágenes que se van a capturar y el retraso de tiempo entre ellas se especifican mediante las propiedades [WPD \_ STILL IMAGE BURST \_ \_ \_ NUMBER](still-image-properties.md) y [WPD STILL IMAGE BURST \_ \_ \_ \_ INTERVAL.](still-image-properties.md)

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**MODO DE \_ CAPTURA \_ DE \_ WPD TIMELAPSE**
</dt> <dd>

La captura de imágenes debe usar el intervalo de tiempo. El número de imágenes y el intervalo entre ellas se describen mediante las propiedades [WPD \_ STILL IMAGE \_ \_ TIMELAPSE \_ NUMBER](still-image-properties.md) y [WPD STILL IMAGE \_ \_ \_ TIMELAPSE \_ INTERVAL.](still-image-properties.md)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración la usa la [propiedad \_ WPD STILL \_ IMAGE CAPTURE \_ \_ MODE.](still-image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




