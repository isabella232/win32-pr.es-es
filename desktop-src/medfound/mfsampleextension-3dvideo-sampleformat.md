---
description: Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6529a08c14846fb1d06cd9b3ed0827a43d1b1ba75310c0379efddadebecdaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722875"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>Atributo MFSampleExtension \_ 3DVideo \_ SampleFormat

Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es miembro de la [**enumeración MFVideo3DSampleFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat)

Un componente que genera fotogramas de vídeo 3D debe establecer este atributo en **TRUE** en cada ejemplo multimedia que contenga un fotograma 3D. El atributo se omite si el atributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) es **FALSE** o no está establecido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




