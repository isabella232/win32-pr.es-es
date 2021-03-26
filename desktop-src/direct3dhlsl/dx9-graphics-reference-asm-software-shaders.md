---
title: Sombreadores de software
description: Los sombreadores de software se implementan para permitir el desarrollo de sombreadores sin soporte de hardware subyacente. Admiten el conjunto completo de características. Dado que se implementan en el software, no producirán el mejor rendimiento.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076394"
---
# <a name="software-shaders"></a><span data-ttu-id="61606-105">Sombreadores de software</span><span class="sxs-lookup"><span data-stu-id="61606-105">Software Shaders</span></span>

<span data-ttu-id="61606-106">Los sombreadores de software se implementan para permitir el desarrollo de sombreadores sin soporte de hardware subyacente.</span><span class="sxs-lookup"><span data-stu-id="61606-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="61606-107">Admiten el conjunto completo de características.</span><span class="sxs-lookup"><span data-stu-id="61606-107">They support the full feature set.</span></span> <span data-ttu-id="61606-108">Dado que se implementan en el software, no producirán el mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="61606-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="61606-109">Versión</span><span class="sxs-lookup"><span data-stu-id="61606-109">Version</span></span>   | <span data-ttu-id="61606-110">Conjunto de características</span><span class="sxs-lookup"><span data-stu-id="61606-110">Feature Set</span></span>                  | <span data-ttu-id="61606-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61606-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="61606-112">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="61606-112">vs\_2\_sw</span></span> | <span data-ttu-id="61606-113">Todas las características de vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="61606-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="61606-114">Solo es compatible con el procesamiento de vértices de software y un dispositivo de referencia.</span><span class="sxs-lookup"><span data-stu-id="61606-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="61606-115">vs \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="61606-115">vs\_3\_sw</span></span> | <span data-ttu-id="61606-116">Todas las características de vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="61606-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="61606-117">Solo es compatible con el procesamiento de vértices de software y un dispositivo de referencia.</span><span class="sxs-lookup"><span data-stu-id="61606-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="61606-118">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="61606-118">ps\_2\_sw</span></span> | <span data-ttu-id="61606-119">Todas las características de PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="61606-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="61606-120">Solo se admite en un dispositivo de referencia.</span><span class="sxs-lookup"><span data-stu-id="61606-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="61606-121">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="61606-121">ps\_3\_sw</span></span> | <span data-ttu-id="61606-122">Todas las características de PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="61606-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="61606-123">Solo se admite en un dispositivo de referencia.</span><span class="sxs-lookup"><span data-stu-id="61606-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="61606-124">Se relajan algunas validaciones para los sombreadores de software.</span><span class="sxs-lookup"><span data-stu-id="61606-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="61606-125">Esto resulta útil para la depuración y la generación de prototipos.</span><span class="sxs-lookup"><span data-stu-id="61606-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="61606-126">Las validaciones siguientes son relajadas: (todas las demás validaciones siguen siendo las mismas)</span><span class="sxs-lookup"><span data-stu-id="61606-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="61606-127">Tipo de validación</span><span class="sxs-lookup"><span data-stu-id="61606-127">Validation type</span></span>                                 | <span data-ttu-id="61606-128">Flexibiliza</span><span class="sxs-lookup"><span data-stu-id="61606-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61606-129">Recuentos de instrucciones:</span><span class="sxs-lookup"><span data-stu-id="61606-129">Instruction Counts:</span></span>                             | <span data-ttu-id="61606-130">Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="61606-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="61606-131">Se permiten instrucciones ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="61606-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="61606-132">Recuentos de constantes float:</span><span class="sxs-lookup"><span data-stu-id="61606-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="61606-133">Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="61606-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="61606-134">Se permiten hasta 8192 constantes.</span><span class="sxs-lookup"><span data-stu-id="61606-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="61606-135">Recuentos de constantes de enteros:</span><span class="sxs-lookup"><span data-stu-id="61606-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="61606-136">Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="61606-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="61606-137">Se permiten hasta 2048 constantes.</span><span class="sxs-lookup"><span data-stu-id="61606-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="61606-138">Recuentos de constantes booleanas:</span><span class="sxs-lookup"><span data-stu-id="61606-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="61606-139">Esto es flexible para vs \_ 2 \_ SW, vs \_ 3 SW \_ y PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="61606-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="61606-140">Se permiten hasta 2048 constantes.</span><span class="sxs-lookup"><span data-stu-id="61606-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="61606-141">Dependiente: profundidad de lectura:</span><span class="sxs-lookup"><span data-stu-id="61606-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="61606-142">Esto es flexible para el \_ SW PS 2 \_ .</span><span class="sxs-lookup"><span data-stu-id="61606-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="61606-143">Al igual que en vs \_ 3 \_ 0 y PS \_ 3 \_ 0, se permiten lecturas dependientes ilimitadas.</span><span class="sxs-lookup"><span data-stu-id="61606-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="61606-144">Número de instrucciones de control de flujo y etiquetas:</span><span class="sxs-lookup"><span data-stu-id="61606-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="61606-145">Esto es relajado para vs \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="61606-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="61606-146">Instrucciones de control de flujo ilimitado y se permiten las etiquetas 2048.</span><span class="sxs-lookup"><span data-stu-id="61606-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="61606-147">Recuento de bucles/Inicio/paso:</span><span class="sxs-lookup"><span data-stu-id="61606-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="61606-148">Estos son relajados para vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW y PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="61606-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="61606-149">El inicio de la iteración y el tamaño del paso de interoperabilidad para instrucciones REP y Loop son intergers con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="61606-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="61606-150">El recuento de interconexiones puede ser hasta el máximo de \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="61606-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="61606-151">Límites de puerto de lectura:</span><span class="sxs-lookup"><span data-stu-id="61606-151">Read-port limits:</span></span>                               | <span data-ttu-id="61606-152">vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW y PS \_ 3 \_ SW no tienen límite de puerto de lectura.</span><span class="sxs-lookup"><span data-stu-id="61606-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="61606-153">Número de interpoladores:</span><span class="sxs-lookup"><span data-stu-id="61606-153">Number of interpolators:</span></span>                        | <span data-ttu-id="61606-154">Hay 16 [registros-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) en vs \_ 3 \_ SW y 10 [PS \_ 3 \_ 0 registros](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) para el \_ Software PS 3 \_ .</span><span class="sxs-lookup"><span data-stu-id="61606-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="61606-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61606-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61606-156">Referencia del sombreador de ASM</span><span class="sxs-lookup"><span data-stu-id="61606-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




