---
description: El elemento compuesto define una composición, un objeto contenedor para las pistas y otras composiciones anidadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento compuesto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677077"
---
# <a name="composite-element"></a><span data-ttu-id="719eb-103">Elemento compuesto</span><span class="sxs-lookup"><span data-stu-id="719eb-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="719eb-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="719eb-104">\[Deprecated.</span></span> <span data-ttu-id="719eb-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="719eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="719eb-106">El `composite` elemento define una composición, un objeto contenedor para pistas y otras composiciones anidadas.</span><span class="sxs-lookup"><span data-stu-id="719eb-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="719eb-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="719eb-107">Attributes</span></span>

<span data-ttu-id="719eb-108">[**Lock**](lock-attribute.md), [**MUTE**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="719eb-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="719eb-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="719eb-109">Parent/Child Information</span></span>



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="719eb-110">Parent</span><span class="sxs-lookup"><span data-stu-id="719eb-110">Parent</span></span>   | <span data-ttu-id="719eb-111">`composite`, [ **Grupo**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="719eb-111">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="719eb-112">Children</span><span class="sxs-lookup"><span data-stu-id="719eb-112">Children</span></span> | <span data-ttu-id="719eb-113">`composite`, [**efecto**](effect-element.md), [**seguimiento**](track-element.md), [**transición**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="719eb-113">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="719eb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="719eb-114">Remarks</span></span>

<span data-ttu-id="719eb-115">Dentro de un `composite` elemento, la prioridad de las capas anidadas viene determinada implícitamente por el orden en que aparecen dentro del elemento.</span><span class="sxs-lookup"><span data-stu-id="719eb-115">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="719eb-116">La primera capa tiene prioridad 0 y las capas siguientes tienen valores de prioridad crecientes.</span><span class="sxs-lookup"><span data-stu-id="719eb-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="719eb-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="719eb-117">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="719eb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="719eb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="719eb-119">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="719eb-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



