---
description: 'MFT_MESSAGE_COMMAND_DRAIN: solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092753"
---
# <a name="mft_message_command_drain"></a>PURGA DE COMANDOS \_ DE \_ MENSAJES DE \_ MFT

Solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.

## <a name="message-parameter"></a>Parámetro message

Ninguno.

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Después de enviar este mensaje, el flujo de entrada especificado no acepta la entrada hasta que MFT procesa todos los datos de las llamadas anteriores a [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

El proceso de purga varía ligeramente entre los MTA sincrónicos y los MTA asincrónicos:

**MFT sincrónicos**

1.  Una vez que el cliente envía este mensaje, llama a [**MFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en un bucle, hasta que **ProcessOutput** devuelve el código de error **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT**.
2.  Siempre y cuando MFT todavía tenga datos que procesar, se producirá un error en las llamadas a [**ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) MFT continúa generando resultados hasta que usa todos los datos almacenados. El MFT descarta los datos que no se pueden procesar en un ejemplo de salida completo. (Por ejemplo, debería quitar un fotograma de vídeo parcial).

**MFT asincrónicos**

1.  El MFT continúa con el envío [de eventos METransformTransformTransformOutput](metransformhaveoutput.md) hasta que no tiene más datos para procesar. No envía eventos [METransformNeedInput](metransformneedinput.md) durante este tiempo.
2.  Una vez que MFT envía el último [evento METransformTransformTransformOutput,](metransformhaveoutput.md) envía un [evento METransformDrainComplete.](metransformdraincomplete.md)
3.  Una vez completada la purga, MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que recibe un mensaje [**MFT \_ MESSAGE NOTIFY START \_ OF \_ \_ \_ STREAM**](mft-message-notify-start-of-stream.md) del cliente.

Una vez que el cliente ha purgado el MFT, el cliente puede enviar más datos de entrada. El primer ejemplo después de la operación de purga debe tener el atributo de discontinuidad [**(atributo MFSampleExtension \_ Discontinuity).**](mfsampleextension-discontinuity-attribute.md)

> [!Note]  
> En versiones anteriores de esta documentación se indicaba que el parámetro de evento *ulParam* es miembro de la [**\_ enumeración \_ MFT DRAIN \_ TYPE.**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) No es correcto. *UlParam contiene* un identificador de secuencia.

 

### <a name="implementation"></a>Implementación

Un MFT asincrónico siempre debe devolver [METransformDrainComplete después](metransformdraincomplete.md) de que se haya purgado.

Un MFT sincrónico puede omitir este mensaje y devolver S \_ OK si se cumplen las condiciones siguientes:

-   MFT nunca almacena más de un ejemplo de entrada a la vez.
-   Cada ejemplo de entrada genera un único ejemplo de salida.

De lo contrario, un MFT sincrónico debe implementar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO DE MENSAJE \_ \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFT asincrónicas](asynchronous-mfts.md)
</dt> </dl>

 

 




