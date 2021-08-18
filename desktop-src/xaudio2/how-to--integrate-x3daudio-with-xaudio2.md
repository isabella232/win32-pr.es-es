---
description: En este tema se muestra cómo integrar X3DAudio con XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Cómo: integrar X3DAudio con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c940acbe78e8d4ca4247f77500adeeca7c9619057a3008dea50fc8b55a9f364e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962694"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Cómo: integrar X3DAudio con XAudio2

En este tema se muestra cómo integrar X3DAudio con XAudio2. Puede usar X3DAudio para proporcionar los valores de volumen y tono para las voces XAudio2 y los parámetros para el efecto de reverberación integrado de XAudio2. En este tema se supone que ha creado un gráfico de audio como se describe en [Cómo:](how-to--build-a-basic-audio-processing-graph.md)Compilar un procesamiento de audio básico Graph . Si aún no ha creado un gráfico de audio, se producirá un error [**en X3DAudioInitialize.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

**Para inicializar X3DAudio**

1.  Inicialice X3DAudio llamando a [**X3DAudioInitialize.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    La función [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) toma marcas que indican la configuración del altavoz, la velocidad del sonido en las unidades de mundo definidas por el usuario por segundo y un identificador para devolver una instancia del motor X3DAudio. Llame [**a IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para obtener la máscara de canal del formato de salida.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Cree instancias de las estructuras [**X3DAUDIO \_ LISTENER y**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) [**X3DAUDIO \_ EMITTER.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

    La [**estructura del agente de \_ escucha X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) representa la posición de lo que escucha el sonido. Por lo general, esta es la posición de la cámara o una posición cercana a ella. La [**estructura \_ EMITTER X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) representa la posición de la cosa que hace el sonido. Habrá una estructura **emitter \_ X3DAUDIO** para cada sonido del que se realiza el seguimiento.

    Los miembros de las estructuras que no se actualizarán en un bucle de juego se deben inicializar aquí. La mayoría de los miembros de las estructuras simplemente se pueden inicializar en cero. Sin embargo, algunos miembros [**de X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) deben establecerse para inicializarse en valores distintos de cero. El miembro ChannelCount del emisor **X3DAUDIO \_** debe inicializarse en el número de canales de la voz que representa el emisor. Además, el miembro CurveDistanceScaler de **X3DAUDIO \_ EMITTER** debe estar en el intervalo FLT \_ MIN a FLT \_ MAX.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Cree una instancia de la estructura [**X3DAUDIO \_ DSP \_ SETTINGS.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)

    La [**estructura X3DAUDIO \_ DSP \_ SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) se usa para devolver los resultados calculados por [**X3DAudioCalculate.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) La **función X3DAudioCalculate** no asigna memoria para ninguno de sus parámetros. Esto significa que debe asignar matrices para los miembros pMatrixCoefficients y pDelayTimes de la estructura **\_ de DSP \_ SETTINGS de X3DAUDIO** si piensa usarlos. Además, debe establecer los miembros SrcChannelCount y DstChannelCount en el número de canales de las voces de origen y destino del emisor.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) en la voz maestra para obtener el número de InputChannels para **nChannels.** Para las versiones del SDK de DirectX de XAUDIO2 antes Windows 8, use IXAudio2::GetDeviceDetails.

     

Realice estos pasos una vez cada dos o tres fotogramas para calcular la nueva configuración y aplicarlos. En este ejemplo, una voz de origen se envía directamente a la voz maestra y a una voz de submezcla con un efecto de reverberación aplicado.

**Para usar X3DAudio para calcular y aplicar una nueva configuración de audio 3D**

1.  Actualice las [**estructuras X3DAUDIO \_ LISTENER y**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) con su posición, velocidad y orientación actuales.

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  Llame [**a X3DAudioCalculate para**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) calcular la nueva configuración de las voces.

    Los parámetros de [**X3DAudioCalculate serán**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) las estructuras [**X3DAUDIO \_ LISTENER y**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) actualizadas. Las marcas indicarán qué valores debe calcular **X3DAudioCalculate** y qué estructura DE CONFIGURACIÓN de DSP de [**X3DAUDIO \_ \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) contendrán los resultados de los cálculos realizados.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) e [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar los valores de volumen y tono a la voz de origen.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Use [**IXAudio2Voice::SetOutputMatrix para**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) aplicar el nivel de reverberación calculado a la voz de submezcla.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para aplicar el coeficiente directo del filtro de paso bajo calculado a la voz de origen.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Información general sobre X3DAudio](x3daudio-overview.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Control de volumen y tono de XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
