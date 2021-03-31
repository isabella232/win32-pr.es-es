---
description: Especifica si se va a repetir el primer campo en un marco entrelazado. Este atributo se aplica a los ejemplos de medios.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155365"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>\_Atributo RepeatFirstField de MFSampleExtension

Especifica si se va a repetir el primer campo en un marco entrelazado. Este atributo se aplica a los ejemplos de medios.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Si el valor es **false** o el atributo no está establecido, el primer campo no se repite. Si el valor es **true**, el primer campo se repite. El valor **true** solo es válido cuando se cumplen las condiciones siguientes:

-   El tipo de medio es entrelazado y progresivo. (El atributo de atributo de [**\_ \_ \_ modo entrelazado MF MT**](mf-mt-interlace-mode-attribute.md) en el tipo de medio es **MFVideoInterlace \_ MixedInterlaceOrProgressive**).
-   El marco es progresivo y el atributo [**\_ entrelazado MFSampleExtension**](mfsampleextension-interlaced-attribute.md) del ejemplo es **true**.
-   El atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) se establece en el ejemplo. El valor puede ser **true** o **false**. Este atributo determina el orden de los campos.

Este atributo se utiliza para la telecine 3:2. En la tabla siguiente se muestra el orden en que se muestran los campos.



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | Orden de los campos         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Inferior, superior, inferior |
| **TRUE**                            | **FALSE**                           | Superior, inferior, superior |
| **FALSE**                           | **TRUE**                            | Inferior, superior        |
| **FALSE**                           | **FALSE**                           | Superior, inferior        |



 

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




