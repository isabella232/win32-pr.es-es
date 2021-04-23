---
description: El elemento compuesto define una composición, un objeto contenedor para pistas y otras composiciones anidadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908843"
---
# <a name="composite-element"></a><span data-ttu-id="84dbe-103">elemento composite</span><span class="sxs-lookup"><span data-stu-id="84dbe-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="84dbe-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="84dbe-104">\[Deprecated.</span></span> <span data-ttu-id="84dbe-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="84dbe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="84dbe-106">El `composite` elemento define una composición, un objeto contenedor para pistas y otras composiciones anidadas.</span><span class="sxs-lookup"><span data-stu-id="84dbe-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="84dbe-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="84dbe-107">Attributes</span></span>

<span data-ttu-id="84dbe-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="84dbe-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="84dbe-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="84dbe-109">Parent/Child Information</span></span>



| <span data-ttu-id="84dbe-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="84dbe-110">Label</span></span> | <span data-ttu-id="84dbe-111">Value</span><span class="sxs-lookup"><span data-stu-id="84dbe-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84dbe-112">Parent</span><span class="sxs-lookup"><span data-stu-id="84dbe-112">Parent</span></span>   | <span data-ttu-id="84dbe-113">`composite`, [ **group**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="84dbe-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="84dbe-114">Children</span><span class="sxs-lookup"><span data-stu-id="84dbe-114">Children</span></span> | <span data-ttu-id="84dbe-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="84dbe-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="84dbe-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84dbe-116">Remarks</span></span>

<span data-ttu-id="84dbe-117">Dentro de un elemento, la prioridad de las capas anidadas viene determinada implícitamente por `composite` el orden en que aparecen dentro del elemento.</span><span class="sxs-lookup"><span data-stu-id="84dbe-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="84dbe-118">La primera capa tiene prioridad 0 y las capas posteriores tienen valores de prioridad crecientes.</span><span class="sxs-lookup"><span data-stu-id="84dbe-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="84dbe-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="84dbe-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="84dbe-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="84dbe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84dbe-121">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="84dbe-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



