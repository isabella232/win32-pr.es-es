---
title: Niveles de hardware
description: Los niveles de hardware del nivel 1 al nivel 3 tienen recursos crecientes disponibles para la canalización.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2020
ms.locfileid: "104549070"
---
# <a name="hardware-tiers"></a><span data-ttu-id="e028d-103">Niveles de hardware</span><span class="sxs-lookup"><span data-stu-id="e028d-103">Hardware Tiers</span></span>

<span data-ttu-id="e028d-104">Los niveles de hardware del nivel 1 al nivel 3 tienen recursos crecientes disponibles para la canalización.</span><span class="sxs-lookup"><span data-stu-id="e028d-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="e028d-105">Límites dependientes del hardware</span><span class="sxs-lookup"><span data-stu-id="e028d-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="e028d-106">Límites invariables</span><span class="sxs-lookup"><span data-stu-id="e028d-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="e028d-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e028d-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="e028d-108">Límites dependientes del hardware</span><span class="sxs-lookup"><span data-stu-id="e028d-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="e028d-109">Recursos disponibles para la canalización</span><span class="sxs-lookup"><span data-stu-id="e028d-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="e028d-110">Nivel 1</span><span class="sxs-lookup"><span data-stu-id="e028d-110">Tier 1</span></span>                                                                   | <span data-ttu-id="e028d-111">Nivel 2</span><span class="sxs-lookup"><span data-stu-id="e028d-111">Tier 2</span></span>        | <span data-ttu-id="e028d-112">Nivel 3</span><span class="sxs-lookup"><span data-stu-id="e028d-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="e028d-113">Niveles de características</span><span class="sxs-lookup"><span data-stu-id="e028d-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="e028d-114">11.0 +</span><span class="sxs-lookup"><span data-stu-id="e028d-114">11.0+</span></span>                                                                    | <span data-ttu-id="e028d-115">11.0 +</span><span class="sxs-lookup"><span data-stu-id="e028d-115">11.0+</span></span>         | <span data-ttu-id="e028d-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="e028d-116">11.1+</span></span>         |
| <span data-ttu-id="e028d-117">Número máximo de descriptores en un montón de vista de búfer de constantes (CBV), sombreador Vista de recursos (SRV) o vista de acceso desordenado (UAV) que se usa para la representación</span><span class="sxs-lookup"><span data-stu-id="e028d-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="e028d-118">1 000 000</span><span class="sxs-lookup"><span data-stu-id="e028d-118">1,000,000</span></span>                                                                | <span data-ttu-id="e028d-119">1 000 000</span><span class="sxs-lookup"><span data-stu-id="e028d-119">1,000,000</span></span>     | <span data-ttu-id="e028d-120">1000000 +</span><span class="sxs-lookup"><span data-stu-id="e028d-120">1,000,000+</span></span>    |
| <span data-ttu-id="e028d-121">Número máximo de vistas de búfer constantes en todas las tablas de descriptores por fase de sombreador</span><span class="sxs-lookup"><span data-stu-id="e028d-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="e028d-122">14</span><span class="sxs-lookup"><span data-stu-id="e028d-122">14</span></span>                                                                       | <span data-ttu-id="e028d-123">14</span><span class="sxs-lookup"><span data-stu-id="e028d-123">14</span></span>            | <span data-ttu-id="e028d-124">**montón completo**</span><span class="sxs-lookup"><span data-stu-id="e028d-124">**full heap**</span></span> |
| <span data-ttu-id="e028d-125">Número máximo de vistas de recursos de sombreador en todas las tablas de descriptores por fase de sombreador</span><span class="sxs-lookup"><span data-stu-id="e028d-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="e028d-126">128</span><span class="sxs-lookup"><span data-stu-id="e028d-126">128</span></span>                                                                      | <span data-ttu-id="e028d-127">**montón completo**</span><span class="sxs-lookup"><span data-stu-id="e028d-127">**full heap**</span></span> | <span data-ttu-id="e028d-128">montón completo</span><span class="sxs-lookup"><span data-stu-id="e028d-128">full heap</span></span>     |
| <span data-ttu-id="e028d-129">Número máximo de vistas de acceso desordenado en todas las tablas de descriptores en todas las fases</span><span class="sxs-lookup"><span data-stu-id="e028d-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="e028d-130">64 para los niveles de características 11.1 +</span><span class="sxs-lookup"><span data-stu-id="e028d-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="e028d-131">8 para el nivel de característica 11</span><span class="sxs-lookup"><span data-stu-id="e028d-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="e028d-132">64</span><span class="sxs-lookup"><span data-stu-id="e028d-132">64</span></span>            | <span data-ttu-id="e028d-133">**montón completo**</span><span class="sxs-lookup"><span data-stu-id="e028d-133">**full heap**</span></span> |
| <span data-ttu-id="e028d-134">Número máximo de muestras en todas las tablas de descriptores por fase de sombreador</span><span class="sxs-lookup"><span data-stu-id="e028d-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="e028d-135">16</span><span class="sxs-lookup"><span data-stu-id="e028d-135">16</span></span>                                                                       | <span data-ttu-id="e028d-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="e028d-136">**2048**</span></span> | <span data-ttu-id="e028d-137">2048</span><span class="sxs-lookup"><span data-stu-id="e028d-137">2048</span></span>     |



 

<span data-ttu-id="e028d-138">Las entradas en **negrita** destacan mejoras significativas en el nivel anterior.</span><span class="sxs-lookup"><span data-stu-id="e028d-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="e028d-139">Existe una restricción adicional para el hardware de nivel 1 que se aplica a todos los montones, y al hardware de nivel 2 que se aplica a los montones CBV y UAV, que todas las entradas del montón de descriptores que se incluyen en las tablas de descriptor de la firma raíz se *deben* rellenar con descriptores en el momento en que se ejecuta el sombreador</span><span class="sxs-lookup"><span data-stu-id="e028d-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="e028d-140">No hay ninguna restricción para el hardware de nivel 3.</span><span class="sxs-lookup"><span data-stu-id="e028d-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="e028d-141">Una mitigación de esta restricción es el uso diligente de [descriptores null](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="e028d-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="e028d-142">Límites invariables</span><span class="sxs-lookup"><span data-stu-id="e028d-142">Invariable limits</span></span>

<span data-ttu-id="e028d-143">El número máximo de muestras en un montón de descriptor visible del sombreador es 2048.</span><span class="sxs-lookup"><span data-stu-id="e028d-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="e028d-144">El número máximo de muestras estáticas únicas en las firmas de raíz dinámica es 2032 (que deja 16 para los controladores que necesitan sus propios muestreadores).</span><span class="sxs-lookup"><span data-stu-id="e028d-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e028d-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e028d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e028d-146">Montones de descriptores</span><span class="sxs-lookup"><span data-stu-id="e028d-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="e028d-147">Niveles de características de hardware</span><span class="sxs-lookup"><span data-stu-id="e028d-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 





