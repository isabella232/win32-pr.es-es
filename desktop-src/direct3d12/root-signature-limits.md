---
title: Límites de la firma raíz
description: La firma raíz es una auténtica inmobiliaria y se deben tener en cuenta los límites y costos estrictos.
ms.assetid: 01121D3A-1926-4246-9C20-5E11F2E0B092
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25986da72cfcad7b714031e063341e1832d6ae68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104095"
---
# <a name="root-signature-limits"></a><span data-ttu-id="531a2-103">Límites de la firma raíz</span><span class="sxs-lookup"><span data-stu-id="531a2-103">Root Signature Limits</span></span>

<span data-ttu-id="531a2-104">La firma raíz es una auténtica inmobiliaria y se deben tener en cuenta los límites y costos estrictos.</span><span class="sxs-lookup"><span data-stu-id="531a2-104">The root signature is prime real estate, and there are strict limits and costs to consider.</span></span>

-   [<span data-ttu-id="531a2-105">Límites de memoria y costos</span><span class="sxs-lookup"><span data-stu-id="531a2-105">Memory limits and costs</span></span>](#memory-limits-and-costs)
-   [<span data-ttu-id="531a2-106">Costos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="531a2-106">Performance costs</span></span>](#performance-costs)
-   [<span data-ttu-id="531a2-107">Muestras estáticas</span><span class="sxs-lookup"><span data-stu-id="531a2-107">Static samplers</span></span>](#static-samplers)
-   [<span data-ttu-id="531a2-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="531a2-108">Related topics</span></span>](#related-topics)

## <a name="memory-limits-and-costs"></a><span data-ttu-id="531a2-109">Límites de memoria y costos</span><span class="sxs-lookup"><span data-stu-id="531a2-109">Memory limits and costs</span></span>

<span data-ttu-id="531a2-110">El tamaño máximo de una firma raíz es 64 DWORDs.</span><span class="sxs-lookup"><span data-stu-id="531a2-110">The maximum size of a root signature is 64 DWORDs.</span></span>

<span data-ttu-id="531a2-111">Este tamaño máximo se elige para evitar el abuso de la firma raíz como una forma de almacenar los datos en bloque.</span><span class="sxs-lookup"><span data-stu-id="531a2-111">This maximum size is chosen to prevent abuse of the root signature as a way of storing bulk data.</span></span> <span data-ttu-id="531a2-112">Cada entrada de la firma raíz tiene un costo para este límite de DWORD 64:</span><span class="sxs-lookup"><span data-stu-id="531a2-112">Each entry in the root signature has a cost towards this 64 DWORD limit:</span></span>

-   <span data-ttu-id="531a2-113">Las tablas de descriptores tienen el costo 1 DWORD cada una.</span><span class="sxs-lookup"><span data-stu-id="531a2-113">Descriptor tables cost 1 DWORD each.</span></span>
-   <span data-ttu-id="531a2-114">Las constantes raíz cuestan 1 DWORD cada una, ya que son valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="531a2-114">Root constants cost 1 DWORD each, since they are 32-bit values.</span></span>
-   <span data-ttu-id="531a2-115">Los descriptores raíz (direcciones virtuales de GPU de 64 bits) cuestan 2 DWORDs cada uno.</span><span class="sxs-lookup"><span data-stu-id="531a2-115">Root descriptors (64-bit GPU virtual addresses) cost 2 DWORDs each.</span></span>

<span data-ttu-id="531a2-116">Los muestreadores estáticos no tienen ningún costo en el tamaño de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="531a2-116">Static samplers do not have any cost in the size of the root signature.</span></span>

## <a name="performance-costs"></a><span data-ttu-id="531a2-117">Costos de rendimiento</span><span class="sxs-lookup"><span data-stu-id="531a2-117">Performance costs</span></span>

<span data-ttu-id="531a2-118">El costo de rendimiento (en términos de niveles de direccionamiento indirecto) es cero para una constante raíz, 1 para un descriptor raíz y 2 para una tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="531a2-118">The performance cost (in terms of levels of indirection) are zero for a root constant, 1 for a root descriptor, and 2 for a descriptor table.</span></span> <span data-ttu-id="531a2-119">Si una firma raíz es grande y se desborda de la memoria más rápida en una memoria ligeramente más lenta (lo que puede ocurrir en algún hardware), agregue 1 al costo de rendimiento de los elementos de desbordamiento al final de la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="531a2-119">If a root signature is large and overflows out of the fastest memory into slightly slower memory (which can happen on some hardware), then add 1 to the performance cost for the overflowing items at the end of the root signature.</span></span>

<span data-ttu-id="531a2-120">Se puede producir un desbordamiento en el hardware que podría tener, por ejemplo, un tamaño fijo de 16 DWORD para el espacio del argumento raíz.</span><span class="sxs-lookup"><span data-stu-id="531a2-120">An overflow can occur on hardware that might have, for example, a fixed size of 16 DWORDs for root argument space.</span></span> <span data-ttu-id="531a2-121">Este límite puede reducirse aún más en uno si se utiliza el ensamblador de entrada.</span><span class="sxs-lookup"><span data-stu-id="531a2-121">This limit might be further reduced by one if the Input Assembler is used.</span></span> <span data-ttu-id="531a2-122">En este caso, se produce un desbordamiento en la memoria ligeramente más lenta si la firma raíz es demasiado grande para la memoria nativa de 15 o 16 DWORD.</span><span class="sxs-lookup"><span data-stu-id="531a2-122">In this case there is overflow into slightly slower memory if the root signature is too large for the 15 or 16 DWORD native memory.</span></span> <span data-ttu-id="531a2-123">En otro hardware no existe memoria de argumentos raíz nativa fija (por lo que la situación de desbordamiento nunca se produce).</span><span class="sxs-lookup"><span data-stu-id="531a2-123">In other hardware there is no fixed native root argument memory (so the overflow situation never occurs).</span></span>

<span data-ttu-id="531a2-124">En todo el hardware, si algún argumento raíz cambia, el controlador debe mantener una versión de todos los argumentos raíz (a diferencia de otro almacenamiento como los montones de descriptor y los recursos de búfer, que no son versiones del controlador).</span><span class="sxs-lookup"><span data-stu-id="531a2-124">For all hardware, if any root argument changes, the driver must maintain a version of all the root arguments (unlike other storage such as descriptor heaps and buffer resources, which are not versioned by the driver).</span></span> <span data-ttu-id="531a2-125">En el hardware en el que se produce una situación de desbordamiento, solo es necesario crear versiones del área nativa o de desbordamiento, en función de dónde se haya producido el cambio.</span><span class="sxs-lookup"><span data-stu-id="531a2-125">In hardware that an overflow situation occurs, only the native or overflow area needs to be versioned, depending on where the change occurred.</span></span> <span data-ttu-id="531a2-126">Obviamente, la cantidad de versiones debe mantenerse en el mínimo necesario.</span><span class="sxs-lookup"><span data-stu-id="531a2-126">The amount of versioning should obviously be kept to the necessary minimum.</span></span>

<span data-ttu-id="531a2-127">En general, tenga en cuenta las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="531a2-127">Generally, consider the following guidelines:</span></span>

-   <span data-ttu-id="531a2-128">Use una firma raíz pequeña según sea necesario, pero equilibre esto con la flexibilidad de una firma raíz más grande.</span><span class="sxs-lookup"><span data-stu-id="531a2-128">Use a small a root signature as necessary, though balance this with the flexibility of a larger root signature.</span></span>
-   <span data-ttu-id="531a2-129">Organice los parámetros en una firma raíz de gran tamaño para que los parámetros con más probabilidades de cambiar con frecuencia, o si la latencia de acceso bajo para un parámetro determinado es importante, se produzca primero.</span><span class="sxs-lookup"><span data-stu-id="531a2-129">Arrange parameters in a large root signature so that the parameters most likely to change often, or if low access latency for a given parameter is important, occur first.</span></span>
-   <span data-ttu-id="531a2-130">Si es conveniente, use constantes raíz o vistas de búfer de constantes raíz en lugar de colocar vistas de búfer constantes en un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="531a2-130">If convenient, use root constants or root constant buffer views over putting constant buffer views in a descriptor heap.</span></span>

## <a name="static-samplers"></a><span data-ttu-id="531a2-131">Muestras estáticas</span><span class="sxs-lookup"><span data-stu-id="531a2-131">Static samplers</span></span>

<span data-ttu-id="531a2-132">Los muestreadores estáticos (muestreadores en los que el estado es totalmente definido e inmutable) forman parte de las firmas raíz, pero no cuentan para el límite DWORD 64.</span><span class="sxs-lookup"><span data-stu-id="531a2-132">Static samplers (samplers where the state is fully defined and immutable) are part of root signatures, but do not count towards the 64 DWORD limit.</span></span> <span data-ttu-id="531a2-133">Si una muestra se puede definir como estática, no es necesario que la muestra forme parte de un montón de descriptores.</span><span class="sxs-lookup"><span data-stu-id="531a2-133">If a sampler can be defined as static, there is no need for the sampler to be part of a descriptor heap.</span></span>

<span data-ttu-id="531a2-134">El uso de muestras estáticas no supone ningún costo de rendimiento, y una firma raíz puede contener una combinación de muestras estáticas (almacenadas en la firma raíz o en espacio reservado en algún hardware) y muestreadores dinámicos (almacenados en un montón de descriptores de muestra).</span><span class="sxs-lookup"><span data-stu-id="531a2-134">There is no performance cost to using static samplers, and a root signature can contain a mix of static samplers (stored in the root signature, or in reserved space on some hardware) and dynamic samplers (stored in a sampler descriptor heap).</span></span> <span data-ttu-id="531a2-135">Los muestreadores de un montón de descriptores se pueden asignar y indexar dinámicamente, lo que los ejemplos estáticos no pueden.</span><span class="sxs-lookup"><span data-stu-id="531a2-135">Samplers in a descriptor heap can be dynamically assigned and indexed, which static samplers cannot.</span></span>

<span data-ttu-id="531a2-136">Los muestreadores estáticos se pueden escribir como parte de la firma raíz en los sombreadores HLSL (consulte [especificación de firmas raíz en HLSL](specifying-root-signatures-in-hlsl.md)).</span><span class="sxs-lookup"><span data-stu-id="531a2-136">Static samplers can be written as part of the root signature in HLSL shaders (refer to [Specifying Root Signatures in HLSL](specifying-root-signatures-in-hlsl.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="531a2-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="531a2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="531a2-138">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="531a2-138">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




