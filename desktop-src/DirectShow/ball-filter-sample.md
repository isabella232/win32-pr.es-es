---
description: Ejemplo de filtro de bola
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Ejemplo de filtro de bola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906823"
---
# <a name="ball-filter-sample"></a><span data-ttu-id="16358-103">Ejemplo de filtro de bola</span><span class="sxs-lookup"><span data-stu-id="16358-103">Ball Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="16358-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="16358-104">Description</span></span>

<span data-ttu-id="16358-105">El filtro de bola es un filtro de origen de vídeo que genera una imagen de una bola de rebote.</span><span class="sxs-lookup"><span data-stu-id="16358-105">The Ball Filter is a video source filter that produces an image of a bouncing ball.</span></span> <span data-ttu-id="16358-106">Este ejemplo muestra la negociación de formato y el uso de las clases base de filtro de origen [**CSource**](csource.md) y [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="16358-106">This sample illustrates format negotiation and the use of the source filter base classes [**CSource**](csource.md) and [**CSourceStream**](csourcestream.md).</span></span>

<span data-ttu-id="16358-107">El código de Fball. h y Fball. cpp administra las interfaces de filtro.</span><span class="sxs-lookup"><span data-stu-id="16358-107">The code in Fball.h and Fball.cpp manages the filter interfaces.</span></span> <span data-ttu-id="16358-108">Estos dos archivos contienen aproximadamente el código mínimo necesario para un filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="16358-108">Those two files contain approximately the minimum code required for a source filter.</span></span> <span data-ttu-id="16358-109">Los archivos Ball. h y Ball. cpp contienen el código que rebota la bola.</span><span class="sxs-lookup"><span data-stu-id="16358-109">The Ball.h and Ball.cpp files contain the code that bounces the ball.</span></span>

<span data-ttu-id="16358-110">Este filtro tiene un solo PIN de salida, que proporciona un flujo de vídeo que muestra una bola que rebota en el fotograma.</span><span class="sxs-lookup"><span data-stu-id="16358-110">This filter has a single output pin, which provides a video stream that shows a ball bouncing around in the frame.</span></span> <span data-ttu-id="16358-111">El filtro Ball también acepta solicitudes de administración de calidad del filtro de nivel inferior, lo que muestra una estrategia de administración de calidad simple.</span><span class="sxs-lookup"><span data-stu-id="16358-111">The Ball filter also accepts quality management requests from the downstream filter, which illustrates a simple quality management strategy.</span></span> <span data-ttu-id="16358-112">Este filtro implementa la interfaz [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para ese propósito.</span><span class="sxs-lookup"><span data-stu-id="16358-112">This filter implements the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface for that purpose.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="16358-113">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="16358-113">Downloading the Sample</span></span>

<span data-ttu-id="16358-114">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="16358-114">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="16358-115">Este ejemplo se instala en la siguiente ruta de acceso: \[ ejemplos *raíz de SDK* \] \\ ejemplo de filtros de DirectShow de \\ multimedia \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="16358-115">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Ball.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16358-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16358-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16358-117">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="16358-117">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



