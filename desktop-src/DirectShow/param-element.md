---
description: El elemento param especifica el valor de una propiedad en una transición, un efecto u otro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909043"
---
# <a name="param-element"></a><span data-ttu-id="7c2d5-103">elemento param</span><span class="sxs-lookup"><span data-stu-id="7c2d5-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="7c2d5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-104">\[Deprecated.</span></span> <span data-ttu-id="7c2d5-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c2d5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7c2d5-106">El `param` elemento especifica el valor de una propiedad en una transición, un efecto u otro subobjeto.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="7c2d5-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="7c2d5-107">Attributes</span></span>

<span data-ttu-id="7c2d5-108">[**name**](name-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="7c2d5-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="7c2d5-109">Información de elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="7c2d5-109">Parent/Child Information</span></span>



| <span data-ttu-id="7c2d5-110">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="7c2d5-110">Label</span></span> | <span data-ttu-id="7c2d5-111">Value</span><span class="sxs-lookup"><span data-stu-id="7c2d5-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c2d5-112">Parent</span><span class="sxs-lookup"><span data-stu-id="7c2d5-112">Parent</span></span>   | <span data-ttu-id="7c2d5-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="7c2d5-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="7c2d5-114">Children</span><span class="sxs-lookup"><span data-stu-id="7c2d5-114">Children</span></span> | <span data-ttu-id="7c2d5-115">[**en**](at-element.md), [ **lineal**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="7c2d5-115">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="7c2d5-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7c2d5-116">Remarks</span></span>

<span data-ttu-id="7c2d5-117">El **atributo** value especifica el valor de la propiedad al principio de la transición o efecto.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-117">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="7c2d5-118">Use el **elemento en** o **lineal** para especificar valores cambiantes.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-118">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="7c2d5-119">Si el **elemento param** no contiene elementos **en** o **lineales,** el valor permanece constante durante la duración del efecto o la transición.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-119">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="7c2d5-120">Un **elemento param** dentro de un **elemento clip** no puede contener elementos **en** o **lineales.**</span><span class="sxs-lookup"><span data-stu-id="7c2d5-120">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="7c2d5-121">Muchas transiciones admiten una propiedad **Progress** estándar que oscila entre 0 y 1,0, lo que indica qué porcentaje de la transición se refleja en la salida.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-121">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="7c2d5-122">En **Progreso** = 0,0, la transición está al principio de su secuencia (completamente la primera imagen de vídeo).</span><span class="sxs-lookup"><span data-stu-id="7c2d5-122">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="7c2d5-123">En **Progreso** = 0,5, la transición se completa a la mitad.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-123">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="7c2d5-124">(Por ejemplo, en un borrado, en **Progreso** = 0,5, el límite de transición está en el centro de la imagen) En **Progreso** = 1.0, la transición se completa (completamente la segunda imagen).</span><span class="sxs-lookup"><span data-stu-id="7c2d5-124">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="7c2d5-125">De forma predeterminada, las transiciones van desde **Progreso** = 0,0 al principio de la transición a **Progreso** = 1,0 al final.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-125">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="7c2d5-126">Otras propiedades suelen ser específicas de una transición o efecto determinados.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-126">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="7c2d5-127">Por ejemplo, la transición de borrado admite una **propiedad GradientSize** que controla el ancho del área de transición.</span><span class="sxs-lookup"><span data-stu-id="7c2d5-127">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="7c2d5-128">Para ejecutar una transición hacia atrás, establezca la propiedad **Progress** en 1.0 al principio de la transición y use el elemento **lineal** para cambiar el valor a 0.0, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7c2d5-128">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="7c2d5-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7c2d5-129">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="7c2d5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c2d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c2d5-131">Elementos XTL</span><span class="sxs-lookup"><span data-stu-id="7c2d5-131">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



