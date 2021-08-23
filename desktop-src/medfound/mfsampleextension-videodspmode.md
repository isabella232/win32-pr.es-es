---
description: Indica si se aplicó la estabilización de vídeo a un fotograma de vídeo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode atributo (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95776fd7b8e130b9538e98843ca72d69980978b6f954747fadca939b8d3c5922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554935"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>Atributo MFSampleExtension \_ VideoDSPMode

Indica si se aplicó la estabilización de vídeo a un fotograma de vídeo.

## <a name="data-type"></a>Tipo de datos

**MFVideoDSPMode almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentarios

El [**Video Stabilization MFT**](video-stabilization-mft.md) establece este atributo en los ejemplos de salida que genera. El valor del atributo es un valor de [**enumeración MFVideoDSPMode.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) Si el valor es **MFVideoDSPMode \_ Stabilization**, significa que el MFT aplicó la estabilización de la imagen al marco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[**Video Stabilization MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




