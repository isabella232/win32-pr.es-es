---
title: Para obtener las estadísticas de rendimiento del lector
description: Para obtener las estadísticas de rendimiento del lector
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- Advanced Systems Format (ASF), estadísticas de rendimiento de lector
- ASF (formato de sistemas avanzados), estadísticas de rendimiento de lector
- Advanced Systems Format (ASF), lectores asincrónicos
- ASF (formato de sistemas avanzados), lectores asincrónicos
- Advanced Systems Format (ASF), estadísticas de rendimiento
- ASF (formato de sistemas avanzados), estadísticas de rendimiento
- lectores asincrónicos, estadísticas de rendimiento
- rendimiento, estadísticas de lector
- rendimiento, lectores asincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904402"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="0ff57-112">Para obtener las estadísticas de rendimiento del lector</span><span class="sxs-lookup"><span data-stu-id="0ff57-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="0ff57-113">Al leer archivos localmente con el lector asincrónico, no es necesario comprobar el rendimiento de las operaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="0ff57-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="0ff57-114">Sin embargo, si la aplicación lee desde una fuente de streaming, las estadísticas de rendimiento pueden ser muy importantes.</span><span class="sxs-lookup"><span data-stu-id="0ff57-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="0ff57-115">La aplicación puede responder a los cambios en el rendimiento de la reproducción para garantizar la mejor experiencia posible del usuario final.</span><span class="sxs-lookup"><span data-stu-id="0ff57-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="0ff57-116">La información de rendimiento que puede recuperar del lector incluye las estadísticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="0ff57-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="0ff57-117">Ancho de banda actual de la conexión.</span><span class="sxs-lookup"><span data-stu-id="0ff57-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="0ff57-118">El número de paquetes recibidos del servidor.</span><span class="sxs-lookup"><span data-stu-id="0ff57-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="0ff57-119">El número de paquetes perdidos que se han recuperado.</span><span class="sxs-lookup"><span data-stu-id="0ff57-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="0ff57-120">El número de paquetes perdidos que no se recuperaron.</span><span class="sxs-lookup"><span data-stu-id="0ff57-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="0ff57-121">El porcentaje del número total de paquetes enviados que se han recibido.</span><span class="sxs-lookup"><span data-stu-id="0ff57-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="0ff57-122">Para obtener las estadísticas de rendimiento del lector, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ff57-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="0ff57-123">Antes de iniciar la reproducción, cree una estructura de [**\_ \_ estadísticas del lector de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) .</span><span class="sxs-lookup"><span data-stu-id="0ff57-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="0ff57-124">Debe establecer el miembro **cbSize** en sizeof ( \_ estadísticas del lector de WM \_ ).</span><span class="sxs-lookup"><span data-stu-id="0ff57-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="0ff57-125">Obtenga un puntero a la interfaz [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) del objeto lector llamando a **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="0ff57-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="0ff57-126">Durante la reproducción, realice llamadas a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) con frecuencia para supervisar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0ff57-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="0ff57-127">Pase la estructura de las **\_ \_ estadísticas del lector de WM** con cada llamada y examine los miembros adecuados.</span><span class="sxs-lookup"><span data-stu-id="0ff57-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ff57-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ff57-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ff57-129">**Leer archivos con el lector asincrónico**</span><span class="sxs-lookup"><span data-stu-id="0ff57-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




