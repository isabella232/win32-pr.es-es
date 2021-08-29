---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl.h)
description: La transición de atados de arco revela la nueva imagen en un conjunto de triángulos en los lados opuestos del marco.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b61314709f6b0000281ac54e10f8aa702a9b24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471521"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>VIDEOIMAGE \_ \_ TRANSITION \_ BOW \_ TIE DE WMT

La transición de atados de arco revela la nueva imagen en un conjunto de triángulos en los lados opuestos del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que se asignan.




| Parámetro | Miembro de estructura | Description | 
|-----------|------------------|-------------|
| Ancho | <strong>fEffectPara0</strong> | Ancho de cada lado triangular del arco. | 
| Alto | <strong>fEffectPara1</strong> | Alto de cada lado triangular del arco. | 
| Dirección | <strong>fEffectPara2</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica el efecto de atado de arco horizontal, en el que los triángulos entran desde los lados derecho e izquierdo del marco.</li><li>1 - Especifica el efecto de atados verticales, en el que los triángulos entran desde la parte superior e inferior del marco.</li></ul> | 
| Composición | <strong>fEffectPara3</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





