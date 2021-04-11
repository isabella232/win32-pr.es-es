---
description: En este tema se muestra cómo puede aumentar o reducir el paso de los datos de audio cambiando la velocidad de reproducción mediante la función SetFrequencyRatio en una voz de origen.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Cómo: cambiar el tono de la voz'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154617"
---
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="a399e-103">Cómo: cambiar el tono de la voz</span><span class="sxs-lookup"><span data-stu-id="a399e-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="a399e-104">En este tema se muestra cómo puede aumentar o reducir el paso de los datos de audio cambiando la velocidad de reproducción mediante la función [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) en una voz de origen.</span><span class="sxs-lookup"><span data-stu-id="a399e-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="a399e-105">Para cambiar el tono de una voz de origen</span><span class="sxs-lookup"><span data-stu-id="a399e-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="a399e-106">Determine la relación de frecuencia deseada para la [**voz de origen**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span><span class="sxs-lookup"><span data-stu-id="a399e-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="a399e-107">Consulte [volumen de XAudio2 y control de paso](xaudio2-volume-and-pitch-control.md) para obtener más información sobre cómo calcular la relación de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="a399e-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="a399e-108">Utilice la función [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) para establecer la relación de frecuencia de la voz de origen.</span><span class="sxs-lookup"><span data-stu-id="a399e-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="a399e-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a399e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a399e-110">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="a399e-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a399e-111">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="a399e-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="a399e-112">Volumen y control de paso de XAudio2</span><span class="sxs-lookup"><span data-stu-id="a399e-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
