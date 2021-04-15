---
description: Recopilar información de Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Recopilar información de Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666109"
---
# <a name="collecting-fine-tuning-information"></a><span data-ttu-id="6aab6-103">Recopilar información de Fine-Tuning</span><span class="sxs-lookup"><span data-stu-id="6aab6-103">Collecting Fine-Tuning Information</span></span>

<span data-ttu-id="6aab6-104">Aunque generalmente se espera que las frecuencias de cable sean exactas, las frecuencias de difusión se pueden ajustar o reducir verticalmente varios kHz en la estación de difusión para reducir las posibles interferencias con los canales vecinos.</span><span class="sxs-lookup"><span data-stu-id="6aab6-104">Although cable frequencies are generally expected to be exact, broadcast frequencies may be adjusted up or down several kHz by the broadcast station to reduce potential interference with neighboring channels.</span></span>

<span data-ttu-id="6aab6-105">Cuando el filtro de sintonizador de TV se sintoniza en un canal, busca la señal más precisa.</span><span class="sxs-lookup"><span data-stu-id="6aab6-105">When the TV Tuner filter tunes to a channel, it scans for the most precise signal.</span></span> <span data-ttu-id="6aab6-106">Para guardar esta información en el registro para las operaciones de optimización posteriores, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6aab6-106">To save this information in the registry for subsequent tuning operations, do the following:</span></span>

