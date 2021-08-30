---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl.h)
description: La transición de división revela la nueva imagen dividiendo la imagen anterior. La división aparece a lo largo de una línea horizontal o vertical recta a partir del marco.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8ae4e805d61ea83f2e5e6cb80d1424547be6a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474701"
---
# <a name="wmt_videoimage_transition_split"></a>DIVISIÓN DE TRANSICIÓN \_ DE WMT VIDEOIMAGE \_ \_

La transición de división revela la nueva imagen dividiendo la imagen anterior. La división aparece a lo largo de una línea horizontal o vertical recta a partir del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Centrar X | <strong>fEffectPara0</strong> | Coordenada X, en relación con el fotograma de vídeo, de la línea de origen de la división. | 
| Centrar Y | <strong>fEffectPara1</strong> | Coordenada Y, en relación con el fotograma de vídeo, de la línea de origen de la división. | 
| Distancia | <strong>fEffectPara2</strong> | Ancho de la división en píxeles. | 
| Dirección | <strong>fEffectPara3</strong> | Orientación de la división. Establezca en uno de los siguientes valores:<br /><ul><li>0: se divide a lo largo de una línea horizontal.</li><li>1 : se divide a lo largo de una línea vertical.</li></ul> | 
| Composición | <strong>fEffectPara4</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





