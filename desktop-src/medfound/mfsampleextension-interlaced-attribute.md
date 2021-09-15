---
description: Indica si un fotograma de vídeo está entrelazado o progresiva.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580289"
---
# <a name="mfsampleextension_interlaced-attribute"></a>Atributo MFSampleExtension \_ entrelazado

Indica si un fotograma de vídeo está entrelazado o progresiva. Si **es TRUE,** el marco está entrelazado. Si **es FALSE,** el marco es progresiva. Si no se establece, el tipo de medio describe el entrelazado. Este atributo se aplica a los ejemplos multimedia.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

Para el contenido de vídeo que contiene fotogramas mixtos progresivas e entrelazados, establezca el tipo de medio en entrelazado y use este atributo en cada fotograma para indicar si el marco es progresiva o entrelazada.

Para el contenido de vídeo que está completamente entrelazado, establezca el tipo de medio en entrelazado y omita este atributo, o bien esta establezca en **TRUE** en cada ejemplo.

Para el contenido de vídeo totalmente progresiva, establezca el tipo de medio en progresiva y omita este atributo, o bien esta establezca en **FALSE** en cada ejemplo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




