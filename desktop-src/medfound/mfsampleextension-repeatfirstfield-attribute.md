---
description: Especifica si se debe repetir el primer campo en un marco entrelazado. Este atributo se aplica a los ejemplos multimedia.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0668e37e6a6958615c83f98c4b6b87eb170b115cf0549f3944a43b21c5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872425"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>Atributo MFSampleExtension \_ RepeatFirstField

Especifica si se debe repetir el primer campo en un marco entrelazado. Este atributo se aplica a los ejemplos multimedia.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**SAMPLESample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentarios

Si el valor es **FALSE o** el atributo no está establecido, no se repite el primer campo. Si el valor es **TRUE**, se repite el primer campo. El valor **TRUE** solo es válido cuando se cumplen las condiciones siguientes:

-   El tipo de medio es mixto entrelazado y progresiva. (El [**atributo del atributo MF MT \_ \_ INTERLACE \_ MODE**](mf-mt-interlace-mode-attribute.md) en el tipo de medio **es MFVideoInterlace \_ MixedInterlaceOrProgressive).**
-   El marco es progresiva y el atributo [**MFSampleExtension \_ entrelazado**](mfsampleextension-interlaced-attribute.md) del ejemplo es **TRUE.**
-   El [**atributo MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) se establece en el ejemplo. El valor puede ser **TRUE** o **FALSE.** El orden de los campos viene determinado por este atributo.

Este atributo se usa para la extracción 3:2. En la tabla siguiente se muestra el orden en el que se muestran los campos.



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | Orden de campo         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Inferior, superior, inferior |
| **TRUE**                            | **FALSE**                           | Superior, inferior, superior |
| **FALSE**                           | **TRUE**                            | Inferior, superior        |
| **FALSE**                           | **FALSE**                           | Superior, inferior        |



 

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




