---
description: El elemento Param especifica el valor de una propiedad en una transición, un efecto u otro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento Param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906737"
---
# <a name="param-element"></a><span data-ttu-id="2a857-103">Elemento Param</span><span class="sxs-lookup"><span data-stu-id="2a857-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="2a857-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2a857-104">\[Deprecated.</span></span> <span data-ttu-id="2a857-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2a857-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2a857-106">El `param` elemento especifica el valor de una propiedad en una transición, efecto u otro subobjeto.</span><span class="sxs-lookup"><span data-stu-id="2a857-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="2a857-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a857-107">Attributes</span></span>

<span data-ttu-id="2a857-108">[**nombre**](name-attribute.md), [ **valor**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="2a857-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="2a857-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="2a857-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a857-110">Parent</span><span class="sxs-lookup"><span data-stu-id="2a857-110">Parent</span></span>   | <span data-ttu-id="2a857-111">[**clip**](clip-element.md), [**efecto**](effect-element.md), [**transición**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="2a857-111">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="2a857-112">Children</span><span class="sxs-lookup"><span data-stu-id="2a857-112">Children</span></span> | <span data-ttu-id="2a857-113">[**en**](at-element.md), [ **lineal**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="2a857-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="2a857-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a857-114">Remarks</span></span>

<span data-ttu-id="2a857-115">El atributo **Value** especifica el valor de la propiedad al inicio de la transición o efecto.</span><span class="sxs-lookup"><span data-stu-id="2a857-115">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="2a857-116">Use el elemento **at** o **linear** para especificar los valores que se van a cambiar.</span><span class="sxs-lookup"><span data-stu-id="2a857-116">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="2a857-117">Si el elemento **param** no contiene elementos **en** o **lineales** , el valor permanece constante a lo largo de la duración del efecto o de la transición.</span><span class="sxs-lookup"><span data-stu-id="2a857-117">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="2a857-118">Un elemento **param** dentro de un elemento **clip** no **puede contener elementos** in o **linear** .</span><span class="sxs-lookup"><span data-stu-id="2a857-118">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="2a857-119">Muchas transiciones admiten una propiedad de **progreso** estándar que va de 0 a 1,0, que indica el porcentaje de la transición que se refleja en la salida.</span><span class="sxs-lookup"><span data-stu-id="2a857-119">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="2a857-120">En **curso** = 0,0, la transición está al principio de su secuencia (completamente la primera imagen de vídeo).</span><span class="sxs-lookup"><span data-stu-id="2a857-120">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="2a857-121">En **curso** = 0,5, la transición está completada a la mitad.</span><span class="sxs-lookup"><span data-stu-id="2a857-121">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="2a857-122">(Por ejemplo, en un borrado, en **curso** = 0,5 el límite de la transición está en el centro de la imagen) En **curso** = 1,0, la transición se completa (por completo la segunda imagen).</span><span class="sxs-lookup"><span data-stu-id="2a857-122">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="2a857-123">De forma predeterminada, las transiciones pasan de **Progress** = 0,0 al inicio de la transición a **Progress** = 1,0 al final.</span><span class="sxs-lookup"><span data-stu-id="2a857-123">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="2a857-124">Otras propiedades suelen ser específicas de una transición o efecto determinado.</span><span class="sxs-lookup"><span data-stu-id="2a857-124">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="2a857-125">Por ejemplo, la transición de borrado admite una propiedad **GradientSize** que controla el ancho del área de transición.</span><span class="sxs-lookup"><span data-stu-id="2a857-125">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="2a857-126">Para ejecutar una transición hacia atrás, establezca la propiedad **Progress** en 1,0 al inicio de la transición y use el elemento **linear** para cambiar el valor a 0,0, tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a857-126">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="2a857-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2a857-127">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="2a857-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a857-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a857-129">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="2a857-129">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



