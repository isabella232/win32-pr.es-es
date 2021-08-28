---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl.h)
description: La transición reveal revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140271d365d9673c948c4ff6f540e9bef33e8006
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469322"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ REVEAL

La transición reveal revela la nueva imagen a lo largo de una línea recta que se origina en un lado del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Distancia | <strong>fEffectPara0</strong> | Cantidad de la nueva imagen revelada, en píxeles. Este valor es relativo al lado de origen del marco. | 
| Dirección | <strong>fEffectPara1</strong> | Dirección de la revelación. Establezca en uno de los siguientes valores:<br /><ul><li>0: mostrar a la derecha; originar desde el lado izquierdo del marco.</li><li>1 - Mostrar a la izquierda; originar desde el lado derecho del marco.</li><li>2 - Mostrar hacia arriba; originar desde la parte inferior del marco.</li><li>3 - Mostrar hacia abajo; originar desde la parte superior del marco.</li></ul> | 
| Composición | <strong>fEffectPara2</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





