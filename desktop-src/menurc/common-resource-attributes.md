---
title: Atributos de recursos comunes
description: Las instrucciones de definición de recursos que se admiten en Windows de 16 bits incluyen una opción Load-MEM que especifica las características de carga y memoria del recurso.
ms.assetid: 53740997-854b-447c-9ab1-de8e17c0de1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa15ae7207c80737e284151f0dfd3d7981935943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704693"
---
# <a name="common-resource-attributes"></a><span data-ttu-id="7bcb3-103">Atributos de recursos comunes</span><span class="sxs-lookup"><span data-stu-id="7bcb3-103">Common Resource Attributes</span></span>

<span data-ttu-id="7bcb3-104">Las instrucciones de definición de recursos que se admiten en Windows de 16 bits incluyen una opción *Load-MEM* que especifica las características de carga y memoria del recurso.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-104">The resource-definition statements supported on 16-bit Windows include a *load-mem* option that specifies the loading and memory characteristics of the resource.</span></span> <span data-ttu-id="7bcb3-105">Estos atributos se permiten en scripts de recursos para la compatibilidad con versiones anteriores, pero se omiten.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-105">These attributes are permitted in resource scripts for backward compatibility, but they are ignored.</span></span> <span data-ttu-id="7bcb3-106">Los recursos de Windows se cargan cuando se carga el módulo correspondiente y se liberan cuando se descarga el módulo.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-106">Windows resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

## <a name="load-attributes"></a><span data-ttu-id="7bcb3-107">Cargar atributos</span><span class="sxs-lookup"><span data-stu-id="7bcb3-107">Load Attributes</span></span>

<span data-ttu-id="7bcb3-108">Los atributos de carga especifican Cuándo se va a cargar el recurso.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-108">The load attributes specify when the resource is to be loaded.</span></span> <span data-ttu-id="7bcb3-109">El parámetro Load debe ser uno de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-109">The load parameter must be one of the following attributes.</span></span>



| <span data-ttu-id="7bcb3-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="7bcb3-110">Attribute</span></span>      | <span data-ttu-id="7bcb3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bcb3-111">Description</span></span>                                                                  |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7bcb3-112">**CARGAR previamente**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-112">**PRELOAD**</span></span>    | <span data-ttu-id="7bcb3-113">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-113">Ignored.</span></span> <span data-ttu-id="7bcb3-114">En Windows de 16 bits, el recurso se carga con el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-114">In 16-bit Windows, the resource is loaded with the executable file.</span></span> |
| <span data-ttu-id="7bcb3-115">**LOADONCALL**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-115">**LOADONCALL**</span></span> | <span data-ttu-id="7bcb3-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-116">Ignored.</span></span> <span data-ttu-id="7bcb3-117">En Windows de 16 bits, el recurso se carga cuando se llama.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-117">In 16-bit Windows, the resource is loaded when called.</span></span>              |



 

## <a name="memory-attributes"></a><span data-ttu-id="7bcb3-118">Atributos de memoria</span><span class="sxs-lookup"><span data-stu-id="7bcb3-118">Memory Attributes</span></span>

<span data-ttu-id="7bcb3-119">Los atributos de memoria especifican si el recurso es fijo o móvil, si es descartable y si es puro.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-119">The memory attributes specify whether the resource is fixed or movable, whether it is discardable, and whether it is pure.</span></span> <span data-ttu-id="7bcb3-120">El parámetro Memory puede ser uno o varios de los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-120">The memory parameter can be one or more of the following attributes.</span></span>



| <span data-ttu-id="7bcb3-121">Atributo</span><span class="sxs-lookup"><span data-stu-id="7bcb3-121">Attribute</span></span>       | <span data-ttu-id="7bcb3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bcb3-122">Description</span></span>                                                                                                                               |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bcb3-123">**FIXED**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-123">**FIXED**</span></span>       | <span data-ttu-id="7bcb3-124">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-124">Ignored.</span></span> <span data-ttu-id="7bcb3-125">En Windows de 16 bits, el recurso permanece en una ubicación de memoria fija.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-125">In 16-bit Windows, the resource remains at a fixed memory location.</span></span>                                                              |
| <span data-ttu-id="7bcb3-126">**MOVIBLE**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-126">**MOVEABLE**</span></span>    | <span data-ttu-id="7bcb3-127">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-127">Ignored.</span></span> <span data-ttu-id="7bcb3-128">En Windows de 16 bits, el recurso se puede migrar si es necesario para compactar la memoria.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-128">In 16-bit Windows, the resource can be moved if necessary to compact memory.</span></span>                                                     |
| <span data-ttu-id="7bcb3-129">**DESCARTABLE**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-129">**DISCARDABLE**</span></span> | <span data-ttu-id="7bcb3-130">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-130">Ignored.</span></span> <span data-ttu-id="7bcb3-131">En Windows de 16 bits, el recurso se puede descartar si ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-131">In 16-bit Windows, the resource can be discarded if no longer needed.</span></span>                                                            |
| <span data-ttu-id="7bcb3-132">**INCLUYA**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-132">**PURE**</span></span>        | <span data-ttu-id="7bcb3-133">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-133">Ignored.</span></span> <span data-ttu-id="7bcb3-134">Aceptado por compatibilidad con scripts de recursos existentes.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-134">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="7bcb3-135">**IMPURAS**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-135">**IMPURE**</span></span>      | <span data-ttu-id="7bcb3-136">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-136">Ignored.</span></span> <span data-ttu-id="7bcb3-137">Aceptado por compatibilidad con scripts de recursos existentes.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-137">Accepted for compatibility with existing resource scripts.</span></span>                                                                       |
| <span data-ttu-id="7bcb3-138">**RECURSO**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-138">**SHARED**</span></span>      | <span data-ttu-id="7bcb3-139">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-139">Ignored.</span></span> <span data-ttu-id="7bcb3-140">En Windows de 16 bits, se omite SHARED en los módulos normales.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-140">In 16-bit Windows, SHARED is ignored for regular modules.</span></span> <span data-ttu-id="7bcb3-141">Para un recurso de un módulo de Windows de ROM, se comparte la memoria.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-141">For a resource from a ROM Windows module, the memory is shared.</span></span>        |
| <span data-ttu-id="7bcb3-142">**NO compartidos**</span><span class="sxs-lookup"><span data-stu-id="7bcb3-142">**NONSHARED**</span></span>   | <span data-ttu-id="7bcb3-143">ignorado.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-143">Ignored.</span></span> <span data-ttu-id="7bcb3-144">En Windows de 16 bits, la Nonshared se omite para los módulos normales.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-144">In 16-bit Windows, NONSHARED is ignored for regular modules.</span></span> <span data-ttu-id="7bcb3-145">En un recurso de un módulo de Windows de ROM, no se comparte la memoria.</span><span class="sxs-lookup"><span data-stu-id="7bcb3-145">For a resource from a ROM Windows module, the memory is not shared.</span></span> |



 

 

 




