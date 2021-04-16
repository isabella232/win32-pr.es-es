---
title: Para administrar la latencia del escritor
description: Para administrar la latencia del escritor
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Advanced Systems Format (ASF), administración de la latencia del escritor
- ASF (formato de sistemas avanzados), administración de la latencia del escritor
- Advanced Systems Format (ASF), latencia del escritor
- ASF (formato de sistemas avanzados), latencia del sistema de escritura
- latencia del escritor
- latency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685676"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="84c0b-109">Para administrar la latencia del escritor</span><span class="sxs-lookup"><span data-stu-id="84c0b-109">To Manage Writer Latency</span></span>

<span data-ttu-id="84c0b-110">El escritor tarda tiempo en procesar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="84c0b-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="84c0b-111">La cantidad de tiempo entre pasar una muestra de entrada y la escritura de un ejemplo de salida se denomina latencia del escritor.</span><span class="sxs-lookup"><span data-stu-id="84c0b-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="84c0b-112">Una serie de factores contribuye a la latencia del escritor y se puede reducir de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="84c0b-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="84c0b-113">El factor más obvio implicado en la latencia del escritor es el tiempo que se tarda en comprimir un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="84c0b-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="84c0b-114">En la mayoría de los casos, tendrá poco o ningún control sobre esto.</span><span class="sxs-lookup"><span data-stu-id="84c0b-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="84c0b-115">Si el ancho de banda no es una preocupación importante, puede reducir la latencia usando menos compresión.</span><span class="sxs-lookup"><span data-stu-id="84c0b-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="84c0b-116">Por supuesto, puede lograr la menor latencia pasando ejemplos que ya están comprimidos.</span><span class="sxs-lookup"><span data-stu-id="84c0b-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="84c0b-117">El siguiente factor, y otro sobre el que normalmente tiene el control, es el orden en el que se pasan los ejemplos al lector.</span><span class="sxs-lookup"><span data-stu-id="84c0b-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="84c0b-118">Puede lograr una mejor latencia si pasa las muestras en orden de tiempo de presentación y garantiza que los ejemplos de entrada estén bien sincronizados entre todos los flujos de entrada.</span><span class="sxs-lookup"><span data-stu-id="84c0b-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="84c0b-119">Cuanto mayor sea la discrepancia en el momento de la presentación entre los ejemplos de flujos diferentes, mayor será la latencia.</span><span class="sxs-lookup"><span data-stu-id="84c0b-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="84c0b-120">Puede establecer un máximo para la discrepancia entre los ejemplos de entrada mediante una llamada a [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="84c0b-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84c0b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84c0b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84c0b-122">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="84c0b-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




