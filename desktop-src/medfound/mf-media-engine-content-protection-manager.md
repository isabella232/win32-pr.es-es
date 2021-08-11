---
description: Habilita el motor de multimedia para reproducir contenido protegido.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER atributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe80e619f3b256f6aa587f32d9ee5b6f43cd2978a5dfb043c62536ff5315bacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244694"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a>Atributo CONTENT \_ \_ PROTECTION \_ MANAGER de \_ \_ MF MEDIA ENGINE

Habilita el motor de multimedia para reproducir contenido protegido.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Comentarios

El valor de este atributo es un puntero a la [**interfaz IMFContentProtectionManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) El autor de la llamada debe implementar la interfaz .

Este atributo puede ser uno de los atributos pasados [**a IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance). Es necesario si se va a reproducir contenido protegido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




