---
description: Consideraciones de rendimiento (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Consideraciones de rendimiento (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080143"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="54c08-103">Consideraciones de rendimiento (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="54c08-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="54c08-104">Uso de grupos de efectos</span><span class="sxs-lookup"><span data-stu-id="54c08-104">Using Effect Pools</span></span>

<span data-ttu-id="54c08-105">Es habitual que las canalizaciones de representación utilicen muchos sombreadores para representar diferentes tipos de objeto y efectos especiales.</span><span class="sxs-lookup"><span data-stu-id="54c08-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="54c08-106">El sombreador es una mezcla de Estados que es común entre todos los sombreadores, como una matriz mundial o una posición ligera, y otro estado específico de cada sombreador, como el color difuso de un objeto o el cálculo del resaltado especular.</span><span class="sxs-lookup"><span data-stu-id="54c08-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="54c08-107">Un grupo de efectos es un lugar en la memoria para almacenar el estado que se usa en muchos sombreadores, así como objetos de dispositivo comunes como, por ejemplo, sombreadores, objetos de estado de representación y búferes de constantes.</span><span class="sxs-lookup"><span data-stu-id="54c08-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="54c08-108">Los resultados de la mejora del rendimiento de la actualización del Estado común una vez para todos los sombreadores que necesitan ese estado.</span><span class="sxs-lookup"><span data-stu-id="54c08-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="54c08-109">Un grupo de efectos es una ubicación de memoria compartida para el estado de efecto.</span><span class="sxs-lookup"><span data-stu-id="54c08-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="54c08-110">Un grupo se crea de forma similar a un efecto; se puede crear a partir de la memoria (o un archivo o un recurso).</span><span class="sxs-lookup"><span data-stu-id="54c08-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="54c08-111">Esto conduce a dos tipos diferentes de efectos: un efecto global que no depende del estado en otro efecto frente a un efecto secundario que depende del estado de otro efecto.</span><span class="sxs-lookup"><span data-stu-id="54c08-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="54c08-112">Especifique si un efecto es un efecto global (el caso predeterminado) o un efecto secundario (proporcionando la marca de efecto de [ \_ \_ compilar efecto \_ secundario \_ de D3D10](d3d10-effect.md) ) cuando se crea el efecto.</span><span class="sxs-lookup"><span data-stu-id="54c08-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="54c08-113">Un efecto global puede servir como grupo de efectos; un efecto secundario no puede ser un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="54c08-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54c08-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="54c08-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54c08-115">Representar un efecto</span><span class="sxs-lookup"><span data-stu-id="54c08-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="54c08-116">Efectos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="54c08-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



