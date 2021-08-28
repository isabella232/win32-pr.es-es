---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl.h)
description: La transición de la rueda revela la nueva imagen girando cuatro líneas alrededor de un punto de pivote común, como los radios de una rueda.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b77e8640f21bd06194b2fe6b1e7048d85b323e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469272"
---
# <a name="wmt_videoimage_transition_wheel"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ WHEEL

La transición de la rueda revela la nueva imagen girando cuatro líneas alrededor de un punto de pivote común, como los radios de una rueda.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Centrar X | <strong>fEffectPara0</strong> | Coordenada X, en relación con el fotograma de vídeo, del centro del efecto de rueda. | 
| Centrar Y | <strong>fEffectPara1</strong> | Coordenada Y, en relación con el fotograma de vídeo, del centro del efecto de rueda. | 
| Ángulo | <strong>fEffectPara2</strong> | Ángulo de rotación, en grados, de los radios del efecto de rueda. Un valor de 0,0 indica la imagen antigua sin que se revela ninguna de las imágenes nuevas. Un valor de 90,0 indica la nueva imagen totalmente revelada. El movimiento de 0,0 a 90,0 aparece como rotación en el sentido de las agujas del reloj de los radios.<br /> | 
| Composición | <strong>fEffectPara3</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





