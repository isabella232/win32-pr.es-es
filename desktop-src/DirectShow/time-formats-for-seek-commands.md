---
description: Formatos de hora para comandos de búsqueda
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formatos de hora para comandos de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547126"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="5cad5-103">Formatos de hora para comandos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="5cad5-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="5cad5-104">Muchos de los métodos de la interfaz **IMediaSeeking** tienen parámetros que expresan valores de posición, como la posición actual o la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="5cad5-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="5cad5-105">De forma predeterminada, estos parámetros se expresan en unidades de 100 nanosegundos, también denominadas hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="5cad5-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="5cad5-106">Cualquier filtro que pueda buscar debe admitir búsquedas por tiempo de referencia.</span><span class="sxs-lookup"><span data-stu-id="5cad5-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="5cad5-107">Algunos filtros pueden buscar también en otras unidades de tiempo, como buscar un número de marco determinado o buscar un desplazamiento de byte determinado dentro de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="5cad5-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="5cad5-108">Cada una de estas unidades de tiempo se denomina formato de hora y se define mediante un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="5cad5-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="5cad5-109">Para obtener una lista de los formatos de hora definidos por DirectShow, consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="5cad5-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="5cad5-110">Los terceros también pueden definir GUID para los formatos de hora personalizados.</span><span class="sxs-lookup"><span data-stu-id="5cad5-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="5cad5-111">Para determinar si los filtros que se encuentran actualmente en el gráfico de filtros admiten un formato de hora determinado, llame al método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="5cad5-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="5cad5-112">El método devuelve S \_ OK si se admite el formato.</span><span class="sxs-lookup"><span data-stu-id="5cad5-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="5cad5-113">De lo contrario, devuelve S \_ false o un código de error.</span><span class="sxs-lookup"><span data-stu-id="5cad5-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="5cad5-114">Si se admite un formato, puede cambiar a ese formato llamando al método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="5cad5-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="5cad5-115">Si el método **SetTimeFormat** se ejecuta correctamente, los comandos de búsqueda subsiguientes se expresan con el nuevo formato de hora.</span><span class="sxs-lookup"><span data-stu-id="5cad5-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="5cad5-116">En el ejemplo siguiente se comprueba si el grafo admite búsquedas por número de marco.</span><span class="sxs-lookup"><span data-stu-id="5cad5-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="5cad5-117">Si es así, busca el número de marco 20:</span><span class="sxs-lookup"><span data-stu-id="5cad5-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="5cad5-118">Tenga en cuenta que los formatos de hora solo se aplican a los comandos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5cad5-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="5cad5-119">No afectan a la reproducción de gráficos ni a otras acciones.</span><span class="sxs-lookup"><span data-stu-id="5cad5-119">They do not affect graph playback or other actions.</span></span>

 

 



