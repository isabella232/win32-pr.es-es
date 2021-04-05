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
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="6347a-103">Cómo: integrar X3DAudio con XAudio2</span><span class="sxs-lookup"><span data-stu-id="6347a-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="6347a-104">En este tema se muestra cómo integrar X3DAudio con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="6347a-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="6347a-105">Puede usar X3DAudio para proporcionar los valores de volumen y de paso para las voces de XAudio2 y los parámetros del efecto de reverberación integrado en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="6347a-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="6347a-106">En este tema se supone que ha creado un gráfico de audio como se describe en [Cómo: compilar un gráfico básico de procesamiento de audio](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="6347a-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="6347a-107">Si aún no ha creado un gráfico de audio, se producirá un error en [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) .</span><span class="sxs-lookup"><span data-stu-id="6347a-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="6347a-108">**Para inicializar X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="6347a-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="6347a-109">Inicialice X3DAudio llamando a [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span><span class="sxs-lookup"><span data-stu-id="6347a-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="6347a-110">La función [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) toma marcas que indican la configuración del altavoz, la velocidad del sonido en unidades universales definidas por el usuario por segundo y un identificador para devolver una instancia del motor de X3DAudio.</span><span class="sxs-lookup"><span data-stu-id="6347a-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="6347a-111">Llame a [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para obtener la máscara de canal del formato de salida.</span><span class="sxs-lookup"><span data-stu-id="6347a-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="6347a-112">Cree instancias de las estructuras [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) y [**X3DAUDIO \_ emisor**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="6347a-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="6347a-113">La estructura del [**\_ agente de escucha de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) representa la posición de lo que oye el sonido.</span><span class="sxs-lookup"><span data-stu-id="6347a-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="6347a-114">Por lo general, se trata de la posición de la cámara o de una posición cercana a ella.</span><span class="sxs-lookup"><span data-stu-id="6347a-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="6347a-115">La estructura de [**\_ emisor X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) representa la posición de la cosa que realiza el sonido.</span><span class="sxs-lookup"><span data-stu-id="6347a-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="6347a-116">Habrá una estructura de **\_ emisor X3DAUDIO** para cada sonido del que se realiza el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="6347a-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="6347a-117">Los miembros de las estructuras que no se actualizarán en un bucle de juego se deben inicializar aquí.</span><span class="sxs-lookup"><span data-stu-id="6347a-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="6347a-118">La mayoría de los miembros de las estructuras simplemente se pueden inicializar en cero.</span><span class="sxs-lookup"><span data-stu-id="6347a-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="6347a-119">Sin embargo, algunos miembros [**del \_ emisor de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) deben configurarse para que se inicialicen en valores distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="6347a-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="6347a-120">El miembro ChannelCount del **\_ emisor de X3DAUDIO** debe inicializarse en el número de canales de la voz que representa el emisor.</span><span class="sxs-lookup"><span data-stu-id="6347a-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="6347a-121">Además, el miembro CurveDistanceScaler del **\_ emisor de X3DAUDIO** debe estar en el intervalo de FLT \_ min a FLT \_ máx.</span><span class="sxs-lookup"><span data-stu-id="6347a-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="6347a-122">Cree una instancia de la estructura de [**\_ \_ configuración de DSP de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) .</span><span class="sxs-lookup"><span data-stu-id="6347a-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="6347a-123">La estructura de [**\_ \_ configuración de X3DAUDIO DSP**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) se usa para devolver los resultados calculados por [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span><span class="sxs-lookup"><span data-stu-id="6347a-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="6347a-124">La función **X3DAudioCalculate** no asigna memoria para ninguno de sus parámetros.</span><span class="sxs-lookup"><span data-stu-id="6347a-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="6347a-125">Esto significa que debe asignar matrices para los miembros pMatrixCoefficients y pDelayTimes de la estructura de **\_ \_ configuración de X3DAUDIO DSP** , si tiene previsto usarlas.</span><span class="sxs-lookup"><span data-stu-id="6347a-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="6347a-126">Además, debe establecer los miembros SrcChannelCount y DstChannelCount en el número de canales en las voces de origen y de destino del emisor.</span><span class="sxs-lookup"><span data-stu-id="6347a-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="6347a-127">Use [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) en la voz de la maestra para obtener el número de InputChannels para **nChannels**.</span><span class="sxs-lookup"><span data-stu-id="6347a-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="6347a-128">Para las versiones del SDK de DirectX de XAUDIO2 anteriores a Windows 8, use IXAudio2:: GetDeviceDetails.</span><span class="sxs-lookup"><span data-stu-id="6347a-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="6347a-129">Siga estos pasos una vez cada dos o tres fotogramas para calcular los nuevos valores y aplicarlos.</span><span class="sxs-lookup"><span data-stu-id="6347a-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="6347a-130">En este ejemplo, una voz de origen envía directamente a la voz de maestro y a una voz de submezcla con un efecto de reverberación aplicado a ella.</span><span class="sxs-lookup"><span data-stu-id="6347a-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="6347a-131">**Para usar X3DAudio para calcular y aplicar la nueva configuración de audio 3D**</span><span class="sxs-lookup"><span data-stu-id="6347a-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="6347a-132">Actualice el [**\_ agente de escucha de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) y las estructuras de [**\_ emisor de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) con su posición actual, velocidad y orientación.</span><span class="sxs-lookup"><span data-stu-id="6347a-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

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

    

2.  <span data-ttu-id="6347a-133">Llame a [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) para calcular los nuevos valores para las voces.</span><span class="sxs-lookup"><span data-stu-id="6347a-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="6347a-134">Los parámetros de [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) serán las estructuras de [**\_ emisores**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) X3DAUDIO y de [**\_ escucha**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) X3DAUDIO actualizadas.</span><span class="sxs-lookup"><span data-stu-id="6347a-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="6347a-135">Las marcas indicarán qué valores deben calcular **X3DAudioCalculate** y qué estructura [**de \_ \_ configuración del DSP de X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) contendrá los resultados de los cálculos realizados.</span><span class="sxs-lookup"><span data-stu-id="6347a-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="6347a-136">Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) y [**IXAudio2SourceVoice:: SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para aplicar los valores de volumen y de paso a la voz de origen.</span><span class="sxs-lookup"><span data-stu-id="6347a-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="6347a-137">Use [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para aplicar el nivel de reverberación calculado a la voz de submezcla.</span><span class="sxs-lookup"><span data-stu-id="6347a-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="6347a-138">Use [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) para aplicar el coeficiente de filtro directo de baja pasada calculada a la voz de origen.</span><span class="sxs-lookup"><span data-stu-id="6347a-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="6347a-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6347a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6347a-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="6347a-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="6347a-141">Información general de X3DAudio</span><span class="sxs-lookup"><span data-stu-id="6347a-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="6347a-142">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="6347a-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6347a-143">Volumen y control de paso de XAudio2</span><span class="sxs-lookup"><span data-stu-id="6347a-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
