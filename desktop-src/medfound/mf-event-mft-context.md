---
description: Contiene un valor definido por el autor de la llamada para un evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: MF_EVENT_MFT_CONTEXT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9518853030ec52a687f02ac0288c3fd3ffcf55b676be56c7036b349e1dec9aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104851"
---
# <a name="mf_event_mft_context-attribute"></a>Atributo MF \_ EVENT \_ MFT \_ CONTEXT

Contiene un valor definido por el autor de la llamada para un [evento METransformMarker.](metransformmarker.md)

## <a name="data-type"></a>Tipo de datos

**ULONG \_ PTR** almacenado como **UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Comentarios

Este atributo se usa con el [evento METransformMarker.](metransformmarker.md) El valor del atributo se toma del parámetro *ulParam* del método [**IMFTransform::P rocessMessage.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicos](asynchronous-mfts.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> </dl>

 

 




