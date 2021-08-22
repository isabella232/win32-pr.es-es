---
description: Especifica un flujo de entrada en una Media Foundation transformación (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: MF_EVENT_MFT_INPUT_STREAM_ID atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d211eb30280e6b7390df8509795d49567c7f8a8c9016b2825786858fe888b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973814"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a>Atributo MF \_ EVENT \_ MFT \_ INPUT STREAM \_ \_ ID

Especifica un flujo de entrada en una Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es un identificador de flujo de entrada.

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>Comentarios

Este atributo se usa con los siguientes eventos:

-   [METransformDrainComplete](metransformdraincomplete.md)
-   [METransformNeedInput](metransformneedinput.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> </dl>

 

 




