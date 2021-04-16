---
description: Agregar un origen
ms.assetid: 8c5d1050-a696-4a5d-be68-806420d0cd78
title: Agregar un origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee583cd8971c183f2e03b92f68e2d6ba555c41db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659295"
---
# <a name="adding-a-source"></a><span data-ttu-id="e6f5e-103">Agregar un origen</span><span class="sxs-lookup"><span data-stu-id="e6f5e-103">Adding a Source</span></span>

<span data-ttu-id="e6f5e-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="e6f5e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="e6f5e-105">Cree un objeto de origen de la misma manera que crea otros objetos Timeline.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-105">Create a source object the same way you create other timeline objects.</span></span> <span data-ttu-id="e6f5e-106">Sin embargo, antes de insertarlo en la escala de tiempo, debe especificar al menos las siguientes propiedades en el origen.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-106">Before inserting it into the timeline, however, you must specify at least the following properties on the source.</span></span>

-   <span data-ttu-id="e6f5e-107">Horas de inicio y detención, con respecto a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-107">The start and stop times, relative to the timeline.</span></span> <span data-ttu-id="e6f5e-108">Llame al método [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f5e-108">Call the [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) method.</span></span>
-   <span data-ttu-id="e6f5e-109">Archivo multimedia que se va a utilizar como origen.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-109">The media file to use as a source.</span></span> <span data-ttu-id="e6f5e-110">Llame al método [**IAMTimelineSrc:: SetMediaName**](iamtimelinesrc-setmedianame.md) con una cadena de caracteres anchos que represente el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-110">Call the [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) method with a wide-character string representing the name of the file.</span></span>
-   <span data-ttu-id="e6f5e-111">Horas de inicio y detención del medio, que son relativas al archivo original.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-111">The media start and stop times, which are relative to the original file.</span></span> <span data-ttu-id="e6f5e-112">Llame al método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f5e-112">Call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="e6f5e-113">Para obtener más información sobre las horas de los medios, consulte [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="e6f5e-113">For more information about media times, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="e6f5e-114">En el ejemplo siguiente, el clip de origen inicia cuatro segundos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-114">In the following example, the source clip starts four seconds into the file.</span></span> <span data-ttu-id="e6f5e-115">La duración del medio es de 10 segundos, dos veces la longitud de la duración de la escala de tiempo, lo que significa que el origen se reproducirá a la doble velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-115">The media duration is 10 seconds, twice the length of the timeline duration, meaning the source will play at twice normal speed.</span></span> <span data-ttu-id="e6f5e-116">Las unidades constantes se definen como 10 millones (10 ^ 7) y es igual a un segundo.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-116">The constant UNITS is defined as 10000000 (10^7) and equals one second.</span></span>


```C++
pSourceObj->SetStartStop(0, 50000000)
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.avi"), 15);
pSource->SetMediaName(bstrFile); 
SysFreeString(bstrFile);
pSource->SetMediaTimes(40000000, 140000000);
```



> [!Note]  
> <span data-ttu-id="e6f5e-117">Actualmente, DES no puede representar simultáneamente más de 75 orígenes que se comprimieron con códecs de administrador de compresión de vídeo (VCM).</span><span class="sxs-lookup"><span data-stu-id="e6f5e-117">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="e6f5e-118">Además, si el proyecto como un conjunto contiene más de 75 tales orígenes, debe usar reconexión dinámica o DES no puede obtener una vista previa del proyecto.</span><span class="sxs-lookup"><span data-stu-id="e6f5e-118">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="e6f5e-119">Para obtener más información, vea [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="e6f5e-119">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

 

<span data-ttu-id="e6f5e-120">Para obtener más información sobre los orígenes, vea [trabajar con orígenes](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="e6f5e-120">For more information about sources, see [Working with Sources](working-with-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6f5e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6f5e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6f5e-122">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="e6f5e-122">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



