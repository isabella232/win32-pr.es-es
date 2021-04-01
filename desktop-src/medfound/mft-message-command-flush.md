---
description: Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811612"
---
# <a name="mft_message_command_flush"></a>\_ \_ vaciado de comandos de mensajes de MFT \_

Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.

## <a name="message-parameter"></a>Parámetro de mensaje

Ninguno.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Después de enviar este mensaje, el MFT puede aceptar nuevos ejemplos de entrada. Los tipos de medios actuales no se invalidan.

### <a name="implementation"></a>Implementación

Todos los MFTs deben implementar este mensaje. Cuando recibe este mensaje, la MFT debe descartar los ejemplos de medios que contiene.

[Asincrónico MFTs](asynchronous-mfts.md): el MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje de [**MFT \_ para \_ notificar el \_ Inicio \_ del \_**](mft-message-notify-start-of-stream.md) mensaje de secuencia desde el cliente.

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

 

 




