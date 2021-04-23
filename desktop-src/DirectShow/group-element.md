---
description: El elemento group define un grupo, el objeto de nivel superior en una escala de tiempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: elemento group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909253"
---
# <a name="group-element"></a><span data-ttu-id="56b57-103">group (Elemento)</span><span class="sxs-lookup"><span data-stu-id="56b57-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="56b57-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="56b57-104">\[Deprecated.</span></span> <span data-ttu-id="56b57-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="56b57-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56b57-106">El **elemento group** define un grupo, el objeto de nivel superior en una escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="56b57-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="56b57-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="56b57-107">Attributes</span></span>

<span data-ttu-id="56b57-108">[**bitdepth,**](bitdepth-attribute.md) [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="56b57-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="56b57-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="56b57-109">Parent/Child Information</span></span>



| <span data-ttu-id="56b57-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="56b57-110">Label</span></span> | <span data-ttu-id="56b57-111">Value</span><span class="sxs-lookup"><span data-stu-id="56b57-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b57-112">Parent</span><span class="sxs-lookup"><span data-stu-id="56b57-112">Parent</span></span>   | [<span data-ttu-id="56b57-113">**línea de tiempo**</span><span class="sxs-lookup"><span data-stu-id="56b57-113">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="56b57-114">Children</span><span class="sxs-lookup"><span data-stu-id="56b57-114">Children</span></span> | <span data-ttu-id="56b57-115">[**compuesto**](composite-element.md), [**efecto**](effect-element.md), [**pista**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="56b57-115">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="56b57-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="56b57-116">Remarks</span></span>

<span data-ttu-id="56b57-117">Dentro de `group` un elemento, la prioridad de las capas anidadas se determina implícitamente por el orden en que aparecen dentro del elemento.</span><span class="sxs-lookup"><span data-stu-id="56b57-117">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="56b57-118">La primera capa tiene prioridad 0 y las capas posteriores tienen valores de prioridad crecientes.</span><span class="sxs-lookup"><span data-stu-id="56b57-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="56b57-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56b57-119">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="56b57-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="56b57-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b57-121">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="56b57-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