1.  <span data-ttu-id="6aab6-107">Llame a [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) para determinar el intervalo de entradas de frecuencia en la tabla de frecuencia actual.</span><span class="sxs-lookup"><span data-stu-id="6aab6-107">Call [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) to determine the range of frequency entries in the current frequency table.</span></span>
2.  <span data-ttu-id="6aab6-108">Llame al método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) una vez para cada índice de frecuencia del intervalo.</span><span class="sxs-lookup"><span data-stu-id="6aab6-108">Call the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method once for each frequency index in the range.</span></span>
3.  <span data-ttu-id="6aab6-109">Llame a [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para guardar la información de ajuste en el registro.</span><span class="sxs-lookup"><span data-stu-id="6aab6-109">Call [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) to save the fine-tuning information in the registry.</span></span> <span data-ttu-id="6aab6-110">La información se almacena en la clave del registro para el espacio de optimización actual.</span><span class="sxs-lookup"><span data-stu-id="6aab6-110">The information is stored under the registry key for the current tuning space.</span></span>

<span data-ttu-id="6aab6-111">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6aab6-111">The following code shows these steps:</span></span>


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



<span data-ttu-id="6aab6-112">Con las versiones anteriores del filtro de sintonizador de TV, se recomendó el método [**IAMTVTuner:: AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) para ajustarse.</span><span class="sxs-lookup"><span data-stu-id="6aab6-112">With earlier versions of the TV Tuner filter, the [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method was recommended for fine-tuning.</span></span> <span data-ttu-id="6aab6-113">Sin embargo, este método omite cualquier invalidación de frecuencia, por lo que ya no se recomienda su uso.</span><span class="sxs-lookup"><span data-stu-id="6aab6-113">However, this method ignores any frequency overrides, so its use is no longer recommended.</span></span> <span data-ttu-id="6aab6-114">El código siguiente es equivalente al método **AutoTune** , pero funciona correctamente con invalidaciones de frecuencia:</span><span class="sxs-lookup"><span data-stu-id="6aab6-114">The following code is equivalent to the **AutoTune** method, but works correctly with frequency overrides:</span></span>


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



<span data-ttu-id="6aab6-115">Con la recepción de difusión, no siempre es posible obtener un bloqueo horizontal, aunque se puede ver la imagen.</span><span class="sxs-lookup"><span data-stu-id="6aab6-115">With broadcast reception, it is not always possible to get a horizontal lock, although the picture is viewable.</span></span> <span data-ttu-id="6aab6-116">En estos casos, el hardware del sintonizador tendrá un bloqueo de frecuencia, pero el descodificador no tendrá un bloqueo horizontal.</span><span class="sxs-lookup"><span data-stu-id="6aab6-116">In these cases, the tuner hardware will have a frequency lock, but the decoder will not have horizontal lock.</span></span> <span data-ttu-id="6aab6-117">Esta condición se puede detectar al usar [**Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) o [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) examinando el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="6aab6-117">This condition can be detected when using [**put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) or [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) by examining the return code.</span></span>



| <span data-ttu-id="6aab6-118">Value</span><span class="sxs-lookup"><span data-stu-id="6aab6-118">Value</span></span>    | <span data-ttu-id="6aab6-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6aab6-119">Description</span></span>                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aab6-120">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="6aab6-120">S\_OK</span></span>    | <span data-ttu-id="6aab6-121">La operación de optimización se realizó correctamente y el sintonizador tenía un bloqueo de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="6aab6-121">The tune operation succeeded and the tuner got a frequency lock.</span></span>                                                                                                                          |
| <span data-ttu-id="6aab6-122">S \_ false</span><span class="sxs-lookup"><span data-stu-id="6aab6-122">S\_FALSE</span></span> | <span data-ttu-id="6aab6-123">No hubo errores durante la operación de optimización, pero el sintonizador no pudo obtener un bloqueo de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="6aab6-123">There were no errors during the tune operation, but the tuner was not able to get a frequency lock.</span></span> <span data-ttu-id="6aab6-124">Es muy improbable que haya un canal visible resultante de esta operación.</span><span class="sxs-lookup"><span data-stu-id="6aab6-124">It is highly unlikely that there is a viewable channel resulting from this operation.</span></span> |



 

<span data-ttu-id="6aab6-125">Cualquier otro código de retorno indica que se produjo algún error.</span><span class="sxs-lookup"><span data-stu-id="6aab6-125">Any other return code indicates that some error occurred.</span></span>

<span data-ttu-id="6aab6-126">Un valor devuelto de S \_ OK no garantiza que el descodificador tenga un bloqueo horizontal.</span><span class="sxs-lookup"><span data-stu-id="6aab6-126">A return value of S\_OK does not guarantee that the decoder has a horizontal lock.</span></span> <span data-ttu-id="6aab6-127">El método [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) actualiza el parámetro *FoundSignal* para indicar si se ha conseguido un bloqueo horizontal.</span><span class="sxs-lookup"><span data-stu-id="6aab6-127">The [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) method updates the *FoundSignal* parameter to indicate whether or not horizontal lock was achieved.</span></span> <span data-ttu-id="6aab6-128">El método [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) devuelve la misma información.</span><span class="sxs-lookup"><span data-stu-id="6aab6-128">The [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) method returns the same information.</span></span>

<span data-ttu-id="6aab6-129">Sin embargo, cuando el valor devuelto es \_ correcto, la aplicación tiene la opción de omitir el parámetro *FoundSignal* , porque el sintonizador informa de un bloqueo de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="6aab6-129">When the return value is S\_OK, however, the application has the option of ignoring the *FoundSignal* parameter, because the tuner is reporting a frequency lock.</span></span> <span data-ttu-id="6aab6-130">Existe la posibilidad de un bloqueo de frecuencia en el ruido, pero esta posibilidad se debe sopesar contra la posibilidad de omitir canales visibles.</span><span class="sxs-lookup"><span data-stu-id="6aab6-130">There is the possibility of a frequency lock on noise, but this possibility should be weighed against the possibility of skipping viewable channels.</span></span>

## <a name="registry-conversion"></a><span data-ttu-id="6aab6-131">Conversión del registro</span><span class="sxs-lookup"><span data-stu-id="6aab6-131">Registry Conversion</span></span>

<span data-ttu-id="6aab6-132">Para admitir invalidaciones de frecuencia, ha cambiado el formato interno de la clave del registro que contiene la información de ajuste.</span><span class="sxs-lookup"><span data-stu-id="6aab6-132">To support frequency overrides, the internal format of the registry key that holds fine-tuning information has changed.</span></span> <span data-ttu-id="6aab6-133">El formato original todavía se admite por compatibilidad con versiones anteriores, pero no admite invalidaciones de frecuencia.</span><span class="sxs-lookup"><span data-stu-id="6aab6-133">The original format is still supported for backward compatibility, but it does not support frequency overrides.</span></span>

<span data-ttu-id="6aab6-134">El formato del registro anterior se convierte al nuevo formato siempre que se llama al método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) .</span><span class="sxs-lookup"><span data-stu-id="6aab6-134">The old registry format is converted to the new format whenever the [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) method is called.</span></span> <span data-ttu-id="6aab6-135">Si la aplicación agrega invalidaciones de frecuencia, debe llamar al método **StoreAutoTune** para convertir al nuevo formato del registro.</span><span class="sxs-lookup"><span data-stu-id="6aab6-135">If your application adds frequency overrides, it should call the **StoreAutoTune** method to convert to the new registry format.</span></span> <span data-ttu-id="6aab6-136">No es necesario recopilar información de ajuste preciso antes de llamar a **StoreAutoTune**.</span><span class="sxs-lookup"><span data-stu-id="6aab6-136">It is not necessary to collect any fine-tuning information before calling **StoreAutoTune**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6aab6-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6aab6-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aab6-138">Ajuste de TV analógica internacional</span><span class="sxs-lookup"><span data-stu-id="6aab6-138">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



