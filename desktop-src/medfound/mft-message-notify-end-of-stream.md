---
description: Notifica a una Media Foundation transformación de datos (MFT) que ha finalizado un flujo de entrada.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951337fb91a26f1498b2aa82d42754fb2954ab649b4a021d37d42047be331ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872165"
---
# <a name="mft_message_notify_end_of_stream"></a>MFT \_ MESSAGE \_ NOTIFY \_ END \_ OF \_ STREAM

Notifica a una Media Foundation transformación de datos (MFT) que ha finalizado un flujo de entrada.

## <a name="message-parameter"></a>Parámetro message

El *parámetro ulParam* contiene el identificador del flujo de entrada, especificado como un **valor DWORD.** En aplicaciones de 64 bits, coloque este valor en los 32 bits inferiores de **ULONG \_ PTR**.

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

No es necesario que el cliente envíe este mensaje.

Una vez que finaliza una secuencia, el cliente puede llamar de nuevo [**a ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para enviar nuevos datos para esa secuencia. Si es así, el cliente debe establecer el atributo de discontinuidad [**(atributo MFSampleExtension \_ Discontinuity)**](mfsampleextension-discontinuity-attribute.md) en el primer ejemplo de entrada después de que finalice la secuencia. (El cliente siempre debe establecer este atributo en el primer ejemplo nuevo después de que finalice una secuencia, independientemente de si el cliente envió el mensaje **MFT \_ MESSAGE NOTIFY END OF \_ \_ \_ \_ STREAM.** Para obtener más información sobre cómo controlar las discontinuidades, vea [Basic MFT Processing Model](basic-mft-processing-model.md).)

Después de enviar este mensaje para cada flujo de entrada, el cliente normalmente envía un comando DRAIN del comando **MFT \_ MESSAGE \_ y, \_** a continuación, recopila el resultado restante. Sin embargo, el cliente no es necesario para purgar el MFT. Si el cliente no purga el MFT, el MFT normalmente descartará los datos no procesados en la siguiente llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), cuando detecte la discontinuidad de la secuencia. Como alternativa, el cliente podría vaciar el MFT antes de llamar a **ProcessInput**.

Este mensaje no quita el flujo de entrada ni restablece el tipo de medio.

### <a name="implementation"></a>Implementación

No se requiere un MFT para responder a este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO DE MENSAJE \_ \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




