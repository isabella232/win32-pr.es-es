---
description: En este tema se muestra cómo se puede cambiar el volumen de una voz a nivel general, en cada canal de salida o entre cada canal de una voz y otra voz en su sendlist.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Cómo: cambiar el volumen de la voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815283"
---
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="91123-103">Cómo: cambiar el volumen de la voz</span><span class="sxs-lookup"><span data-stu-id="91123-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="91123-104">En este tema se muestra cómo se puede cambiar el volumen de una voz a nivel general, en cada canal de salida o entre cada canal de una voz y otra voz en su [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="91123-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="91123-105">Para establecer un nivel de volumen general para la entrada de la voz</span><span class="sxs-lookup"><span data-stu-id="91123-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="91123-106">Utilice la función [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .</span><span class="sxs-lookup"><span data-stu-id="91123-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="91123-107">Para establecer el volumen de los canales de salida de la voz</span><span class="sxs-lookup"><span data-stu-id="91123-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="91123-108">Cree una matriz de números de punto flotante que contenga los volúmenes deseados de todos los canales de salida de la voz.</span><span class="sxs-lookup"><span data-stu-id="91123-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="91123-109">La matriz tendrá una entrada para cada canal de la voz.</span><span class="sxs-lookup"><span data-stu-id="91123-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="91123-110">Utilice la función [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) para establecer el volumen de los canales de salida.</span><span class="sxs-lookup"><span data-stu-id="91123-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="91123-111">Para establecer el volumen de conexiones</span><span class="sxs-lookup"><span data-stu-id="91123-111">To set the volume of connections</span></span>

<span data-ttu-id="91123-112">Establezca el volumen de conexión entre la voz y una voz en su [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="91123-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="91123-113">Cree una matriz de números de punto flotante que defina una matriz de salida si la voz se envía a otra voz.</span><span class="sxs-lookup"><span data-stu-id="91123-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="91123-114">La matriz debe tener un número de entradas igual a canales de voz de origen × canales de voz de destino.</span><span class="sxs-lookup"><span data-stu-id="91123-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="91123-115">En este ejemplo, la asignación es de una voz con un canal a una voz con dos canales.</span><span class="sxs-lookup"><span data-stu-id="91123-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="91123-116">Use la función [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) para establecer la matriz de salida.</span><span class="sxs-lookup"><span data-stu-id="91123-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="91123-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91123-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91123-118">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="91123-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="91123-119">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="91123-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="91123-120">Volumen y control de paso de XAudio2</span><span class="sxs-lookup"><span data-stu-id="91123-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
