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
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="db5a3-103">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="db5a3-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="db5a3-104">El requisito mínimo para habilitar XAudio2 para reproducir datos de audio es un gráfico de procesamiento de audio, que se crea a partir de una sola voz de masterización y una sola voz de origen.</span><span class="sxs-lookup"><span data-stu-id="db5a3-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="db5a3-105">Para compilar un gráfico básico de procesamiento de audio</span><span class="sxs-lookup"><span data-stu-id="db5a3-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="db5a3-106">Inicialice el motor de XAudio2 siguiendo los pasos descritos en [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="db5a3-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="db5a3-107">Rellene una estructura [**de \_ búfer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) de **WAVEFORMATEX** y XAUDIO2 siguiendo los pasos descritos en [Cómo: cargar archivos de datos de audio en XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="db5a3-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="db5a3-108">Cree una voz de origen mediante la función [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .</span><span class="sxs-lookup"><span data-stu-id="db5a3-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="db5a3-109">Cuando se especifica NULL para el argumento pSendList de [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), la salida de la voz de origen se dirige a la voz de mastering creada en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="db5a3-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="db5a3-110">Después de finalizar este paso, hay un gráfico de audio simple que consta de la voz de origen, la voz de la maestra y el dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="db5a3-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="db5a3-111">En los pasos restantes de este tema de procedimientos se muestra cómo iniciar el flujo de datos de audio a través del gráfico.</span><span class="sxs-lookup"><span data-stu-id="db5a3-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="db5a3-112">Un gráfico de audio simple</span><span class="sxs-lookup"><span data-stu-id="db5a3-112">A simple audio graph</span></span>

    ![un gráfico de audio simple.](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="db5a3-114">Use la función [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) para enviar un [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) a la voz de origen.</span><span class="sxs-lookup"><span data-stu-id="db5a3-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="db5a3-115">Utilice la función [**iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar la voz de origen.</span><span class="sxs-lookup"><span data-stu-id="db5a3-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="db5a3-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db5a3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db5a3-117">Gráficos de audio</span><span class="sxs-lookup"><span data-stu-id="db5a3-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="db5a3-118">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="db5a3-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
