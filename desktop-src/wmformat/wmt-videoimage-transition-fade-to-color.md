---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl.h)
description: La transición de atenuación a color se disuelve de la imagen a un marco de color sólido.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR windows Media Format
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
ms.openlocfilehash: 315a0d190a65c8f756eabaff6b86dd2efb6d4dbe97e5b5de8e7a3dfe782c880a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109945"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>TRANSICIÓN DE \_ WMT VIDEOIMAGE \_ A \_ \_ \_ COLOR

La transición de atenuación a color se disuelve de la imagen a un marco de color sólido.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros usados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.



| Parámetro         | Miembro de estructura | Descripción                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rojo               | **fEffectPara0** | Valor rojo del color de fondo. Establezca en un número entre 0 y 255.                                                                                                                                                     |
| Verde             | **fEffectPara1** | Valor verde del color de fondo. Establezca en un número entre 0 y 255.                                                                                                                                                   |
| Azul              | **fEffectPara2** | Valor azul del color de fondo. Establezca en un número entre 0 y 255.                                                                                                                                                    |
| Peso de fondo | **fEffectPara3** | Peso del color de fondo. Este parámetro expresa el porcentaje del color de fondo de la combinación como decimal. Por ejemplo, para combinar el color de fondo al 30 %, haciendo que la imagen se establezca en 0,30 %. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





