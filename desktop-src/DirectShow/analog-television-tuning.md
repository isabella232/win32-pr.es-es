---
description: Optimización de televisión analógica
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Optimización de televisión analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659291"
---
# <a name="analog-television-tuning"></a><span data-ttu-id="1fd39-103">Optimización de televisión analógica</span><span class="sxs-lookup"><span data-stu-id="1fd39-103">Analog Television Tuning</span></span>

<span data-ttu-id="1fd39-104">La optimización se controla mediante el filtro de sintonizador de TV, a través de la interfaz [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="1fd39-104">Tuning is controlled by the TV Tuner filter, through the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="1fd39-105">La interfaz IAMTVTuner hereda IAMTuner.</span><span class="sxs-lookup"><span data-stu-id="1fd39-105">The IAMTVTuner interface inherits IAMTuner.</span></span> <span data-ttu-id="1fd39-106">Para obtener un puntero a la interfaz, llame al método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="1fd39-106">To obtain a pointer to the interface, call the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method as follows:</span></span>


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



<span data-ttu-id="1fd39-107">El primer parámetro indica que se busque en el flujo ascendente desde el filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="1fd39-107">The first parameter indicates to search upstream from the capture filter.</span></span>

<span data-ttu-id="1fd39-108">Tablas de frecuencia</span><span class="sxs-lookup"><span data-stu-id="1fd39-108">Frequency Tables</span></span>

<span data-ttu-id="1fd39-109">Internamente, el filtro de sintonizador de TV mantiene una lista de tablas de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1fd39-109">Internally, the TV Tuner filter keeps a list of frequency tables.</span></span> <span data-ttu-id="1fd39-110">Cada tabla de frecuencia corresponde a las frecuencias de difusión o de cable para un país o región determinados.</span><span class="sxs-lookup"><span data-stu-id="1fd39-110">Each frequency table corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="1fd39-111">También hay una tabla de frecuencias genérica "Unicable", que se usa cuando un país o región no tiene un conjunto estándar de asignaciones de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1fd39-111">There is also a generic "Unicable" frequency table, which is used when a country/region does not have a standard set of frequency assignments.</span></span>

<span data-ttu-id="1fd39-112">Cada tabla de frecuencia contiene una lista de frecuencias de optimización.</span><span class="sxs-lookup"><span data-stu-id="1fd39-112">Each frequency table contains a list of tuning frequencies.</span></span> <span data-ttu-id="1fd39-113">En algunos países o regiones, los índices de la tabla se corresponden directamente con los números de canal; es decir, la frecuencia de canal n es la entrada n de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1fd39-113">For some countries/regions, the indexes in the table correspond directly to channel numbers — in other words, the frequency for channel n is the n th entry in the table.</span></span> <span data-ttu-id="1fd39-114">Sin embargo, para algunos países o regiones, no hay ninguna correspondencia directa entre los números de canal y las frecuencias.</span><span class="sxs-lookup"><span data-stu-id="1fd39-114">For some countries/regions, however, there is no direct correspondence between channel numbers and frequencies.</span></span> <span data-ttu-id="1fd39-115">En ese caso, la aplicación debe mantener una lista que asigne los números de canal (normalmente elegidos por el usuario) a las entradas de la tabla de frecuencias.</span><span class="sxs-lookup"><span data-stu-id="1fd39-115">In that case, the application must keep a list that maps channel numbers (typically chosen by the user) to frequency table entries.</span></span> <span data-ttu-id="1fd39-116">Por ejemplo, lo que el usuario ve como "canal 5" podría ser el número de entrada 12 en la tabla de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1fd39-116">For example, what the user sees as "channel 5" might be entry number 12 in the frequency table.</span></span>

<span data-ttu-id="1fd39-117">Para obtener más información, consulte Ajuste de la [televisión analógica internacional](international-analog-tv-tuning.md).</span><span class="sxs-lookup"><span data-stu-id="1fd39-117">For details, see [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span>

<span data-ttu-id="1fd39-118">Operaciones básicas de optimización</span><span class="sxs-lookup"><span data-stu-id="1fd39-118">Basic Tuning Operations</span></span>

<span data-ttu-id="1fd39-119">Si el sintonizador admite varios modos de recepción, como televisión y radio FM, llame a [**IAMTuner::p \_ modo UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) para seleccionar el modo.</span><span class="sxs-lookup"><span data-stu-id="1fd39-119">If the tuner supports multiple reception modes, such as television and FM radio, call [**IAMTuner::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) to select the mode.</span></span> <span data-ttu-id="1fd39-120">El método [**IAMTuner:: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) devuelve todos los modos que admite el sintonizador.</span><span class="sxs-lookup"><span data-stu-id="1fd39-120">The [**IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) method returns all of the modes that the tuner supports.</span></span> <span data-ttu-id="1fd39-121">Por ejemplo, el código siguiente comprueba si el sintonizador admite radio FM y, en ese caso, cambia a ese modo.</span><span class="sxs-lookup"><span data-stu-id="1fd39-121">For example, the following code checks whether the tuner supports FM radio, and if so, switches to that mode.</span></span>


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



<span data-ttu-id="1fd39-122">Para establecer el país o la región, llame al método [**IAMTuner: \_ :p**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) el método CountryCode.</span><span class="sxs-lookup"><span data-stu-id="1fd39-122">To set the country/region, call the [**IAMTuner::put\_CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) method.</span></span> <span data-ttu-id="1fd39-123">El sintonizador usa este valor para seleccionar la tabla de frecuencias adecuada.</span><span class="sxs-lookup"><span data-stu-id="1fd39-123">The tuner uses this value to select the appropriate frequency table.</span></span> <span data-ttu-id="1fd39-124">Para obtener más información [, consulte asignaciones de país o región](country-region-assignments.md) .</span><span class="sxs-lookup"><span data-stu-id="1fd39-124">See [Country/Region Assignments](country-region-assignments.md) for more information.</span></span>

<span data-ttu-id="1fd39-125">Para establecer el canal, llame al método [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) .</span><span class="sxs-lookup"><span data-stu-id="1fd39-125">To set the channel, call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method.</span></span> <span data-ttu-id="1fd39-126">El argumento para este método no es realmente un número de canal, sino un índice en la tabla de frecuencia actual.</span><span class="sxs-lookup"><span data-stu-id="1fd39-126">The argument to this method is actually not a channel number, but rather an index into the current frequency table.</span></span> <span data-ttu-id="1fd39-127">Tal y como se ha descrito anteriormente, el número de índice puede corresponderse o no a un número de canal.</span><span class="sxs-lookup"><span data-stu-id="1fd39-127">As described previously, the index number may or may not correspond to a channel number.</span></span> <span data-ttu-id="1fd39-128">El método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) devuelve los valores de índice mínimo y máximo de la tabla de frecuencias actual.</span><span class="sxs-lookup"><span data-stu-id="1fd39-128">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method returns the minimum and maximum index values for the current frequency table.</span></span>

<span data-ttu-id="1fd39-129">Invalidar entradas de frecuencia</span><span class="sxs-lookup"><span data-stu-id="1fd39-129">Overriding Frequency Entries</span></span>

<span data-ttu-id="1fd39-130">Es posible que algunas entradas de las tablas de frecuencia sean incorrectas o estén obsoletas.</span><span class="sxs-lookup"><span data-stu-id="1fd39-130">It is possible that some entries in the frequency tables might be incorrect or become obsolete.</span></span> <span data-ttu-id="1fd39-131">Por lo tanto, se proporciona un mecanismo para invalidar entradas individuales mediante las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="1fd39-131">Therefore, a mechanism is provided for overriding individual entries using registry keys.</span></span>

<span data-ttu-id="1fd39-132">En el tema sobre el ajuste de la [televisión analógica internacional](international-analog-tv-tuning.md), se explican los detalles.</span><span class="sxs-lookup"><span data-stu-id="1fd39-132">The specifics are explained in the topic [International Analog TV Tuning](international-analog-tv-tuning.md).</span></span> <span data-ttu-id="1fd39-133">Cada clave del registro define un "espacio de optimización" que contiene una o más subclaves.</span><span class="sxs-lookup"><span data-stu-id="1fd39-133">Each registry key defines a "tuning space" which contains one or more subkeys.</span></span> <span data-ttu-id="1fd39-134">Cada subclave invalida una entrada de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1fd39-134">Each subkey overrides one frequency entry.</span></span> <span data-ttu-id="1fd39-135">Para establecer el espacio de optimización actual, use el método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) .</span><span class="sxs-lookup"><span data-stu-id="1fd39-135">To set the current tuning space, use the [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method.</span></span> <span data-ttu-id="1fd39-136">Al activar el espacio de optimización, se invalidan las entradas de frecuencia en la tabla de frecuencia actual.</span><span class="sxs-lookup"><span data-stu-id="1fd39-136">Activating the tuning space overrides the frequency entries in the current frequency table.</span></span> <span data-ttu-id="1fd39-137">Por lo tanto, depende de la aplicación mantener una correspondencia entre los espacios de optimización y los países o regiones.</span><span class="sxs-lookup"><span data-stu-id="1fd39-137">Therefore, it is up to the application to maintain a correspondence between tuning spaces and countries/regions.</span></span> <span data-ttu-id="1fd39-138">El mejor enfoque es simplemente usar el identificador de país o región como nombre del espacio de optimización.</span><span class="sxs-lookup"><span data-stu-id="1fd39-138">The best approach is simply to use the country/region identifier as the name of the tuning space.</span></span>

<span data-ttu-id="1fd39-139">Ajustar las entradas de frecuencia</span><span class="sxs-lookup"><span data-stu-id="1fd39-139">Fine Tuning the Frequency Entries</span></span>

<span data-ttu-id="1fd39-140">La estación de difusión puede ajustar o reducir verticalmente varias frecuencias de difusión para reducir las posibles interferencias con canales vecinos.</span><span class="sxs-lookup"><span data-stu-id="1fd39-140">Broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span> <span data-ttu-id="1fd39-141">Dada la frecuencia nominal, la tarjeta sintonizadora puede buscar la frecuencia exacta.</span><span class="sxs-lookup"><span data-stu-id="1fd39-141">Given the nominal frequency, the tuner card can scan for the exact frequency.</span></span> <span data-ttu-id="1fd39-142">El filtro de sintonizador de TV tiene un mecanismo para guardar las frecuencias ajustadas en el registro.</span><span class="sxs-lookup"><span data-stu-id="1fd39-142">The TV Tuner filter has a mechanism for saving the adjusted frequencies in the registry.</span></span>

<span data-ttu-id="1fd39-143">Para cada entrada de la tabla Frequency, llame al \_ método put Channel para ajustarse a esa frecuencia.</span><span class="sxs-lookup"><span data-stu-id="1fd39-143">For each entry in the frequency table, call the put\_Channel method to tune to that frequency.</span></span> <span data-ttu-id="1fd39-144">El sintonizador buscará la frecuencia más precisa.</span><span class="sxs-lookup"><span data-stu-id="1fd39-144">The tuner will scan for the most precise frequency.</span></span> <span data-ttu-id="1fd39-145">Puede comprobar si el sintonizador ha logrado un bloqueo horizontal mediante una llamada a [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span><span class="sxs-lookup"><span data-stu-id="1fd39-145">You can check whether the tuner achieved a horizontal lock by calling [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent).</span></span> <span data-ttu-id="1fd39-146">El filtro de sintonizador de TV también almacena el resultado internamente.</span><span class="sxs-lookup"><span data-stu-id="1fd39-146">The TV Tuner filter also stores the result internally.</span></span>

<span data-ttu-id="1fd39-147">Después de examinar todas las frecuencias, llame al método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para escribir los valores actualizados en el registro.</span><span class="sxs-lookup"><span data-stu-id="1fd39-147">After scanning all of the frequencies, call the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method to write the updated values into the registry.</span></span> <span data-ttu-id="1fd39-148">Los valores actualizados se almacenan en la entrada del registro para el espacio de optimización actual.</span><span class="sxs-lookup"><span data-stu-id="1fd39-148">The updated values are stored under the registry entry for the current tuning space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd39-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fd39-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd39-150">Televisión analógica</span><span class="sxs-lookup"><span data-stu-id="1fd39-150">Analog Television</span></span>](analog-television.md)
</dt> </dl>

 

 



