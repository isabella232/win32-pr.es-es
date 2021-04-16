---
description: In-Place procesamiento
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677161"
---
# <a name="in-place-processing"></a><span data-ttu-id="e6aac-103">In-Place procesamiento</span><span class="sxs-lookup"><span data-stu-id="e6aac-103">In-Place Processing</span></span>

<span data-ttu-id="e6aac-104">Ciertas transformaciones de datos se pueden realizar mediante la modificación directa de los datos.</span><span class="sxs-lookup"><span data-stu-id="e6aac-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="e6aac-105">Esto se denomina procesamiento *en contexto* .</span><span class="sxs-lookup"><span data-stu-id="e6aac-105">This is called *in-place* processing.</span></span> <span data-ttu-id="e6aac-106">Muchos efectos de audio y vídeo se pueden realizar de esta manera.</span><span class="sxs-lookup"><span data-stu-id="e6aac-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="e6aac-107">Si un DMO admite el procesamiento en contexto, expone la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) .</span><span class="sxs-lookup"><span data-stu-id="e6aac-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="e6aac-108">El procesamiento en contexto suele ser más eficaz que el uso de búferes independientes para la salida.</span><span class="sxs-lookup"><span data-stu-id="e6aac-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="e6aac-109">(Una excepción principal es cuando el búfer reside en la memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6aac-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="e6aac-110">En esta situación, las operaciones de lectura son mucho más lentas que las operaciones de escritura, por lo que no se recomienda el procesamiento en contexto).</span><span class="sxs-lookup"><span data-stu-id="e6aac-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="e6aac-111">Para procesar los datos en su lugar, el cliente realiza una llamada única al método [**IMediaObjectInPlace::P rador**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , en lugar de llamadas independientes a **ProcessInput** y **ProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="e6aac-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="e6aac-112">El método **Process** es sincrónico; todo el procesamiento se produce dentro de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e6aac-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="e6aac-113">Además, el procesamiento en contexto no usa objetos **IMediaBuffer** .</span><span class="sxs-lookup"><span data-stu-id="e6aac-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="e6aac-114">El método **Process** toma un puntero directamente al búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="e6aac-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="e6aac-115">Un DMO que admite el procesamiento en contexto todavía debe implementar la interfaz **IMediaObject** , incluidos los métodos **ProcessInput** y **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="e6aac-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="e6aac-116">El cliente puede elegir si desea usar el procesamiento en contexto o utilizar búferes independientes.</span><span class="sxs-lookup"><span data-stu-id="e6aac-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="e6aac-117">Sin embargo, no mezcle los dos tipos de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="e6aac-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="e6aac-118">Si llama al **proceso**, no llame a **ProcessInput** o **ProcessOutput** y viceversa.</span><span class="sxs-lookup"><span data-stu-id="e6aac-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="e6aac-119">**Colas de efectos**</span><span class="sxs-lookup"><span data-stu-id="e6aac-119">**Effect Tails**</span></span>

<span data-ttu-id="e6aac-120">Una DMO en contexto podría crear una salida adicional después de que la entrada se detenga.</span><span class="sxs-lookup"><span data-stu-id="e6aac-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="e6aac-121">Esto se denomina *cola de efectos*.</span><span class="sxs-lookup"><span data-stu-id="e6aac-121">This is called an *effect tail*.</span></span> <span data-ttu-id="e6aac-122">Por ejemplo, un efecto de reverberación continúa después de que la entrada alcance el silencio.</span><span class="sxs-lookup"><span data-stu-id="e6aac-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="e6aac-123">Si hay una cola de efectos, el método **Process** devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="e6aac-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="e6aac-124">Una vez que la aplicación ha procesado todos sus datos, puede generar la cola del efecto mediante el envío de búferes vacíos al método de **proceso** .</span><span class="sxs-lookup"><span data-stu-id="e6aac-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6aac-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6aac-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6aac-126">Hospedar directamente un DMO</span><span class="sxs-lookup"><span data-stu-id="e6aac-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



