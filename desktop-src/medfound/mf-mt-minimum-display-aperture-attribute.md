---
description: Define la apertura de la pantalla, que es la región de un fotograma de vídeo que contiene datos de imagen válidos.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ff6dd226492c848bd2347ccc2bac17c2dd8824467e661e83be06d590f65c0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012945"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>Atributo MF \_ MT \_ MINIMUM DISPLAY \_ \_ APERTURE

Define la apertura de la pantalla, que es la región de un fotograma de vídeo que contiene datos de imagen válidos.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

El valor del atributo es [**una estructura MFVideoArea.**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea)

La apertura de pantalla mínima es la región que contiene la parte válida de la señal. Los píxeles situados fuera de la apertura contienen datos no válidos y no deben mostrarse.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de medios de vídeo](video-media-types.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**APERTURA \_ GEOMÉTRICA DE MF MT \_ \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




