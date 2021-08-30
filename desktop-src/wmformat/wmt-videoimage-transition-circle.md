---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Wmsdkidl.h)
description: La transición de círculo revela la nueva imagen en un círculo.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd4c2e4d40a78b10ee669a92dba7fc814fe6223
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471111"
---
# <a name="wmt_videoimage_transition_circle"></a>CÍRCULO DE TRANSICIÓN \_ DE IMAGEN DE VÍDEO DE WMT \_ \_

La transición de círculo revela la nueva imagen en un círculo.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que se asignan.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Centrar X | <strong>fEffectPara0</strong> | Coordenada X, en relación con el fotograma de vídeo, del centro del círculo. | 
| Centrar Y | <strong>fEffectPara1</strong> | Coordenada Y, en relación con el fotograma de vídeo, del centro del círculo. | 
| Radio | <strong>fEffectPara2</strong> | Radio, en píxeles, del círculo. | 
| Composición | <strong>fEffectPara3</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





