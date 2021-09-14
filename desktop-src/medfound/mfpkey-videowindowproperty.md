---
description: Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: MFPKEY_VIDEOWINDOW (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268807"
---
# <a name="mfpkey_videowindow-property"></a>Propiedad VIDEOWINDOW de MFPKEY \_

Especifica la cantidad de contenido, en milisegundos, que puede caber en el búfer del modelo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVideoWIndow

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

3000

## <a name="remarks"></a>Observaciones

La ventana de búfer es uno de los parámetros de modelo de "cubo de fugas" usados en el control de velocidad de códecs.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Configuración de la codificación de vídeo](configuringvideoencoding.md)
</dt> <dt>

[El modelo de búfer de cubo filtrada](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




