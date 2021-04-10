---
description: Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155973"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>MFSampleExtension \_ 3DVideo \_ SampleFormat

Especifica cómo se almacena un fotograma de vídeo 3D en un ejemplo multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la enumeración [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .

Un componente que genera fotogramas de vídeo 3D debe establecer este atributo en **true** en cada ejemplo multimedia que contenga un fotograma 3D. El atributo se omite si el atributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) es **false** o no se establece.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




