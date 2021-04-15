---
description: Notifica a una transformación de Media Foundation (MFT) que un flujo de entrada ha finalizado.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715790"
---
# <a name="mft_message_notify_end_of_stream"></a>\_ \_ \_ final \_ de notificación de mensaje de \_ MFT

Notifica a una transformación de Media Foundation (MFT) que un flujo de entrada ha finalizado.

## <a name="message-parameter"></a>Parámetro de mensaje

El parámetro *ulParam* contiene el identificador del flujo de entrada, especificado como un valor **DWORD** . En las aplicaciones de 64 bits, coloque este valor en los 32 bits inferiores de **ULong \_ ptr**.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

No es necesario que el cliente envíe este mensaje.

Una vez finalizada una secuencia, el cliente puede volver a llamar a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para enviar datos nuevos para esa secuencia. En ese caso, el cliente debe establecer el atributo discontinuidad (atributo discontinuidad [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) ) en el primer ejemplo de entrada después de que finalice la secuencia. (El cliente siempre debe establecer este atributo en el primer ejemplo nuevo una vez finalizada una secuencia, independientemente de si el cliente envió el **\_ mensaje \_ de MFT notifica el \_ final del mensaje de la \_ \_ secuencia** . Para obtener más información sobre cómo controlar las discontinuidades, vea [modelo de procesamiento de MFT básico](basic-mft-processing-model.md)).

Después de enviar este mensaje para cada flujo de entrada, el cliente normalmente envía un comando de purga de comando de mensaje de MFT y, a continuación, recopila el resultado restante. **\_ \_ \_** Sin embargo, no es necesario que el cliente vacíe la MFT. Si el cliente no purga la MFT, normalmente descartará todos los datos sin procesar en la siguiente llamada a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), cuando detecte la discontinuidad de la secuencia. Como alternativa, el cliente puede vaciar el MFT antes de llamar a **ProcessInput**.

Este mensaje no quita el flujo de entrada ni restablece el tipo de medio.

### <a name="implementation"></a>Implementación

No se requiere una MFT para responder a este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de mensaje de MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




