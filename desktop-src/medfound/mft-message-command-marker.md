---
description: Marca un punto en la secuencia. Este mensaje solo se aplica a las MTA asincrónicas.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc55a96ae9680b37d83ec776c66848ed04f4a30b62d1d0378035c88823d2c19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872175"
---
# <a name="mft_message_command_marker"></a>MARCADOR DE COMANDO \_ DE MENSAJE \_ \_ MFT

Marca un punto en la secuencia. Este mensaje solo se aplica a [las MTA asincrónicas.](asynchronous-mfts.md)

## <a name="message-parameter"></a>Parámetro message

Valor arbitrario. MFT devuelve el valor al cliente en el [evento METransformMarker.](metransformmarker.md)

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

El MFT responde a este mensaje como sigue:

1.  El MFT genera tantos ejemplos de salida como sea posible a partir de los datos de entrada existentes, enviando un [evento METransformTransformTransformOutput](metransformhaveoutput.md) para cada ejemplo de salida.
2.  Una vez generada toda la salida, MFT envía un [evento METransformMarker.](metransformmarker.md) Este evento debe enviarse después de todos los [eventos METransformTransformTransformOutput.](metransformhaveoutput.md)

El cliente no es necesario para enviar este mensaje y debe enviar este mensaje solo a las MTA asincrónicas. Un MFT sincrónico no enviará un [evento METransformMarker](metransformmarker.md) en respuesta a este mensaje.

### <a name="implementation"></a>Implementación

Las MTA asincrónicas deben responder a este mensaje como se describe. Las MTA sincrónicas deben omitir este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TIPO DE MENSAJE \_ \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




