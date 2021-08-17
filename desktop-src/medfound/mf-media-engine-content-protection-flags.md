---
description: Especifica si el motor multimedia reproducirá contenido protegido.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1cb6b9c9a49c690af84678435ac2bb4fdab76a2fb13c95fecd9ddc33771d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956445"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a>Atributo \_ MF MEDIA ENGINE CONTENT PROTECTION \_ \_ \_ \_ FLAGS

Especifica si el motor multimedia reproducirá contenido protegido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un **OR** bit a bit de marcas de la enumeración [**MF MEDIA ENGINE PROTECTION \_ \_ \_ \_ FLAGS.**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) Para habilitar la reproducción de contenido protegido, establezca la marca MF MEDIA ENGINE ENABLE PROTECTED CONTENT ( **HABILITAR \_ \_ \_ \_ \_ CONTENIDO** PROTEGIDO).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor multimedia](media-engine-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




