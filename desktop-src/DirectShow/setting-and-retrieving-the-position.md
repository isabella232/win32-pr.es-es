---
description: Establecimiento y recuperación de la posición
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: Establecimiento y recuperación de la posición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805209"
---
# <a name="setting-and-retrieving-the-position"></a><span data-ttu-id="d5ecf-103">Establecimiento y recuperación de la posición</span><span class="sxs-lookup"><span data-stu-id="d5ecf-103">Setting and Retrieving the Position</span></span>

<span data-ttu-id="d5ecf-104">El gráfico de filtro mantiene dos valores de posición: posición actual y posición de detención.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-104">The filter graph maintains two position values, current position and stop position.</span></span> <span data-ttu-id="d5ecf-105">Se definen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="d5ecf-105">These are defined as follows:</span></span>

-   <span data-ttu-id="d5ecf-106">Cuando se está ejecutando el gráfico, la posición actual es la posición de reproducción actual, con respecto al principio del origen.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-106">When the graph is running, the current position is the current playback position, relative to the beginning of the source.</span></span> <span data-ttu-id="d5ecf-107">Cuando el gráfico está detenido o en pausa, la posición actual es el punto en el que se iniciará la transmisión por secuencias en el siguiente comando de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-107">When the graph is stopped or paused, the current position is the point where streaming will begin on the next run command.</span></span>
-   <span data-ttu-id="d5ecf-108">La posición de detención es el punto en el que finalizará la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-108">The stop position is the point where the stream will end.</span></span> <span data-ttu-id="d5ecf-109">Cuando el gráfico llega a la posición de detención, no se transmiten más datos y el administrador de gráficos de filtros envía un evento de [**\_ finalización de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ecf-109">When the graph reaches the stop position, no more data is streamed, and the filter graph manager posts an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="d5ecf-110">No obstante, el gráfico no cambia automáticamente a un estado detenido.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-110">(The graph does not automatically switch to a stopped state, however.</span></span> <span data-ttu-id="d5ecf-111">Para obtener más información, consulte [responder a eventos](responding-to-events.md)).</span><span class="sxs-lookup"><span data-stu-id="d5ecf-111">For more information, see [Responding to Events](responding-to-events.md).)</span></span>

<span data-ttu-id="d5ecf-112">Para recuperar estos valores, llame al método [**IMediaSeeking:: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="d5ecf-112">To retrieve these values, call the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span> <span data-ttu-id="d5ecf-113">Los valores devueltos siempre son relativos al origen multimedia original.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-113">The returned values are always relative to the original media source.</span></span> <span data-ttu-id="d5ecf-114">De forma predeterminada, los valores están en unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-114">By default, the values are in reference time units.</span></span> <span data-ttu-id="d5ecf-115">En algunos casos, puede cambiar las unidades de tiempo; para obtener más información, vea [formatos de hora para comandos de búsqueda](time-formats-for-seek-commands.md).</span><span class="sxs-lookup"><span data-stu-id="d5ecf-115">In some cases, you can change the time units; for more information, see [Time Formats For Seek Commands](time-formats-for-seek-commands.md).</span></span>

<span data-ttu-id="d5ecf-116">Para buscar una nueva posición o establecer una nueva posición de detención, llame al método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) , como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5ecf-116">To seek to a new position or set a new stop position, call the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method, as shown in the following example:</span></span>


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> <span data-ttu-id="d5ecf-117">Un segundo es 10 millones unidades de tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-117">One second is 10,000,000 units of reference time.</span></span> <span data-ttu-id="d5ecf-118">Para mayor comodidad, en el ejemplo se define este valor en un \_ segundo.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-118">For convenience, the example defines this value as ONE\_SECOND.</span></span> <span data-ttu-id="d5ecf-119">Si usa la biblioteca de clases base de DirectShow, las unidades constantes tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-119">If you are using the DirectShow base-class library, the constant UNITS has the same value.</span></span>

 

<span data-ttu-id="d5ecf-120">El parámetro *rtNow* especifica la nueva posición actual.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-120">The *rtNow* parameter specifies the new current position.</span></span> <span data-ttu-id="d5ecf-121">El segundo parámetro es una marca que define cómo interpretar *rtNow*.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-121">The second parameter is a flag that defines how to interpret *rtNow*.</span></span> <span data-ttu-id="d5ecf-122">En este ejemplo, la \_ marca AM Seek \_ AbsolutePositioning indica que *rtNow* especifica una posición absoluta en el origen.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-122">In this example, the AM\_SEEKING\_AbsolutePositioning flag indicates that *rtNow* specifies an absolute position in the source.</span></span> <span data-ttu-id="d5ecf-123">Por lo tanto, el gráfico de filtros buscará una posición de dos segundos desde el inicio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-123">Therefore, the filter graph will seek to a position two seconds from the start of the stream.</span></span> <span data-ttu-id="d5ecf-124">El parámetro *rtStop* proporciona la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-124">The *rtStop* parameter gives the stop time.</span></span> <span data-ttu-id="d5ecf-125">El último parámetro especifica que *rtStop* también es una posición absoluta.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-125">The last parameter specifies that *rtStop* is also an absolute position.</span></span>

<span data-ttu-id="d5ecf-126">Para especificar una posición relativa al valor de posición anterior, use la \_ marca AM \_ RelativePositioning Seek.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-126">To specify a position relative to the previous position value, use the AM\_SEEKING\_RelativePositioning flag.</span></span> <span data-ttu-id="d5ecf-127">Para dejar uno de los valores de posición sin modificar, use la \_ marca AM buscar \_ nopositioning.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-127">To leave one of the position values unchanged, use the AM\_SEEKING\_NoPositioning flag.</span></span> <span data-ttu-id="d5ecf-128">En ese caso, el parámetro de hora correspondiente puede ser **null** .</span><span class="sxs-lookup"><span data-stu-id="d5ecf-128">The corresponding time parameter can be **NULL** in that case.</span></span> <span data-ttu-id="d5ecf-129">El siguiente ejemplo busca hacia delante 10 segundos pero deja la posición de detención sin cambios:</span><span class="sxs-lookup"><span data-stu-id="d5ecf-129">The following example seeks forward by 10 seconds but leaves the stop position unchanged:</span></span>


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



<span data-ttu-id="d5ecf-130">Si el gráfico de filtros se detiene, el representador de vídeo no actualiza la imagen después de una operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-130">If the filter graph is stopped, the video renderer does not update the image after a seek operation.</span></span> <span data-ttu-id="d5ecf-131">Para el usuario, aparecerá como si no se produjera la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-131">To the user, it will appear as if the seek did not happen.</span></span> <span data-ttu-id="d5ecf-132">Para actualizar la imagen, Pause el gráfico después de la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-132">To update the image, pause the graph after the seek operation.</span></span> <span data-ttu-id="d5ecf-133">Pausar las guías de gráficos un nuevo fotograma de vídeo para el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-133">Pausing the graph cues a new video frame for the video renderer.</span></span> <span data-ttu-id="d5ecf-134">Puede usar el método [**IMediaControl:: StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) , que pone en pausa el gráfico y, a continuación, lo detiene.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-134">You can use the [**IMediaControl::StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) method, which pauses the graph and then stops it.</span></span>

 

 



