---
description: Notifica a una Media Foundation transformación de datos (MFT) que el primer ejemplo está a punto de procesarse.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973034"
---
# <a name="mft_message_notify_start_of_stream"></a>MENSAJE MFT \_ \_ NOTIFY START OF \_ \_ \_ STREAM

Notifica a una Media Foundation transformación de datos (MFT) que el primer ejemplo está a punto de procesarse.

## <a name="message-parameter"></a>Parámetro message

Ninguno.

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

En el caso de las MTA sincrónicas, es opcional enviar este mensaje.

En el caso de las MTA asincrónicas, el cliente debe enviar este mensaje.

### <a name="implementation"></a>Implementación

No se requiere un MFT sincrónico para responder al mensaje.

Un MFT asincrónico debe implementar este mensaje, como se describe en [MTA asincrónicos.](asynchronous-mfts.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO DE \_ MENSAJE \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




