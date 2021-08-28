---
description: Especifica el perfil de audio y el nivel de una secuencia de codificación de audio avanzada (AAC).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89934c55ff07124c28952c621513ddd4fd8db504c6e9df7cc6094f8ba7b875ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104571"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a>Atributo MF \_ MT \_ AAC \_ AUDIO PROFILE \_ LEVEL \_ \_ INDICATION

Especifica el perfil de audio y el nivel de una secuencia de codificación de audio avanzada (AAC).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentarios

Este atributo contiene el valor del campo **audioProfileLevelIndication,** tal como se define en ISO/IEC 14496-3.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




