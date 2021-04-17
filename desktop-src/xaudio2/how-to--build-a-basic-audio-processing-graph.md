---
description: El requisito mínimo para habilitar XAudio2 para reproducir datos de audio es un gráfico de procesamiento de audio, que se crea a partir de una sola voz de masterización y una sola voz de origen.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Cómo: crear un gráfico de procesamiento de audio básico'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716379"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>Cómo: crear un gráfico de procesamiento de audio básico

El requisito mínimo para habilitar XAudio2 para reproducir datos de audio es un gráfico de procesamiento de audio, que se crea a partir de una sola voz de masterización y una sola voz de origen.

## <a name="to-build-a-basic-audio-processing-graph"></a>Para compilar un gráfico básico de procesamiento de audio

1.  Inicialice el motor de XAudio2 siguiendo los pasos descritos en [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md).
2.  Rellene una estructura [**de \_ búfer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) de **WAVEFORMATEX** y XAUDIO2 siguiendo los pasos descritos en [Cómo: cargar archivos de datos de audio en XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).
3.  Cree una voz de origen mediante la función [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .

    Cuando se especifica NULL para el argumento pSendList de [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), la salida de la voz de origen se dirige a la voz de mastering creada en el paso 1.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Después de finalizar este paso, hay un gráfico de audio simple que consta de la voz de origen, la voz de la maestra y el dispositivo de audio. En los pasos restantes de este tema de procedimientos se muestra cómo iniciar el flujo de datos de audio a través del gráfico.

    Un gráfico de audio simple

    ![un gráfico de audio simple.](images/xaudio2-audio-graph.png)

4.  Use la función [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) para enviar un [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) a la voz de origen.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Utilice la función [**iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar la voz de origen.

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gráficos de audio](audio-graphs.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> </dl>

 

 
