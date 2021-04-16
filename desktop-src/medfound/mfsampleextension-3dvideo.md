---
description: Especifica si un ejemplo multimedia contiene un fotograma de vídeo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: MFSampleExtension_3DVideo atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705901"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>\_Atributo 3DVideo de MFSampleExtension

Especifica si un ejemplo multimedia contiene un fotograma de vídeo 3D.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, el ejemplo multimedia contiene un fotograma de vídeo que tiene dos o más vistas Stereoscopic. El valor predeterminado es **FALSE**.

Un componente que genera fotogramas de vídeo 3D debe establecer este atributo en **true** en cada ejemplo multimedia que contenga un fotograma 3D.

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

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




