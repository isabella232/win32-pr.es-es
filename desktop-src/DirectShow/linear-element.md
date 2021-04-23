---
description: El elemento lineal define el valor de un elemento param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: linear (Elemento, Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910093"
---
# <a name="linear-element"></a><span data-ttu-id="60c8c-103">linear (Elemento)</span><span class="sxs-lookup"><span data-stu-id="60c8c-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="60c8c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="60c8c-104">\[Deprecated.</span></span> <span data-ttu-id="60c8c-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60c8c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="60c8c-106">El elemento lineal define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene **el elemento param.**</span><span class="sxs-lookup"><span data-stu-id="60c8c-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="60c8c-107">El `linear` elemento hace que el parámetro realice una transición sin problemas de su valor anterior al nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="60c8c-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="60c8c-108">Para un salto instantáneo a un nuevo valor, use el [**elemento at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="60c8c-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="60c8c-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="60c8c-109">Attributes</span></span>

<span data-ttu-id="60c8c-110">[**time**](time-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="60c8c-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="60c8c-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="60c8c-111">Parent/Child Information</span></span>



| <span data-ttu-id="60c8c-112">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="60c8c-112">Label</span></span> | <span data-ttu-id="60c8c-113">Value</span><span class="sxs-lookup"><span data-stu-id="60c8c-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="60c8c-114">Parent</span><span class="sxs-lookup"><span data-stu-id="60c8c-114">Parent</span></span>   | [<span data-ttu-id="60c8c-115">**param**</span><span class="sxs-lookup"><span data-stu-id="60c8c-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="60c8c-116">Children</span><span class="sxs-lookup"><span data-stu-id="60c8c-116">Children</span></span> | <span data-ttu-id="60c8c-117">None</span><span class="sxs-lookup"><span data-stu-id="60c8c-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="60c8c-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="60c8c-118">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="60c8c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c8c-119">Requirements</span></span>



| <span data-ttu-id="60c8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c8c-120">Requirement</span></span> | <span data-ttu-id="60c8c-121">Value</span><span class="sxs-lookup"><span data-stu-id="60c8c-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c8c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60c8c-122">Header</span></span><br/> | <dl> <span data-ttu-id="60c8c-123"><dt>Camerauicontrol.h</dt></span><span class="sxs-lookup"><span data-stu-id="60c8c-123"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60c8c-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60c8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c8c-125">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="60c8c-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




