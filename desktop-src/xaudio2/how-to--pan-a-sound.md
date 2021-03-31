---
description: En este tema se muestra cómo puede establecer la matriz de salida de una voz de origen mono que se envía a una voz de masterización estéreo con el fin de lograr la panorámica entre los altavoces izquierdo y derecho.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Cómo: desplazar un sonido'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911101"
---
# <a name="how-to-pan-a-sound"></a><span data-ttu-id="87d2d-103">Cómo: desplazar un sonido</span><span class="sxs-lookup"><span data-stu-id="87d2d-103">How to: Pan a Sound</span></span>

<span data-ttu-id="87d2d-104">En este tema se muestra cómo puede establecer la matriz de salida de una voz de origen mono que se envía a una voz de masterización estéreo con el fin de lograr la panorámica entre los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="87d2d-104">This topic shows you how you can set the output matrix of a mono source voice that outputs to a stereo mastering voice in order to achieve panning between the left and right speakers.</span></span>

## <a name="to-setup-panning"></a><span data-ttu-id="87d2d-105">Para configurar el movimiento panorámico</span><span class="sxs-lookup"><span data-stu-id="87d2d-105">To setup panning</span></span>

1.  <span data-ttu-id="87d2d-106">Recupere la configuración de los altavoces mediante [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="87d2d-106">Retrieve the speaker configuration using [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  <span data-ttu-id="87d2d-107">Cree una matriz que contenga la matriz de salida.</span><span class="sxs-lookup"><span data-stu-id="87d2d-107">Create an array to hold the output matrix.</span></span> <span data-ttu-id="87d2d-108">El tamaño mínimo de la matriz de salida es el número de canales de la voz de origen que tiene el número de canales de la voz de salida.</span><span class="sxs-lookup"><span data-stu-id="87d2d-108">The minimum size of the output matrix is the number of channels in the source voice times the number of channels in the output voice.</span></span> <span data-ttu-id="87d2d-109">En este caso, una matriz de ocho elementos controlará una voz mono con cualquier formato de salida hasta 7,1 sonido envolvente.</span><span class="sxs-lookup"><span data-stu-id="87d2d-109">In this case an eight element array will handle a mono voice outputting to any output format up to 7.1 surround sound.</span></span>

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  <span data-ttu-id="87d2d-110">Calcular los niveles de envío en función de la panorámica deseada entre los altavoces izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="87d2d-110">Calculate the send levels based on the desired panning between the left and right speakers.</span></span> <span data-ttu-id="87d2d-111">En este ejemplo, los valores de la panorámica oscilarán entre-1 y 1 con-1, lo que indica todo el sonido hasta el altavoz izquierdo y 1, que indica el sonido del altavoz derecho.</span><span class="sxs-lookup"><span data-stu-id="87d2d-111">In this example, pan values will range from -1 to 1 with -1 indicating all sound to the left speaker and 1 indicating all sound to the right speaker.</span></span>

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  <span data-ttu-id="87d2d-112">Establezca los índices de matriz de salida correspondientes a los altavoces izquierdo y derecho con los valores calculados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="87d2d-112">Set the output matrix indices corresponding to the left and right speakers with the values calculated in the previous step.</span></span> <span data-ttu-id="87d2d-113">Los oradores izquierdo y derecho se determinan examinando la máscara de canal devuelta por [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="87d2d-113">The left and right speakers are determined by looking at the channel mask returned by [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span> <span data-ttu-id="87d2d-114">Puesto que los canales siempre deben estar codificados en el orden especificado en la página de referencia de [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , es posible determinar el índice de matriz correspondiente a un orador individual.</span><span class="sxs-lookup"><span data-stu-id="87d2d-114">Since the channels must always be encoded in the order specified on the [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) reference page, it is possible to determine the array index corresponding to an individual speaker.</span></span>

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  <span data-ttu-id="87d2d-115">Aplique la matriz de salida a la voz de origen mediante [**IXAudio2Voice:: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span><span class="sxs-lookup"><span data-stu-id="87d2d-115">Apply the output matrix to the originating voice by using [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span></span> <span data-ttu-id="87d2d-116">La voz de origen será una voz de origen o una voz de submezcla que envía a una voz de submezcla o a una voz de la maestra.</span><span class="sxs-lookup"><span data-stu-id="87d2d-116">The originating voice will be either a source voice or a submix voice sending to either a submix voice or a mastering voice.</span></span> <span data-ttu-id="87d2d-117">Puede obtener información sobre las voces de origen y de destino, como su número de canales, mediante [**IXAudio2Voice:: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span><span class="sxs-lookup"><span data-stu-id="87d2d-117">You can get info about the originating and destination voices, like their number of channels, by using [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span></span>

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="87d2d-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87d2d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87d2d-119">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="87d2d-119">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="87d2d-120">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="87d2d-120">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="87d2d-121">Volumen y control de paso de XAudio2</span><span class="sxs-lookup"><span data-stu-id="87d2d-121">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
