---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: La transición de fundido a color se resuelve de la imagen en un marco de color sólido.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR formato de Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699584"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>\_ \_ transición de imagen de transmisión de imágenes WMT \_ \_ a \_ color

La transición de fundido a color se resuelve de la imagen en un marco de color sólido.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros que se usan en esta transición y se enumeran los miembros de la estructura de [**\_ \_ SAMPLE2 de imágenes WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) en la que se asignan.



| Parámetro         | Miembro de estructura | Descripción                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rojo               | **fEffectPara0** | Valor rojo del color de fondo. Establezca en un número comprendido entre 0 y 255.                                                                                                                                                     |
| Verde             | **fEffectPara1** | Valor verde del color de fondo. Establezca en un número comprendido entre 0 y 255.                                                                                                                                                   |
| Azul              | **fEffectPara2** | Valor azul del color de fondo. Establezca en un número comprendido entre 0 y 255.                                                                                                                                                    |
| Peso de fondo | **fEffectPara3** | Peso del color de fondo. Este parámetro expresa el porcentaje del color de fondo de la combinación como un decimal. Por ejemplo, para mezclar el color de fondo en un 30%, lo que permite que la imagen del 70% de la combinación se establezca en 0,30. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Transiciones de imagen de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





