---
description: El \_ \_ \_ tipo de enumeración recortes de valores de estado de WPD describe el estado de recorte de una imagen.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Enumeración WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678933"
---
# <a name="wpd_cropped_status_values-enumeration"></a>\_ \_ Enumeración de valores de estado recortados de WPD \_

El tipo de enumeración **\_ recortes de \_ \_ valores de estado de WPD** describe el estado de recorte de una imagen.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_Estado recortado de WPD \_ \_ no \_ recortado**
</dt> <dd>

La imagen no se ha recortado.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**\_Estado recortado de WPD recortado \_ \_**
</dt> <dd>

La imagen se ha recortado.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_ \_ \_ \_ no \_ se debe \_ recortar el estado recortado de WPD**
</dt> <dd>

La imagen no ha sido y no debe recortarse.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Indica el estado recortado de una imagen. Esta enumeración se usa en la propiedad [ \_ \_ \_ Estado recortado de imagen de WPD](image-properties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




