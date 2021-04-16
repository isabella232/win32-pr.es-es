---
description: Ejemplo de filtro InfTee
ms.assetid: ba401528-9706-41fb-99d1-2bc3ffc05f1a
title: Ejemplo de filtro InfTee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0fc5a1d550e0327da0d0d3dd47c8847ffafee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677168"
---
# <a name="inftee-filter-sample"></a><span data-ttu-id="5b815-103">Ejemplo de filtro InfTee</span><span class="sxs-lookup"><span data-stu-id="5b815-103">InfTee Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="5b815-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b815-104">Description</span></span>

<span data-ttu-id="5b815-105">El filtro InfTee proporciona una implementación de ejemplo del filtro [tee de PIN infinitos](infinite-pin-tee-filter.md) de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5b815-105">The InfTee filter provides a sample implementation of the DirectShow [Infinite Pin Tee](infinite-pin-tee-filter.md) filter.</span></span> <span data-ttu-id="5b815-106">El filtro tiene un PIN de entrada y un número dinámico de clavijas de salida.</span><span class="sxs-lookup"><span data-stu-id="5b815-106">The filter has one input pin and a dynamic number of output pins.</span></span> <span data-ttu-id="5b815-107">Todos los ejemplos de medios enviados al filtro se entregan simultáneamente desde todos los pin de salida.</span><span class="sxs-lookup"><span data-stu-id="5b815-107">All media samples sent to the filter are delivered simultaneously from all of the output pins.</span></span>

<span data-ttu-id="5b815-108">Este filtro aparece en GraphEdit bajo el nombre "ejemplo infinita de PIN Tee" para distinguirlo del filtro Tee estándar de PIN infinito que se proporciona en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5b815-108">This filter appears in GraphEdit under the name "Sample Infinite Pin Tee," to distinguish it from the standard Infinite Pin Tee filter that is provided in DirectShow.</span></span>

## <a name="usage"></a><span data-ttu-id="5b815-109">Uso</span><span class="sxs-lookup"><span data-stu-id="5b815-109">Usage</span></span>

<span data-ttu-id="5b815-110">Dado que este filtro no cambia los datos que recibe, todos los pin deben aceptar el mismo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="5b815-110">Because this filter does not change the data that it receives, all pins must agree to the same media type.</span></span> <span data-ttu-id="5b815-111">Durante el proceso de conexión, el filtro podría volver a conectar algunos PIN para que los tipos de medios coincidan.</span><span class="sxs-lookup"><span data-stu-id="5b815-111">During the connection process, the filter might reconnect some pins in order to make the media types match.</span></span>

<span data-ttu-id="5b815-112">Los datos que llegan al pin de entrada no se copian antes de que se envíen a los pin de salida.</span><span class="sxs-lookup"><span data-stu-id="5b815-112">Data arriving at the input pin is not copied before it is sent to the output pins.</span></span> <span data-ttu-id="5b815-113">El filtro también garantiza que los datos se entreguen a los filtros de nivel inferior para garantizar que ambas salidas reciben el servicio puntualmente.</span><span class="sxs-lookup"><span data-stu-id="5b815-113">The filter also ensures that the data is delivered to the downstream filters, to guarantee that both outputs receive timely service.</span></span> <span data-ttu-id="5b815-114">En concreto, si una de las salidas puede bloquearse en la función miembro [**COutputQueue:: Receive**](coutputqueue-receive.md) , el tee gira un subproceso para entregar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5b815-114">In particular, if one of the outputs can block in the [**COutputQueue::Receive**](coutputqueue-receive.md) member function, then the tee spins off a thread to deliver the sample.</span></span> <span data-ttu-id="5b815-115">Si no hay ningún subproceso para entregar el ejemplo, el subproceso que entrega el ejemplo al pin de entrada Tee podría pasar los datos a un filtro de nivel inferior; en ese momento, podría bloquearse y mantener los datos del otro filtro de nivel inferior durante largos períodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="5b815-115">If there were no thread to deliver the sample, then the thread that delivers the sample to the tee input pin might pass the data to a downstream filter; at that point, it might block, keeping data from the other downstream filter for long periods of time.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="5b815-116">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b815-116">Downloading the Sample</span></span>

<span data-ttu-id="5b815-117">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5b815-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="5b815-118">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* \\ \\ filtros DirectShow de multimedia \\ \\ \\ InfTee.</span><span class="sxs-lookup"><span data-stu-id="5b815-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\InfTee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b815-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b815-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b815-120">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="5b815-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



