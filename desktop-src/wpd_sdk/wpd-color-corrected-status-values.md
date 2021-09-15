---
description: El tipo de \_ enumeración WPD COLOR CORRECTED STATUS VALUES describe el estado de corrección \_ de color de una imagen o un archivo de \_ \_ vídeo.
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
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572005"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>Enumeración \_ WPD COLOR \_ CORRECTED \_ STATUS \_ VALUES

El **tipo de \_ enumeración WPD COLOR \_ CORRECTED STATUS \_ \_ VALUES** describe el estado de corrección de color de una imagen o un archivo de vídeo.

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

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**ESTADO CORREGIDO \_ DEL COLOR \_ WPD NO \_ \_ \_ CORREGIDO**
</dt> <dd>

No se ha corregido el color de la imagen.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**SE \_ CORRIGIÓ \_ EL ESTADO CORREGIDO DEL \_ COLOR \_ WPD**
</dt> <dd>

Se ha corregido el color de la imagen.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**EL \_ ESTADO CORRECTO DEL COLOR \_ WPD \_ NO DEBE \_ \_ \_ \_ CORREGIRSE**
</dt> <dd>

La imagen no se ha corregido y no debe ser de color.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica el estado de color corregido de una imagen. Esta enumeración la usa la propiedad [ \_ WPD IMAGE \_ COLOR \_ CORRECTED \_ STATUS.](image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




