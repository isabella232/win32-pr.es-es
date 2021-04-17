---
description: Obtener una vista previa del audio de TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Obtener una vista previa del audio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494866"
---
# <a name="previewing-tv-audio"></a><span data-ttu-id="e2a5e-103">Obtener una vista previa del audio de TV</span><span class="sxs-lookup"><span data-stu-id="e2a5e-103">Previewing TV Audio</span></span>

<span data-ttu-id="e2a5e-104">Para obtener una vista previa del audio de TV, enrute el PIN del descodificador de audio en el filtro de barras cruzadas al pin de sintonizador de audio.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-104">To preview TV audio, route the Audio Decoder pin on the crossbar filter to the Audio Tuner pin.</span></span> <span data-ttu-id="e2a5e-105">Para silenciar el audio, enrute el PIN del descodificador de audio a-1, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-105">To mute the audio, route the Audio Decoder pin to -1, as shown in the following diagram.</span></span> <span data-ttu-id="e2a5e-106">(Los filtros de barras cruzadas se describen en [trabajar con barras cruzadas](working-with-crossbars.md)).</span><span class="sxs-lookup"><span data-stu-id="e2a5e-106">(Crossbar filters are described in [Working with Crossbars](working-with-crossbars.md).)</span></span>

![enrutamiento del PIN del descodificador de audio](images/vidcap07.png)

<span data-ttu-id="e2a5e-108">El enfoque básico es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="e2a5e-108">The basic approach is as follows:</span></span>

1.  <span data-ttu-id="e2a5e-109">Use el método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para buscar el filtro de barras cruzadas.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-109">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the crossbar filter.</span></span>
2.  <span data-ttu-id="e2a5e-110">Use el método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) para enumerar los pines de entrada y salida del filtro de barras cruzadas.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-110">Use the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method to enumerate the crossbar filter's input and output pins.</span></span> <span data-ttu-id="e2a5e-111">Busque un PIN de salida de descodificador de audio y un PIN de entrada de sintonizador de audio.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-111">Search for an audio decoder output pin and an audio tuner input pin.</span></span>
3.  <span data-ttu-id="e2a5e-112">Si encuentra los pin correctos, llame a [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) para enrutar los pin.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-112">If you find the correct pins, call [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) to route the pins.</span></span> <span data-ttu-id="e2a5e-113">Si no es así, busque el flujo ascendente de otra Cruz y repita el proceso.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-113">If not, look upstream for another crossbar and repeat the process.</span></span>
4.  <span data-ttu-id="e2a5e-114">Para silenciar el audio, enrute el PIN del descodificador de audio a-1.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-114">To mute the audio, route the audio decoder pin to -1.</span></span>

<span data-ttu-id="e2a5e-115">La mayoría de los sintonizadores de TV usan un solo filtro de barras cruzadas, pero algunos usan dos filtros de barras cruzadas.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-115">Most TV tuners use a single crossbar filter, but some use two crossbar filters.</span></span> <span data-ttu-id="e2a5e-116">Por lo tanto, es posible que tenga que buscar una segunda cruz si se produce un error en la primera.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-116">Therefore, you might have to search for a second crossbar if the first one fails.</span></span>

> [!Note]  
> <span data-ttu-id="e2a5e-117">Contrariamente a lo que cabría esperar, no se requiere ningún filtro de captura de audio o representador de audio para obtener una vista previa del audio, ya que hay una conexión física entre la tarjeta sintonizadora y la tarjeta de sonido.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-117">Contrary to what you might expect, no audio capture filter or audio renderer is required to preview the audio, because there is a physical connection between the tuner card and the sound card.</span></span>

 

<span data-ttu-id="e2a5e-118">En el código siguiente se muestran estos pasos con más detalle.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-118">The following code shows these steps in more detail.</span></span> <span data-ttu-id="e2a5e-119">En primer lugar, se trata de una función auxiliar que busca un filtro de cruz para un tipo de PIN especificado:</span><span class="sxs-lookup"><span data-stu-id="e2a5e-119">First, here is a helper function that searches a crossbar filter for a specified pin type:</span></span>


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



<span data-ttu-id="e2a5e-120">La función siguiente intenta activar o desactivar el audio, dependiendo del valor del parámetro *bActivate* .</span><span class="sxs-lookup"><span data-stu-id="e2a5e-120">The next function attempts to activate or mute the audio, depending on the value of the *bActivate* parameter.</span></span> <span data-ttu-id="e2a5e-121">Busca los pin necesarios en el filtro de barras cruzadas especificado.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-121">It searches the specified crossbar filter for the required pins.</span></span> <span data-ttu-id="e2a5e-122">Si no se encuentra, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-122">If it cannot find them, it returns an error code.</span></span>


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



<span data-ttu-id="e2a5e-123">La función siguiente busca un filtro de barras cruzadas en el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-123">The next function searches the filter graph for a crossbar filter.</span></span> <span data-ttu-id="e2a5e-124">Si encuentra uno, intenta activar o desactivar el audio (con la función anterior).</span><span class="sxs-lookup"><span data-stu-id="e2a5e-124">If it finds one, it attempts to activate or mute the audio (using the previous function).</span></span> <span data-ttu-id="e2a5e-125">Si se produce un error en esa operación, el método busca una segunda cruz y vuelve a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-125">If that operation fails, the method searches upstream for a second crossbar and tries again.</span></span> <span data-ttu-id="e2a5e-126">Para obtener un enfoque más generalizado para administrar varios filtros de barras cruzadas en un gráfico, vea la clase CCrossbar en la aplicación de ejemplo AmCap.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-126">For a more generalized approach to managing multiple crossbar filters in a graph, see the CCrossbar class in the AmCap sample application.</span></span>


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



<span data-ttu-id="e2a5e-127">En el código siguiente se muestra cómo llamar a estas funciones:</span><span class="sxs-lookup"><span data-stu-id="e2a5e-127">The following code shows how to call these functions:</span></span>


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



<span data-ttu-id="e2a5e-128">Tenga en cuenta que estas funciones de ejemplo repiten muchas de las llamadas a funciones.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-128">Note that these example functions repeat many of the same function calls.</span></span> <span data-ttu-id="e2a5e-129">Por ejemplo, enumeran las barras cruzadas cada vez.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-129">For example, they enumerate the crossbar pins each time.</span></span> <span data-ttu-id="e2a5e-130">En una aplicación real, puede almacenar en caché parte de esta información.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-130">In a real application, you might cache some of this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2a5e-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2a5e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a5e-132">Audio analógico de televisión</span><span class="sxs-lookup"><span data-stu-id="e2a5e-132">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="e2a5e-133">Trabajar con barras cruzadas</span><span class="sxs-lookup"><span data-stu-id="e2a5e-133">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



