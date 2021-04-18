---
description: Define la abertura de la pantalla, que es la región de un fotograma de vídeo que contiene datos de imagen válidos.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715249"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>\_Atributo de \_ \_ abertura de pantalla mínima MF MT \_

Define la abertura de la pantalla, que es la región de un fotograma de vídeo que contiene datos de imagen válidos.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

El valor del atributo es una estructura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

La abertura de pantalla mínima es la región que contiene la parte válida de la señal. Los píxeles que están fuera de la abertura contienen datos no válidos y no se deben mostrar.

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

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ apertura geométrica de MF MT \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**\_apertura de \_ \_ análisis panorámico MF MT \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




