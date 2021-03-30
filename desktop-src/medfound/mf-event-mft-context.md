---
description: Contiene un valor definido por el autor de la llamada para un evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082348"
---
# <a name="mf_event_mft_context-attribute"></a>\_Atributo de \_ contexto de MFT de evento MF \_

Contiene un valor definido por el autor de la llamada para un evento [METransformMarker](metransformmarker.md) .

## <a name="data-type"></a>Tipo de datos

**ULong \_ PTR** almacenado como **UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Observaciones

Este atributo se usa con el evento [METransformMarker](metransformmarker.md) . El valor del atributo se toma del parámetro *ulParam* del método [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrónico](asynchronous-mfts.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> </dl>

 

 




