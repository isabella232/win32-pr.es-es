---
description: En este tema se muestra cómo integrar X3DAudio con XAudio2.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: 'Cómo: integrar X3DAudio con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815278"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>Cómo: integrar X3DAudio con XAudio2

En este tema se muestra cómo integrar X3DAudio con XAudio2. Puede usar X3DAudio para proporcionar los valores de volumen y de paso para las voces de XAudio2 y los parámetros del efecto de reverberación integrado en XAudio2. En este tema se supone que ha creado un gráfico de audio como se describe en [Cómo: compilar un gráfico básico de procesamiento de audio](how-to--build-a-basic-audio-processing-graph.md). Si aún no ha creado un gráfico de audio, se producirá un error en [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) .

**Para inicializar X3DAudio**

1.  Inicialice X3DAudio llamando a [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    La función [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) toma marcas que indican la configuración del altavoz, la velocidad del sonido en unidades universales definidas por el usuario por segundo y un identificador para devolver una instancia del motor de X3DAudio. Llame a [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para obtener la máscara de canal del formato de salida.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Cree instancias de las estructuras [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) y [**X3DAUDIO \_ emisor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .

    La estructura del [**\_ agente de escucha de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) representa la posición de lo que oye el sonido. Por lo general, se trata de la posición de la cámara o de una posición cercana a ella. La estructura de [**\_ emisor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) representa la posición de la cosa que realiza el sonido. Habrá una estructura de **\_ emisor X3DAUDIO** para cada sonido del que se realiza el seguimiento.

    Los miembros de las estructuras que no se actualizarán en un bucle de juego se deben inicializar aquí. La mayoría de los miembros de las estructuras simplemente se pueden inicializar en cero. Sin embargo, algunos miembros [**del \_ emisor de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) deben configurarse para que se inicialicen en valores distintos de cero. El miembro ChannelCount del **\_ emisor de X3DAUDIO** debe inicializarse en el número de canales de la voz que representa el emisor. Además, el miembro CurveDistanceScaler del **\_ emisor de X3DAUDIO** debe estar en el intervalo de FLT \_ min a FLT \_ máx.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Cree una instancia de la estructura de [**\_ \_ configuración de DSP de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .

    La estructura de [**\_ \_ configuración de X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) se usa para devolver los resultados calculados por [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate). La función **X3DAudioCalculate** no asigna memoria para ninguno de sus parámetros. Esto significa que debe asignar matrices para los miembros pMatrixCoefficients y pDelayTimes de la estructura de **\_ \_ configuración de X3DAUDIO DSP** , si tiene previsto usarlas. Además, debe establecer los miembros SrcChannelCount y DstChannelCount en el número de canales en las voces de origen y de destino del emisor.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Use [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) en la voz de la maestra para obtener el número de InputChannels para **nChannels**. Para las versiones del SDK de DirectX de XAUDIO2 anteriores a Windows 8, use IXAudio2:: GetDeviceDetails.

     

Siga estos pasos una vez cada dos o tres fotogramas para calcular los nuevos valores y aplicarlos. En este ejemplo, una voz de origen envía directamente a la voz de maestro y a una voz de submezcla con un efecto de reverberación aplicado a ella.

**Para usar X3DAudio para calcular y aplicar la nueva configuración de audio 3D**

1.  Actualice el [**\_ agente de escucha de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) y las estructuras de [**\_ emisor de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) con su posición actual, velocidad y orientación.

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

    

2.  Llame a [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) para calcular los nuevos valores para las voces.

    Los parámetros de [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) serán las estructuras de [**\_ emisores**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) X3DAUDIO y de [**\_ escucha**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) X3DAUDIO actualizadas. Las marcas indicarán qué valores deben calcular **X3DAudioCalculate** y qué estructura [**de \_ \_ configuración del DSP de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) contendrá los resultados de los cálculos realizados.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) y [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar los valores de volumen y de paso a la voz de origen.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para aplicar el nivel de reverberación calculado a la voz de submezcla.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Use [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para aplicar el coeficiente de filtro directo de baja pasada calculada a la voz de origen.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Información general de X3DAudio](x3daudio-overview.md)
</dt> <dt>

[Guía de programación de XAudio2](programming-guide.md)
</dt> <dt>

[Volumen y control de paso de XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
