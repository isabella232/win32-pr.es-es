---
description: Un cliente de XAudio2 tiene control total sobre la asignación desde los canales de una voz a los canales de cada una de sus voces de destino.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: Asignación de canales predeterminada de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d77371223ccef02d6f0831a7aea182326f8477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498148"
---
# <a name="xaudio2-default-channel-mapping"></a>Asignación de canales predeterminada de XAudio2

Un cliente de XAudio2 tiene control total sobre la asignación desde los canales de una voz a los canales de cada uno de sus voicesIt de destino controla la asignación mediante el uso del método [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . Sin embargo, en algunas circunstancias, XAudio2 simplifica esta tarea mediante la configuración automática de una matriz de envío predeterminada. Para ello, se usa la máscara de canal, si existe, asociada a los canales de audio de una voz. Una máscara de canal es una combinación de las máscaras de bits de un altavoz \_ , tal y como se define en X3DAudio. h y en otra parte. XAudio2 requiere que las máscaras de canal sean 0 o que tengan el mismo número de bits establecido que el número de canales.

En la tabla siguiente se muestran los requisitos de máscara de canal y los valores predeterminados para los formatos admitidos por XAudio2. 

| Formato | Requisito de máscara de canal             | Máscara predeterminada                        | Miembro de estructura correspondiente                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | El archivo puede contener una máscara de canal    | La máscara del canal es 0 o no está presente        | WAVEFORMATEXTENSIBLE. dwChannelMask o None (WAVEFORMATEX) |
| ADPCM  | El archivo no contiene una máscara de canal | Siempre se usa la máscara de canal predeterminada | Ninguno (ADPCMWAVEFORMAT)                                    |



 

En el caso de las voces de submezcla y de la maestra, y para las voces de origen sin una máscara de canal o una máscara de canal de 0, XAudio2 supone posiciones de oradores predeterminadas según la siguiente tabla. 

| Canales  | Posiciones de canal IMPLÍCITAS                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Siempre se asigna a FrontLeft y FrontRight a escala completa en ambos altavoces (caso especial para sonidos mono)                 |
| 2         | FrontLeft, FrontRight (configuración básica de estéreo)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (configuración 2,1)                                                               |
| 4         | FrontLeft, FrontRight, la izquierda, la derecha (quadraphonic)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (configuración 5,0)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (configuración 5,1) (vea los comentarios siguientes) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, recenter (configuración 6,1)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, Left, Right, SideLeft, SideRight (configuración 7,1)        |
| 9 o más | Sin posiciones IMPLÍCITAS (asignación uno a uno)                                                                            |



 

Si un par de voz determinado en el gráfico de audio no tiene ninguna posición de orador asociada con su voz de origen o de destino (una voz tiene más de ocho canales), ninguna voz se puede reproducir hasta que la voz de origen tenga una matriz de envío establecida explícitamente mediante el método [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) . Se producirá un error al llamar al método [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para cualquier voz hasta que lo haga.

Si la voz de origen y la de destino tienen un número diferente de posiciones de orador y [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) no se ha llamado a la voz de origen, XAudio2 envía cada canal de origen al altavoz (o altavoces) de destino más cercano disponible, proporcionalmente a lo cerca que se encuentre en el altavoz previsto. Hay dos casos especiales en los que el comportamiento predeterminado es diferente.

1.  Si el audio de origen es mono y se coloca en \_ el \_ centro frontal o no tiene ninguna posición definida, siempre se envía al altavoz de \_ \_ la izquierda y a \_ la parte delantera \_ derecha si existen en el audio de salida. Si no existen, recurre al caso normal.
2.  Si el origen y el destino son de 6 canales y se colocan en cualquiera de las configuraciones de altavoces estándar 5,1 (izquierda + derecha + centro + sub + backl + Back-in o Left + Right + Center + sub + Sidel + SideR), los canales se asignan de uno a uno. En otras palabras, SideLeft/Right y Left/Right se tratan de forma equivalente. Esto se debe a que hay una confusión histórica en torno a estas configuraciones. Por lo tanto, el intento asumido siempre es asignar uno a uno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Voces](voices.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
