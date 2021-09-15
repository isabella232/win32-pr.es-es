---
description: Especifica el rol de dispositivo para la secuencia de audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468713"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>Atributo MF \_ MEDIA ENGINE AUDIO ENDPOINT \_ \_ \_ \_ ROLE

Especifica el rol de dispositivo para la secuencia de audio.

## <a name="data-type"></a>Tipo de datos

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la [**enumeración ERole.**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)

Este atributo se usa con el [**método IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia. El atributo es opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
