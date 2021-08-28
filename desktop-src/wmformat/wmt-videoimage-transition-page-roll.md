---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl.h)
description: La transición de lanzamiento de página transforma la imagen antigua con un efecto de volteo de página, lo que revela la nueva imagen debajo.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474981"
---
# <a name="wmt_videoimage_transition_page_roll"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ PAGE \_ ROLL

La transición de lanzamiento de página transforma la imagen antigua con un efecto de volteo de página, lo que revela la nueva imagen debajo.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Descripción | 
|-----------|------------------|-------------|
| Radio | <strong>fEffectPara0</strong> | Radio de la tirada en el efecto de lanzamiento de página. | 
| Distancia | <strong>fEffectPara1</strong> | Cantidad de la nueva imagen revelada por el efecto de lanzamiento de página, en píxeles. | 
| Dirección | <strong>fEffectPara2</strong> | Esquina o lado del fotograma de vídeo, desde el que se origina el lanzamiento de página. Establezca en uno de los siguientes valores:<br /><ul><li>0 : lado izquierdo</li><li>1 - Lado derecho</li><li>2 - Inferior</li><li>3 - Superior</li><li>4 - Esquina inferior izquierda</li><li>5 - Esquina inferior derecha</li><li>6 - Esquina superior izquierda</li><li>7 - Esquina superior derecha</li></ul> | 
| Composición | <strong>fEffectPara3</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





