---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl.h)
description: La transición de iris revela la nueva imagen a lo largo de un eje X y un eje Y. El efecto visual de esta transición es que la nueva imagen aparece en un cruce de ampliación que llega a todos los lados del marco.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919af0b15ef8a7437c9852df3ff12623553cdabf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472971"
---
# <a name="wmt_videoimage_transition_iris"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ IRIS

La transición de iris revela la nueva imagen a lo largo de un eje X y un eje Y. El efecto visual de esta transición es que la nueva imagen aparece en un cruce de ampliación que llega a todos los lados del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que se asignan.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Centrar X | <strong>fEffectPara0</strong> | Coordenada X, en relación con el fotograma de vídeo, del centro del efecto iris. | 
| Centrar Y | <strong>fEffectPara1</strong> | Coordenada Y, en relación con el fotograma de vídeo, del centro del efecto iris. | 
| Ancho | <strong>fEffectPara2</strong> | Ancho de la línea vertical que revela la nueva imagen, en píxeles. | 
| Alto | <strong>fEffectPara3</strong> | Alto de la línea horizontal que revela la nueva imagen, en píxeles. | 
| Composición | <strong>fEffectPara4</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





