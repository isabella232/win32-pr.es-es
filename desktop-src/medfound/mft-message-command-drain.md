---
description: Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666871"
---
# <a name="mft_message_command_drain"></a>\_consumo de \_ comandos de mensajes de MFT \_

Solicita una transformación de Media Foundation (MFT) para vaciar todos los datos almacenados.

## <a name="message-parameter"></a>Parámetro de mensaje

Ninguno.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Después de enviar este mensaje, el flujo de entrada especificado no acepta la entrada hasta que el MFT procesa todos los datos de llamadas anteriores a [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

El proceso de purga varía ligeramente entre MFTs sincrónicos y MFTs asincrónicos:

**MFTs sincrónicos**

1.  Una vez que el cliente envía este mensaje, llama a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) en un bucle, hasta que **ProcessOutput** devuelve el código de error de la **\_ transformación MF E \_ \_ necesita \_ más \_ entrada**.
2.  Siempre que la MFT siga teniendo datos para procesar, se producirá un error en otras llamadas a [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . La MFT continúa generando resultados hasta que utiliza todos los datos almacenados. La MFT descarta todos los datos que no se pueden procesar en un ejemplo de salida completo. (Por ejemplo, debe quitar un fotograma de vídeo parcial).

**MFTs asincrónico**

1.  La MFT sigue enviando eventos [METransformHaveOutput](metransformhaveoutput.md) hasta que no tiene más datos para procesar. No envía eventos [METransformNeedInput](metransformneedinput.md) durante este tiempo.
2.  Después de que el MFT envíe el último evento [METransformHaveOutput](metransformhaveoutput.md) , envía un evento [METransformDrainComplete](metransformdraincomplete.md) .
3.  Una vez completada la purga, el MFT no envía otro evento [METransformNeedInput](metransformneedinput.md) hasta que reciba un [**mensaje de MFT para \_ \_ notificar el \_ Inicio \_ del \_**](mft-message-notify-start-of-stream.md) mensaje de secuencia desde el cliente.

Una vez que el cliente ha purgado la MFT, el cliente puede enviar más datos de entrada. El primer ejemplo después de la operación de purga debe tener el atributo discontinuidad (atributo discontinuidad [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) ).

> [!Note]  
> En las versiones anteriores de esta documentación se indicó que el parámetro de evento *ulParam* es un miembro de la enumeración de [**\_ \_ \_ tipo Drain de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) . No es correcto. *UlParam* contiene un identificador de flujo.

 

### <a name="implementation"></a>Implementación

Una MFT asincrónica siempre debe devolver [METransformDrainComplete](metransformdraincomplete.md) una vez que se ha purgado.

Los MFT sincrónicos pueden pasar por alto este mensaje y devolver S \_ correcto si se cumplen las condiciones siguientes:

-   La MFT nunca almacena más de una muestra de entrada a la vez.
-   Cada ejemplo de entrada genera un único ejemplo de salida.

De lo contrario, un MFT sincrónico debe implementar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de mensaje de MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFTs asincrónico](asynchronous-mfts.md)
</dt> </dl>

 

 




