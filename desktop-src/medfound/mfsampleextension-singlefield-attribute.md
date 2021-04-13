---
description: Especifica si un ejemplo de vídeo contiene un solo campo o dos campos intercalados. Este atributo se aplica a los ejemplos de medios.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: MFSampleExtension_SingleField atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543926"
---
# <a name="mfsampleextension_singlefield-attribute"></a>\_Atributo SingleField de MFSampleExtension

Especifica si un ejemplo de vídeo contiene un solo campo o dos campos intercalados. Este atributo se aplica a los ejemplos de medios.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Si el valor es **true**, el ejemplo contiene un campo. Si el valor es **false** o el atributo no está establecido, el ejemplo contiene un marco completo. (Dos campos, si están entrelazados, o un marco progresivo).

Si el tipo de medio es fotogramas progresivos o campos intercalados, este atributo debe ser **falso** o dejar sin establecer.

Si el tipo de medio es un campo único, este atributo debe ser **true**. Establezca el atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) en el ejemplo para indicar si es el campo superior o el campo inferior.

Actualmente, el representador de vídeo mejorado (EVR) no admite contenido que cambie entre fotogramas entrelazados y campos individuales.

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

 

 




