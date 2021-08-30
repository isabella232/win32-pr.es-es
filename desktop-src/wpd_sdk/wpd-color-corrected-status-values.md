---
description: El tipo de \_ enumeración WPD COLOR CORRECTED STATUS VALUES describe el estado de corrección \_ de color de un archivo de imagen o \_ \_ vídeo.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: WPD_COLOR_CORRECTED_STATUS_VALUES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 94caa345c0c7bee6c500109d6ebc6cbedd0aefae5254a254dbc5af907e0be737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089595"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>Enumeración \_ WPD COLOR \_ CORRECTED \_ STATUS \_ VALUES

El **tipo de \_ enumeración WPD COLOR \_ CORRECTED STATUS \_ \_ VALUES** describe el estado de corrección de color de un archivo de imagen o vídeo.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**ESTADO CORRECTO \_ DEL COLOR \_ WPD NO \_ \_ \_ CORREGIDO**
</dt> <dd>

No se ha corregido el color de la imagen.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**ESTADO CORRECTO \_ DEL COLOR \_ WPD \_ \_ CORREGIDO**
</dt> <dd>

Se ha corregido el color de la imagen.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**EL \_ ESTADO CORRECTO DEL COLOR \_ WPD \_ NO DEBE \_ \_ \_ \_ CORREGIRSE**
</dt> <dd>

No se ha corregido el color de la imagen ni debe corregirse.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Indica el estado corregido del color de una imagen. Esta enumeración la usa la propiedad [ \_ WPD IMAGE \_ COLOR \_ CORRECTED \_ STATUS.](image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




