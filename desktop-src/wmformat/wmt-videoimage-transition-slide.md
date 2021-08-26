---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl.h)
description: La transición de diapositiva revela la nueva imagen deslizando la imagen antigua fuera del marco.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9866706528cab038042adc8d098743ce6588c805
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476341"
---
# <a name="wmt_videoimage_transition_slide"></a>DIAPOSITIVA DE TRANSICIÓN \_ DE IMAGEN DE VÍDEO \_ DE WMT \_

La transición de diapositiva revela la nueva imagen deslizando la imagen antigua fuera del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que se asignan.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Distancia | <strong>fEffectPara0</strong> | Distancia, en píxeles, que la imagen antigua se desliza fuera del marco. | 
| Dirección | <strong>fEffectPara1</strong> | Dirección en la que se desliza la imagen antigua. Establezca en uno de los siguientes valores:<br /><ul><li>0 : deslice hacia la derecha.</li><li>1 - Deslice hacia la izquierda.</li><li>2 - Deslice hacia arriba.</li><li>3 - Deslice hacia abajo.</li></ul> | 
| Composición | <strong>fEffectPara2</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





