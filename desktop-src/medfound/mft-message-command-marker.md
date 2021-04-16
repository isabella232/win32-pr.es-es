---
description: Marca un punto en la secuencia. Este mensaje se aplica solo a MFTs asincrónicos.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715791"
---
# <a name="mft_message_command_marker"></a>\_marcador de \_ comando de mensaje de MFT \_

Marca un punto en la secuencia. Este mensaje se aplica solo a [MFTs asincrónicos](asynchronous-mfts.md).

## <a name="message-parameter"></a>Parámetro de mensaje

Un valor arbitrario. La MFT devuelve el valor al cliente en el evento [METransformMarker](metransformmarker.md) .

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

La MFT responde a este mensaje a continuación:

1.  La MFT genera tantos ejemplos de salida como los datos de entrada existentes, y envía un evento [METransformHaveOutput](metransformhaveoutput.md) para cada ejemplo de salida.
2.  Una vez generada la salida, el MFT envía un evento [METransformMarker](metransformmarker.md) . Este evento se debe enviar después de todos los eventos [METransformHaveOutput](metransformhaveoutput.md) .

No es necesario que el cliente envíe este mensaje y debe enviar este mensaje solo a MFTs asincrónicos. Un MFT sincrónico no enviará un evento [METransformMarker](metransformmarker.md) en respuesta a este mensaje.

### <a name="implementation"></a>Implementación

Los MFTs asincrónicos deben responder a este mensaje tal y como se describe. Los MFTs sincrónicos deben omitir este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_tipo de mensaje de MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




