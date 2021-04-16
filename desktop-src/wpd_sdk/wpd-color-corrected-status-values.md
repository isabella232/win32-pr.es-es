---
description: El \_ \_ \_ \_ tipo de enumeración valores de estado corregidos en color de WPD describe el estado de corrección del color de un archivo de imagen o vídeo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Enumeración WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718897"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>\_ \_ \_ Enumeración de valores de estado corregidos en color de WPD \_

El tipo de enumeración **\_ \_ \_ \_ valores de estado corregidos en color de WPD** describe el estado de corrección del color de un archivo de imagen o vídeo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_Estado corregido de color de WPD \_ \_ \_ no \_ corregido**
</dt> <dd>

No se ha corregido el color de la imagen.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**se \_ \_ corrigió el \_ Estado corregido de color de WPD \_**
</dt> <dd>

Se corrigió el color de la imagen.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**el \_ Estado corrección del color de WPD \_ \_ \_ \_ no debe \_ \_ corregirse**
</dt> <dd>

La imagen no ha sido, y no debe ser, se ha corregido el color.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica el estado de corrección del color de una imagen. Esta enumeración se usa en la propiedad de [ \_ \_ \_ \_ Estado corrección de color de imagen de WPD](image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




