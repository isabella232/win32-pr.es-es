---
description: Especifica el rol de dispositivo para la secuencia de audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a15a973aef342e3d37cde3e6d9f3dd7d61c553fecaa943215dbcc77a319950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104781"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>Atributo MF \_ MEDIA ENGINE AUDIO ENDPOINT \_ \_ \_ \_ ROLE

Especifica el rol de dispositivo para la secuencia de audio.

## <a name="data-type"></a>Tipo de datos

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** almacenado como **UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un miembro de la [**enumeración ERole.**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia. El atributo es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
