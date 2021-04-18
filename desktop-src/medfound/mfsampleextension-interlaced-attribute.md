---
description: Indica si un fotograma de vídeo está entrelazado o progresivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720446"
---
# <a name="mfsampleextension_interlaced-attribute"></a>\_Atributo entrelazado MFSampleExtension

Indica si un fotograma de vídeo está entrelazado o progresivo. Si es **true**, el marco está entrelazado. Si es **false**, el marco es progresivo. Si no se establece, el tipo de medio describe el entrelazado. Este atributo se aplica a los ejemplos de medios.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Observaciones

En el caso de contenido de vídeo que contenga fotogramas progresivos e entrelazados mixtos, establezca el tipo de medio en entrelazado y use este atributo en cada fotograma para indicar si el marco es progresivo o entrelazado.

Para el contenido de vídeo que está totalmente entrelazado, establezca el tipo de medio en entrelazado y Omita este atributo, o establézcalo en **true** en cada ejemplo.

Para el contenido de vídeo que es totalmente progresivo, establezca el tipo de medio en progresivo y Omita este atributo, o establézcalo en **false** en cada ejemplo.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[Ejemplos de medios](media-samples.md)
</dt> <dt>

[Entrelazado de vídeo](video-interlacing.md)
</dt> </dl>

 

 




