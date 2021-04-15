---
description: Trabajar con barras cruzadas
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Trabajar con barras cruzadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688602"
---
# <a name="working-with-crossbars"></a><span data-ttu-id="271db-103">Trabajar con barras cruzadas</span><span class="sxs-lookup"><span data-stu-id="271db-103">Working with Crossbars</span></span>

<span data-ttu-id="271db-104">Si una tarjeta de captura de vídeo tiene más de una entrada física o admite más de una ruta de acceso de hardware para los datos, el gráfico de filtros puede contener el [filtro de barras de vídeo analógicas](analog-video-crossbar-filter.md).</span><span class="sxs-lookup"><span data-stu-id="271db-104">If a video capture card has more than one physical input, or supports more than one hardware path for data, then the filter graph may contain the [Analog Video Crossbar Filter](analog-video-crossbar-filter.md).</span></span> <span data-ttu-id="271db-105">El generador de gráficos de captura agrega automáticamente este filtro cuando sea necesario. será ascendente desde el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="271db-105">The Capture Graph Builder automatically adds this filter when needed; it will be upstream from the capture filter.</span></span> <span data-ttu-id="271db-106">Dependiendo del hardware, el gráfico de filtros podría contener más de una instancia del filtro de barras cruzadas.</span><span class="sxs-lookup"><span data-stu-id="271db-106">Depending on the hardware, the filter graph might contain more than one instance of the crossbar filter.</span></span>

<span data-ttu-id="271db-107">El filtro de barras cruzadas expone la interfaz [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , que puede usar para enrutar una entrada determinada a una salida determinada.</span><span class="sxs-lookup"><span data-stu-id="271db-107">The crossbar filter exposes the [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) interface, which you can use to route a particular input to a particular output.</span></span> <span data-ttu-id="271db-108">Por ejemplo, una tarjeta de vídeo puede tener un conector coaxial y una entrada de S-video.</span><span class="sxs-lookup"><span data-stu-id="271db-108">For example, a video card might have a coaxial connector and an S-Video input.</span></span> <span data-ttu-id="271db-109">Se representarán como clavijas de entrada en el filtro de barras cruzadas.</span><span class="sxs-lookup"><span data-stu-id="271db-109">These would be represented as input pins on the crossbar filter.</span></span> <span data-ttu-id="271db-110">Para seleccionar una entrada, enrute el PIN de entrada correspondiente a la clavija de salida de las barras cruzadas mediante el método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="271db-110">To select an input, route the corresponding input pin to the crossbar's output pin, using the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

<span data-ttu-id="271db-111">Para buscar los filtros de barras cruzadas en el gráfico, puede usar el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar filtros que admitan **IAMCrossbar**.</span><span class="sxs-lookup"><span data-stu-id="271db-111">To locate crossbar filters in the graph, you can use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to search for filters that support **IAMCrossbar**.</span></span> <span data-ttu-id="271db-112">Por ejemplo, el código siguiente busca dos barras cruzadas:</span><span class="sxs-lookup"><span data-stu-id="271db-112">For example, the following code searches for two crossbars:</span></span>


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



<span data-ttu-id="271db-113">Para obtener un enfoque más generalizado, consulte la clase CCrossbar en el [ejemplo AMCAP](amcap-sample.md).</span><span class="sxs-lookup"><span data-stu-id="271db-113">For a more generalized approach, see the CCrossbar class in the [AmCap Sample](amcap-sample.md).</span></span>

<span data-ttu-id="271db-114">Una vez que tenga un puntero a la interfaz **IAMCrossbar** , puede obtener información sobre el filtro de barras cruzadas, incluido el tipo físico de cada pin, y la matriz de los pines de entrada que se pueden enrutar a los terminales de salida.</span><span class="sxs-lookup"><span data-stu-id="271db-114">Once you have a pointer to the **IAMCrossbar** interface, you can get information about the crossbar filter, including the physical type of each pin, and the matrix of which input pins can be routed to which output pins.</span></span>

-   <span data-ttu-id="271db-115">Para determinar el tipo de conector físico al que corresponde un PIN, llame al método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) .</span><span class="sxs-lookup"><span data-stu-id="271db-115">To determine the type of physical connector to which a pin corresponds, call the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method.</span></span> <span data-ttu-id="271db-116">El método devuelve un miembro de la enumeración [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) .</span><span class="sxs-lookup"><span data-stu-id="271db-116">The method returns a member of the [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) enumeration.</span></span> <span data-ttu-id="271db-117">Por ejemplo, un PIN de S-video devuelve el valor PhysConn \_ video \_ Svideo.</span><span class="sxs-lookup"><span data-stu-id="271db-117">For example, an S-Video pin returns the value PhysConn\_Video\_SVideo.</span></span>

    <span data-ttu-id="271db-118">El método **Get \_ CrossbarInfo** también indica si dos patillas están relacionadas entre sí.</span><span class="sxs-lookup"><span data-stu-id="271db-118">The **get\_CrossbarInfo** method also indicates whether two pins are related to each other.</span></span> <span data-ttu-id="271db-119">Por ejemplo, un PIN de sintonizador de vídeo puede estar relacionado con un PIN de sintonizador de audio.</span><span class="sxs-lookup"><span data-stu-id="271db-119">For example, a video tuner pin might be related to an audio tuner pin.</span></span> <span data-ttu-id="271db-120">Los pin relacionados tienen la misma dirección del PIN y normalmente forman parte del mismo conector físico o conector de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="271db-120">Related pins have the same pin direction, and are typically part of the same physical jack or connector on the card.</span></span>

