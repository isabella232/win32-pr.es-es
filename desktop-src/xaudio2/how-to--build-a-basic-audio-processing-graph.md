---
description: El requisito mínimo para permitir que XAudio2 reprodgue datos de audio es un gráfico de procesamiento de audio, que se construye a partir de una sola voz maestra y una sola voz de origen.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Cómo: crear un gráfico de procesamiento de audio básico'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bab39c878b37a6f89ef7598f6fa6b6eb1a997654373122fe3c3980bf12f160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082969"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a>Cómo: crear un gráfico de procesamiento de audio básico

El requisito mínimo para permitir que XAudio2 reprodgue datos de audio es un gráfico de procesamiento de audio, que se construye a partir de una sola voz maestra y una sola voz de origen.

## <a name="to-build-a-basic-audio-processing-graph"></a>Para crear un gráfico de procesamiento de audio básico

1.  Inicialice el motor XAudio2 siguiendo los pasos descritos [en Cómo: Inicializar XAudio2.](how-to--initialize-xaudio2.md)
2.  Rellene una **estructura DE BÚFERES DE DESATEX** y [**XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) siguiendo los pasos descritos en Cómo: Cargar archivos de datos de [audio en XAudio2.](how-to--load-audio-data-files-in-xaudio2.md)
3.  Cree una voz de origen mediante [**la función CreateSourceVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)

    Al especificar NULL para el argumento pSendList de [**CreateSourceVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)la salida de la voz de origen va a la voz maestra creada en el paso 1.

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    Después de finalizar este paso, hay un gráfico de audio simple que consta de la voz de origen, la voz maestra y el dispositivo de audio. Los pasos restantes de este tema de procedimientos muestran cómo iniciar el flujo de datos de audio a través del gráfico.

    Un gráfico de audio simple

    ![un gráfico de audio simple.](images/xaudio2-audio-graph.png)

4.  Use la función [**SubmitSourceBuffer para**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) enviar un [**\_ búfer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) a la voz de origen.

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  Use la [**función Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar la voz de origen.

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

 

 
