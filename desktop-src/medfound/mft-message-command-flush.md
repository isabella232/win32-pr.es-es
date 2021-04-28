---
description: 'MFT_MESSAGE_COMMAND_FLUSH: solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092743"
---
# <a name="mft_message_command_flush"></a>COMANDO DE MENSAJE DE MFT \_ \_ \_ FLUSH

Solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.

## <a name="message-parameter"></a>Parámetro message

Ninguno.

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Después de enviar este mensaje, MFT puede aceptar nuevos ejemplos de entrada. Los tipos de medios actuales no se invalidan.

### <a name="implementation"></a>Implementación

Todas las MTA deben implementar este mensaje. Cuando recibe este mensaje, el MFT debe descartar las muestras de medios que esté manteniendo.

[MFT asincrónico:](asynchronous-mfts.md)MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) del cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO DE \_ MENSAJE \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




