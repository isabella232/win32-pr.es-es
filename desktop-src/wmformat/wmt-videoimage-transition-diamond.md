---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl.h)
description: La transición de rombo revela la nueva imagen en un rombo.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38731c93ae9ada520f286ae1662d45ec95d399d4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473501"
---
# <a name="wmt_videoimage_transition_diamond"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAMOND

La transición de rombo revela la nueva imagen en un rombo.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Centrar X | <strong>fEffectPara0</strong> | Coordenada X, en relación con el fotograma de vídeo, del centro del rombo. | 
| Centrar Y | <strong>fEffectPara1</strong> | Coordenada Y, en relación con el fotograma de vídeo, del centro del rombo. | 
| Ancho | <strong>fEffectPara2</strong> | Ancho del rombo en píxeles. | 
| Alto | <strong>fEffectPara3</strong> | Alto del rombo en píxeles. | 
| Composición | <strong>fEffectPara4</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





