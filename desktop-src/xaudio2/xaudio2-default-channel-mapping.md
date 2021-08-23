---
description: Un cliente XAudio2 tiene control total de la asignación desde los canales de una voz a los canales de cada una de sus voces de destino.
ms.assetid: 219d5b70-3f07-f973-f9ec-1cb3cf0be37e
title: Asignación de canales predeterminada de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42bb2f67709586532a19d86a916d3b7852652e76f9b6ce1ae115f1fc670e37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025953"
---
# <a name="xaudio2-default-channel-mapping"></a>Asignación de canales predeterminada de XAudio2

Un cliente XAudio2 tiene control total de la asignación desde los canales de una voz a los canales de cada una de sus voces de destinoIt controla la asignación mediante el uso del método [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) Sin embargo, en algunas circunstancias, XAudio2 simplifica esta tarea configurando automáticamente una matriz de envío predeterminada. Para ello, usa la máscara de canal, si existe, asociada a los canales de audio de una voz. Una máscara de canal es una combinación de máscaras de bits SPEAKER xxx, tal como se define \_ en X3DAudio.h y en otra parte. XAudio2 requiere que las máscaras de canal sean 0 o que tengan el mismo número de bits establecido que el número de canales.

En la tabla siguiente se muestran los requisitos de máscara de canal y los valores predeterminados para los formatos admitidos por XAudio2. 

| Formato | Requisito de máscara de canal             | Máscara predeterminada                        | Miembro de estructura correspondiente                            |
|--------|--------------------------------------|-------------------------------------|-----------------------------------------------------------|
| PCM    | El archivo puede contener una máscara de canal    | La máscara de canal es 0 o está ausente        | SELECIÓNATEXTENSIBLE.dwChannelMask o ninguno (FORMADEDATOATEX) |
| Adpcm  | El archivo no contiene una máscara de canal | Siempre se usa la máscara de canal predeterminada | Ninguno (ADPCMWAVEFORMAT)                                    |



 

Para las voces de submezcla y mastering, y para las voces de origen sin una máscara de canal o una máscara de canal de 0, XAudio2 asume las posiciones predeterminadas del hablante según la tabla siguiente. 

| Canales  | Posiciones implícitas del canal                                                                                            |
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| 1         | Siempre se asigna a FrontLeft y FrontRight a escala completa en ambos altavoces (caso especial para sonidos mono)                 |
| 2         | FrontLeft, FrontRight (configuración estéreo básica)                                                                    |
| 3         | FrontLeft, FrontRight, LowFrequency (configuración 2.1)                                                               |
| 4         | FrontLeft, FrontRight, BackLeft, BackRight (quadrafónico)                                                             |
| 5         | FrontLeft, FrontRight, FrontCenter, SideLeft, SideRight (configuración 5.0)                                           |
| 6         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight (configuración 5.1) (consulte los comentarios siguientes) |
| 7         | FrontLeft, FrontRight, FrontCenter, LowFrequency, SideLeft, SideRight, BackCenter (configuración 6.1)                 |
| 8         | FrontLeft, FrontRight, FrontCenter, LowFrequency, BackLeft, BackRight, SideLeft, SideRight (configuración 7.1)        |
| 9 o más | Sin posiciones implícitas (asignación uno a uno)                                                                            |



 

Si un par de voz determinado en el gráfico de audio no tiene posiciones de altavoz asociadas a su voz de origen o de destino (una voz tiene más de ocho canales), ninguna voz se puede reproducir hasta que la voz de origen tenga un conjunto de matrices de envío explícitamente mediante el método [**IXAudio2Voice::SetOutputMatrix.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) Se producirá un error al llamar al [**método IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para cualquiera de las voces hasta que lo haga.

Si la voz de origen y la voz de destino tienen un número diferente de posiciones del hablante e [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) no se ha llamado en la voz de origen, XAudio2 envía cada canal de origen al orador de destino (o altavoces) más cercano disponible, proporcionalmente a la proximidad que tienen al hablante previsto. Hay dos casos especiales en los que el comportamiento predeterminado es diferente.

1.  Si el audio de origen es mono y se coloca en SPEAKER FRONT CENTER o no tiene ninguna posición definida, siempre se envía a SPEAKER FRONT LEFT y SPEAKER FRONT RIGHT si existen en el \_ \_ audio de \_ \_ \_ \_ salida. Si no existen, vuelve al caso normal.
2.  Si el origen y el destino son de 6 canales y se sitúan en cualquiera de las configuraciones estándar del hablante 5.1 (Izquierda+Derecha+Centro+Sub+BackL+BackR o Izquierda+Derecha+Centro+Sub+SideL+SideR), los canales se asignan a través de uno a uno. En otras palabras, SideLeft/Right y BackLeft/Right se tratan de forma equivalente. Esto se debe a que ha habido confusión histórica en torno a estas configuraciones. Por lo tanto, la intención que se supone siempre es asignar uno a uno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Voces](voices.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[**GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)
</dt> </dl>

 

 
