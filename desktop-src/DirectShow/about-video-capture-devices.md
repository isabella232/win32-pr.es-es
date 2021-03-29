---
description: Acerca de los dispositivos de captura de vídeo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: Acerca de los dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805930"
---
# <a name="about-video-capture-devices"></a><span data-ttu-id="3c180-103">Acerca de los dispositivos de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3c180-103">About Video Capture Devices</span></span>

<span data-ttu-id="3c180-104">La mayoría de los dispositivos de captura de vídeo nuevos usan controladores Modelo de controlador de Windows (WDM).</span><span class="sxs-lookup"><span data-stu-id="3c180-104">Most new video capture devices use Windows Driver Model (WDM) drivers.</span></span> <span data-ttu-id="3c180-105">En la arquitectura de WDM, Microsoft proporciona un conjunto de controladores independientes del hardware, denominados controladores de clase, y el proveedor de hardware proporciona los minicontroladores específicos de hardware.</span><span class="sxs-lookup"><span data-stu-id="3c180-105">In the WDM architecture, Microsoft supplies a set of hardware-independent drivers, called class drivers, and the hardware vendor provides hardware-specific minidrivers.</span></span> <span data-ttu-id="3c180-106">Un minicontrolador implementa las funciones que son específicas del dispositivo; para la mayoría de las funciones, el minicontrolador llama al controlador de clases de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c180-106">A minidriver implements any functions that are specific to the device; for most functions, the minidriver calls the Microsoft class driver.</span></span>

<span data-ttu-id="3c180-107">En un gráfico de filtros de DirectShow, cualquier dispositivo de captura WDM aparece como el filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3c180-107">In a DirectShow filter graph, any WDM capture device appears as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="3c180-108">El filtro de captura de vídeo WDM se configura a sí mismo en función de las características del controlador.</span><span class="sxs-lookup"><span data-stu-id="3c180-108">The WDM Video Capture filter configures itself based on the characteristics of the driver.</span></span> <span data-ttu-id="3c180-109">Aparece bajo un nombre proporcionado por el controlador; no verá un filtro denominado "filtro de captura de vídeo WDM" en cualquier lugar del gráfico.</span><span class="sxs-lookup"><span data-stu-id="3c180-109">It appears under a name provided by the driver — you will not see a filter called "WDM Video Capture Filter" anywhere in the graph.</span></span>

<span data-ttu-id="3c180-110">Algunos dispositivos antiguos de captura siguen usando los controladores de vídeo para Windows (VFW).</span><span class="sxs-lookup"><span data-stu-id="3c180-110">Some older capture devices still use Video for Windows (VFW) drivers.</span></span> <span data-ttu-id="3c180-111">Aunque estos controladores están ahora obsoletos, se admiten en DirectShow a través del filtro de [captura VFW](vfw-capture-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3c180-111">Although these drivers are now obsolete, they are supported in DirectShow through the [VFW Capture](vfw-capture-filter.md) filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c180-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c180-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c180-113">Acerca de la captura de vídeo en DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c180-113">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



