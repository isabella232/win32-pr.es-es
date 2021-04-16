---
description: El elemento linear define el valor de un elemento Param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento Param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678983"
---
# <a name="linear-element"></a><span data-ttu-id="fc2a5-103">Elemento linear</span><span class="sxs-lookup"><span data-stu-id="fc2a5-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="fc2a5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-104">\[Deprecated.</span></span> <span data-ttu-id="fc2a5-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc2a5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fc2a5-106">El elemento linear define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="fc2a5-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="fc2a5-107">El `linear` elemento hace que el parámetro realice una transición fluida de su valor anterior al nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="fc2a5-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="fc2a5-108">Para un salto instantáneo a un nuevo valor, use el elemento [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fc2a5-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="fc2a5-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc2a5-109">Attributes</span></span>

<span data-ttu-id="fc2a5-110">[**hora**](time-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="fc2a5-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="fc2a5-111">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="fc2a5-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="fc2a5-112">Parent</span><span class="sxs-lookup"><span data-stu-id="fc2a5-112">Parent</span></span>   | [<span data-ttu-id="fc2a5-113">**param**</span><span class="sxs-lookup"><span data-stu-id="fc2a5-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="fc2a5-114">Children</span><span class="sxs-lookup"><span data-stu-id="fc2a5-114">Children</span></span> | <span data-ttu-id="fc2a5-115">None</span><span class="sxs-lookup"><span data-stu-id="fc2a5-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="fc2a5-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fc2a5-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="fc2a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc2a5-117">Requirements</span></span>



| <span data-ttu-id="fc2a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc2a5-118">Requirement</span></span> | <span data-ttu-id="fc2a5-119">Value</span><span class="sxs-lookup"><span data-stu-id="fc2a5-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2a5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc2a5-120">Header</span></span><br/> | <dl> <span data-ttu-id="fc2a5-121"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc2a5-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc2a5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc2a5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc2a5-123">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="fc2a5-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




