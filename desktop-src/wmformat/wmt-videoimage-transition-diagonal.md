---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl.h)
description: La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del marco.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea028777580f7414a834a0aa3e73e18db607eccd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471991"
---
# <a name="wmt_videoimage_transition_diagonal"></a>DIAGONAL DE TRANSICIÓN \_ DE IMAGEN DE VÍDEO \_ DE WMT \_

La transición diagonal revela la nueva imagen a lo largo de una línea diagonal que se origina en una esquina del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que se asignan.




| Parámetro | Miembro de estructura | Description | 
|-----------|------------------|-------------|
| Ancho | <strong>fEffectPara0</strong> | Ancho de la sección diagonal en píxeles. | 
| Alto | <strong>fEffectPara1</strong> | Alto de la sección diagonal en píxeles. | 
| Dirección | <strong>fEffectPara2</strong> | Determina la esquina desde la que se origina la transición. Establezca en una de las siguientes opciones:<br /><ul><li>0- Esquina superior derecha</li><li>1 - Parte superior izquierda</li><li>2 - Inferior derecha</li><li>3 - Inferior izquierda</li></ul> | 
| Composición | <strong>fEffectPara3</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





