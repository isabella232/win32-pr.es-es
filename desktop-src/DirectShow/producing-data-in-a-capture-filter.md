---
description: En este tema se describe cómo un filtro de captura de DirectShow personalizado debe generar datos de salida.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Generar datos en un filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997893"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="c111c-103">Generar datos en un filtro de captura</span><span class="sxs-lookup"><span data-stu-id="c111c-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="c111c-104">En este tema se describe cómo un filtro de captura de DirectShow personalizado debe generar datos de salida.</span><span class="sxs-lookup"><span data-stu-id="c111c-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="c111c-105">Cambiar el estado de los cambios</span><span class="sxs-lookup"><span data-stu-id="c111c-105">Filter State Changes</span></span>

<span data-ttu-id="c111c-106">Un filtro de captura debe generar datos solo cuando se está ejecutando el filtro.</span><span class="sxs-lookup"><span data-stu-id="c111c-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="c111c-107">No envíe datos desde los pin cuando el filtro esté en pausa.</span><span class="sxs-lookup"><span data-stu-id="c111c-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="c111c-108">Además, devuelva la **\_ indicación VFW S \_ peralte \_** desde el método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) cuando el filtro esté en pausa.</span><span class="sxs-lookup"><span data-stu-id="c111c-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="c111c-109">Este valor devuelto informa al administrador de gráficos de filtro que no debe esperar ningún dato del filtro mientras el filtro está en pausa.</span><span class="sxs-lookup"><span data-stu-id="c111c-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="c111c-110">Para obtener más información, vea [filtrar Estados](filter-states.md).</span><span class="sxs-lookup"><span data-stu-id="c111c-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="c111c-111">En el código siguiente se muestra cómo implementar el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :</span><span class="sxs-lookup"><span data-stu-id="c111c-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="c111c-112">Controlar flujos individuales</span><span class="sxs-lookup"><span data-stu-id="c111c-112">Controlling Individual Streams</span></span>

<span data-ttu-id="c111c-113">Los pin de salida de un filtro de captura deben admitir la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , de modo que una aplicación pueda activar o desactivar cada pin individualmente.</span><span class="sxs-lookup"><span data-stu-id="c111c-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="c111c-114">Por ejemplo, una aplicación puede obtener una vista previa sin captura y, a continuación, cambiar al modo de captura sin volver a generar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="c111c-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="c111c-115">Puede usar la clase [**CBaseStreamControl**](cbasestreamcontrol.md) para implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="c111c-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="c111c-116">Marcas de tiempo</span><span class="sxs-lookup"><span data-stu-id="c111c-116">Time Stamps</span></span>

<span data-ttu-id="c111c-117">Cuando el filtro captura un ejemplo, marca de tiempo el ejemplo con la hora de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="c111c-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="c111c-118">La hora de finalización es la hora de inicio más la duración.</span><span class="sxs-lookup"><span data-stu-id="c111c-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="c111c-119">Por ejemplo, si el filtro captura a diez muestras por segundo y el tiempo de secuencia es de 200 millones unidades cuando el filtro captura el ejemplo, las marcas de tiempo deben ser 200 millones y 201 millones.</span><span class="sxs-lookup"><span data-stu-id="c111c-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="c111c-120">(Hay 10 millones unidades por segundo).</span><span class="sxs-lookup"><span data-stu-id="c111c-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="c111c-121">Para calcular el tiempo de transmisión, llame al método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener la hora de referencia actual y, a continuación, sustrato a la hora de inicio original.</span><span class="sxs-lookup"><span data-stu-id="c111c-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="c111c-122">También puede llamar al método [**CBaseFilter:: StreamTime**](cbasefilter-streamtime.md) , que realiza el mismo cálculo.</span><span class="sxs-lookup"><span data-stu-id="c111c-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="c111c-123">Para establecer la marca de tiempo en un ejemplo, llame al método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="c111c-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="c111c-124">Sin embargo, si el filtro tiene un PIN de vista previa, los ejemplos del PIN de vista previa no deben tener marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c111c-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="c111c-125">La razón es que los ejemplos siempre llegarán al representador ligeramente después del tiempo de captura.</span><span class="sxs-lookup"><span data-stu-id="c111c-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="c111c-126">Si los ejemplos tienen marca de tiempo, el representador los tratará como tardíos y puede intentar ponerse al día mediante la eliminación de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c111c-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="c111c-127">(Para obtener más información, consulte [filtros de captura de vídeo de DirectShow](directshow-video-capture-filters.md)). Tenga en cuenta que la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) requiere que el PIN realice un seguimiento de las horas de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c111c-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="c111c-128">En el caso de un PIN de vista previa, puede que tenga que modificar la implementación para que no se base en las marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c111c-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="c111c-129">Las marcas de tiempo siempre deben aumentar de una muestra a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="c111c-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="c111c-130">Esto es así incluso cuando el filtro se pausa.</span><span class="sxs-lookup"><span data-stu-id="c111c-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="c111c-131">Si el filtro se ejecuta, se detiene y, a continuación, se ejecuta de nuevo, el primer ejemplo después de la pausa debe tener una marca de tiempo mayor que la última muestra antes de la pausa.</span><span class="sxs-lookup"><span data-stu-id="c111c-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="c111c-132">En función de los datos que se van a capturar, puede ser conveniente establecer la hora del medio en los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c111c-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="c111c-133">Para obtener más información, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="c111c-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c111c-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c111c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c111c-135">Filtros de captura de vídeo de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c111c-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="c111c-136">Hora y relojes en DirectShow</span><span class="sxs-lookup"><span data-stu-id="c111c-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="c111c-137">Escribir filtros de captura</span><span class="sxs-lookup"><span data-stu-id="c111c-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



