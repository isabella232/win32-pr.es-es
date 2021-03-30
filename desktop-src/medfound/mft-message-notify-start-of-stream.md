---
description: Notifica a una transformación de Media Foundation (MFT) que la primera muestra está a punto de procesarse.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082299"
---
# <a name="mft_message_notify_start_of_stream"></a>el \_ mensaje \_ de MFT notifica el \_ Inicio \_ de la \_ secuencia

Notifica a una transformación de Media Foundation (MFT) que la primera muestra está a punto de procesarse.

## <a name="message-parameter"></a>Parámetro de mensaje

Ninguno.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

En el caso de MFTs sincrónicos, es opcional enviar este mensaje.

En el caso de MFTs asincrónico, el cliente debe enviar este mensaje.

### <a name="implementation"></a>Implementación

No es necesario un MFT sincrónico para responder al mensaje.

Un MFT asincrónico debe implementar este mensaje, tal y como se describe en [MFTs asincrónico](asynchronous-mfts.md).

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

 

 




