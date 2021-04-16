---
title: Seleccionar velocidades de bits
description: Seleccionar velocidades de bits
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- perfiles, elegir velocidades de bits
- perfiles, velocidades de bits
- códecs, elegir velocidades de bits
- códecs, velocidades de bits
- perfiles, seleccionar velocidades de bits
- códecs, seleccionar velocidades de bits
- velocidades de bits, seleccionar
- tasas de bits, perfiles
- velocidades de bits, códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356663"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="0bd7d-112">Seleccionar velocidades de bits</span><span class="sxs-lookup"><span data-stu-id="0bd7d-112">Selecting Bit Rates</span></span>

<span data-ttu-id="0bd7d-113">En el caso de los archivos que se transmitirán por secuencias a través de una red, debe considerar detenidamente qué tasas de bits debe usar.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="0bd7d-114">En la mayoría de los casos, puede Agregar las velocidades de bits de todas las secuencias de un archivo de forma conjunta para obtener una idea general del ancho de banda disponible necesario para transmitir el archivo.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="0bd7d-115">Sin embargo, también se requiere una determinada cantidad de sobrecarga para cada flujo.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="0bd7d-116">Esta sobrecarga se resume en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="0bd7d-117">Intervalo de velocidad de bits (kbps)</span><span class="sxs-lookup"><span data-stu-id="0bd7d-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="0bd7d-118">Ancho de banda adicional necesario para la sobrecarga (kbps)</span><span class="sxs-lookup"><span data-stu-id="0bd7d-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="0bd7d-119">de 10 a 16</span><span class="sxs-lookup"><span data-stu-id="0bd7d-119">10 – 16</span></span>               | <span data-ttu-id="0bd7d-120">3</span><span class="sxs-lookup"><span data-stu-id="0bd7d-120">3</span></span>                                                 |
| <span data-ttu-id="0bd7d-121">17 – 30</span><span class="sxs-lookup"><span data-stu-id="0bd7d-121">17 – 30</span></span>               | <span data-ttu-id="0bd7d-122">4</span><span class="sxs-lookup"><span data-stu-id="0bd7d-122">4</span></span>                                                 |
| <span data-ttu-id="0bd7d-123">31 – 45</span><span class="sxs-lookup"><span data-stu-id="0bd7d-123">31 – 45</span></span>               | <span data-ttu-id="0bd7d-124">5</span><span class="sxs-lookup"><span data-stu-id="0bd7d-124">5</span></span>                                                 |
| <span data-ttu-id="0bd7d-125">46 – 70</span><span class="sxs-lookup"><span data-stu-id="0bd7d-125">46 – 70</span></span>               | <span data-ttu-id="0bd7d-126">6</span><span class="sxs-lookup"><span data-stu-id="0bd7d-126">6</span></span>                                                 |
| <span data-ttu-id="0bd7d-127">71 – 225</span><span class="sxs-lookup"><span data-stu-id="0bd7d-127">71 – 225</span></span>              | <span data-ttu-id="0bd7d-128">7</span><span class="sxs-lookup"><span data-stu-id="0bd7d-128">7</span></span>                                                 |
| <span data-ttu-id="0bd7d-129">>225</span><span class="sxs-lookup"><span data-stu-id="0bd7d-129">>225</span></span>               | <span data-ttu-id="0bd7d-130">9</span><span class="sxs-lookup"><span data-stu-id="0bd7d-130">9</span></span>                                                 |



 

<span data-ttu-id="0bd7d-131">La sobrecarga normal necesaria para una secuencia no tiene en cuenta las extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="0bd7d-132">Cada extensión de unidad de datos se agrega al tamaño del ejemplo al que está adjunta.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="0bd7d-133">Dependiendo del tipo de extensión de unidad de datos, esto puede aumentar en gran medida la velocidad de bits de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="0bd7d-134">También debe tener en cuenta que el ancho de banda máximo teórico disponible a través de una conexión de red no es una velocidad de bits de destino práctica.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="0bd7d-135">El ancho de banda disponible promedio para una conexión determinada es muy breve de la capacidad de ancho de banda de la conexión, debido al tráfico de red y a muchos otros factores.</span><span class="sxs-lookup"><span data-stu-id="0bd7d-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bd7d-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bd7d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd7d-137">**Diseñar perfiles**</span><span class="sxs-lookup"><span data-stu-id="0bd7d-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




