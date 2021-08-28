---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl.h)
description: La transición del rectángulo revela la nueva imagen en un rectángulo dentro del marco.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8721455c09a263d9c856358d2ca55bb818ac48e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467402"
---
# <a name="wmt_videoimage_transition_rectangle"></a>RECTÁNGULO DE TRANSICIÓN \_ DE VIDEOIMAGE \_ DE WMT \_

La transición del rectángulo revela la nueva imagen en un rectángulo dentro del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Centrar X | <strong>fEffectPara0</strong> | Coordenada X, relativa al marco de vídeo, del centro del rectángulo. | 
| Centrar Y | <strong>fEffectPara1</strong> | Coordenada Y, con respecto al marco de vídeo, del centro del rectángulo. | 
| Ancho | <strong>fEffectPara2</strong> | Ancho del rectángulo en píxeles. | 
| Alto | <strong>fEffectPara3</strong> | Alto del rectángulo en píxeles. | 
| Composición | <strong>fEffectPara4</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





