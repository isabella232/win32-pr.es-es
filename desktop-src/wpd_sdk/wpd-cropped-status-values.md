---
description: El tipo de enumeración \_ WPD CROPPED \_ STATUS VALUES describe el estado de recorte de una \_ imagen.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: WPD_CROPPED_STATUS_VALUES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 881fcde3a6da5f649190f12be7df760c584934deba2a769353798b695292c638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652709"
---
# <a name="wpd_cropped_status_values-enumeration"></a>Enumeración \_ WPD CROPPED \_ STATUS \_ VALUES

El **tipo de enumeración \_ WPD CROPPED \_ STATUS \_ VALUES** describe el estado de recorte de una imagen.

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**ESTADO RECORTADO DE WPD \_ \_ NO \_ \_ RECORTADO**
</dt> <dd>

La imagen no se ha recortado.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**ESTADO RECORTADO DE WPD \_ \_ \_ RECORTADO**
</dt> <dd>

La imagen se ha recortado.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**EL ESTADO RECORTADO DE WPD \_ \_ NO DEBE \_ \_ \_ \_ RECORTARSE**
</dt> <dd>

La imagen no se ha recortado ni debe estar recortada.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Indica el estado recortado de una imagen. Esta enumeración la usa la [propiedad \_ WPD IMAGE \_ CROPPED \_ STATUS.](image-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