-   <span data-ttu-id="271db-121">Para determinar si puede enrutar un PIN de entrada a un determinado PIN de salida, llame al método [**IAMCrossbar:: CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .</span><span class="sxs-lookup"><span data-stu-id="271db-121">To determine whether you can route an input pin to a particular output pin, call the [**IAMCrossbar::CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) method.</span></span>
-   <span data-ttu-id="271db-122">Para determinar el enrutamiento actual entre los pin, llame al método [**IAMCrossbar:: get \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .</span><span class="sxs-lookup"><span data-stu-id="271db-122">To determine the current routing between pins, call the [**IAMCrossbar::get\_IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) method.</span></span>

<span data-ttu-id="271db-123">Los métodos anteriores especifican los pin por número de índice, con clavijas de salida y clavijas de entrada indizadas a partir de cero.</span><span class="sxs-lookup"><span data-stu-id="271db-123">The previous methods all specify pins by index number, with output pins and input pins both indexed from zero.</span></span> <span data-ttu-id="271db-124">Llame al método **IAMCrossbar:: get \_ PinCounts** para buscar el número de PIN en el filtro.</span><span class="sxs-lookup"><span data-stu-id="271db-124">Call the **IAMCrossbar::get\_PinCounts** method to find the number of pins on the filter.</span></span>

<span data-ttu-id="271db-125">Por ejemplo, el código siguiente muestra información sobre un filtro de barras cruzadas en la ventana de la consola:</span><span class="sxs-lookup"><span data-stu-id="271db-125">For example, the following code displays information about a crossbar filter to the console window:</span></span>


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



<span data-ttu-id="271db-126">En el caso de una tarjeta hipotética, esta función podría generar el siguiente resultado:</span><span class="sxs-lookup"><span data-stu-id="271db-126">For a hypothetical card, this function might produce the following output:</span></span>


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



<span data-ttu-id="271db-127">En el lado de salida, los elementos de vídeo y sintonizador de vídeo están relacionados con el descodificador de audio.</span><span class="sxs-lookup"><span data-stu-id="271db-127">On the output side, the S-Video and the video tuner are both related to the audio decoder.</span></span> <span data-ttu-id="271db-128">En el lado de entrada, el sintonizador de vídeo está relacionado con el sintonizador de audio y el S-video está relacionado con la línea de audio en.</span><span class="sxs-lookup"><span data-stu-id="271db-128">On the input side, the video tuner is related to the audio tuner, and the S-Video is related to the audio line in.</span></span> <span data-ttu-id="271db-129">La entrada S-video se enruta a la salida S-video; y la entrada del sintonizador de vídeo se enruta a la salida del sintonizador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="271db-129">The S-Video input is routed to the S-Video output; and the video tuner input is routed to the video tuner output.</span></span> <span data-ttu-id="271db-130">Actualmente no se enruta nada al descodificador de audio, pero la línea de audio o el sintonizador de audio se pueden enrutar a él.</span><span class="sxs-lookup"><span data-stu-id="271db-130">Currently nothing is routed to the audio decoder, but either the audio line in or the audio tuner could be routed to it.</span></span>

<span data-ttu-id="271db-131">Puede cambiar el enrutamiento existente llamando al método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="271db-131">You can change the existing routing by calling the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

 

 



