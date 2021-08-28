---
description: 'MFT_MESSAGE_COMMAND_DRAIN: solicita una transformación Media Foundation datos (MFT) para vaciar todos los datos almacenados.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8faf20ca1169d87370a7dc1b5a128b11c9f17937a514f4aaea37631aee4d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012625"
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

Una vez que el cliente ha purgado el MFT, el cliente puede enviar más datos de entrada. El primer ejemplo después de la operación de purga debe tener el atributo discontinuity [**(atributo MFSampleExtension \_ Discontinuity).**](mfsampleextension-discontinuity-attribute.md)

> [!Note]  
> En versiones anteriores de esta documentación se indicaba que el parámetro de *evento ulParam* es miembro de la [**\_ enumeración MFT \_ DRAIN \_ TYPE.**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) No es correcto. *UlParam contiene* un identificador de secuencia.

 

### <a name="implementation"></a>Implementación

Un MFT asincrónico siempre debe devolver [METransformDrainComplete](metransformdraincomplete.md) después de que se haya purgado.

Un MFT sincrónico puede omitir este mensaje y devolver S \_ OK si se cumplen las condiciones siguientes:

-   MFT nunca almacena más de una muestra de entrada a la vez.
-   Cada ejemplo de entrada genera un único ejemplo de salida.

De lo contrario, un MFT sincrónico debe implementar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO DE \_ MENSAJE \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFT asincrónicos](asynchronous-mfts.md)
</dt> </dl>

 

 




