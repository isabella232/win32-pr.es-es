---
title: AmbientAttributes.alphaBlendTo
description: El método alphaBlendTo ajusta la propiedad alphaBlend durante un período de tiempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes. alphaBlendTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699541"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="abf00-104">AmbientAttributes.alphaBlendTo</span><span class="sxs-lookup"><span data-stu-id="abf00-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="abf00-105">El método **alphaBlendTo** ajusta la propiedad **alphaBlend** durante un período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="abf00-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="abf00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abf00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf00-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span><span class="sxs-lookup"><span data-stu-id="abf00-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="abf00-108">**Número** (largo) que especifica el nuevo valor de opacidad.</span><span class="sxs-lookup"><span data-stu-id="abf00-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="abf00-109">Oscila entre 0 (sin opacidad) y 255 (opacidad completa).</span><span class="sxs-lookup"><span data-stu-id="abf00-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="abf00-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span><span class="sxs-lookup"><span data-stu-id="abf00-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="abf00-111">**Número** (**largo**) que especifica el tiempo, en milisegundos, que toma el elemento para cambiar la opacidad.</span><span class="sxs-lookup"><span data-stu-id="abf00-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf00-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abf00-112">Return Value</span></span>

<span data-ttu-id="abf00-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="abf00-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abf00-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abf00-114">Remarks</span></span>

<span data-ttu-id="abf00-115">Este método es útil para que los elementos aparezcan o desaparezcan gradualmente.</span><span class="sxs-lookup"><span data-stu-id="abf00-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="abf00-116">Cuando se usa **alphaBlendTo** con un elemento de **texto** que no tiene el parámetro **BackgroundColor** especificado, se usará un color de fondo negro.</span><span class="sxs-lookup"><span data-stu-id="abf00-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="abf00-117">Si el color de primer plano también es negro (que es el valor predeterminado del *texto*).**foregroundColor**), es posible que el texto sea ilegible.</span><span class="sxs-lookup"><span data-stu-id="abf00-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="abf00-118">Para evitarlo, especifique siempre el atributo **BackgroundColor** o establezca **foregroundColor** en un color distinto de Black.</span><span class="sxs-lookup"><span data-stu-id="abf00-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="abf00-119">Este atributo no se admite en Windows 98.</span><span class="sxs-lookup"><span data-stu-id="abf00-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="abf00-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abf00-120">Requirements</span></span>



| <span data-ttu-id="abf00-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="abf00-121">Requirement</span></span> | <span data-ttu-id="abf00-122">Value</span><span class="sxs-lookup"><span data-stu-id="abf00-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="abf00-123">Versión</span><span class="sxs-lookup"><span data-stu-id="abf00-123">Version</span></span><br/> | <span data-ttu-id="abf00-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="abf00-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abf00-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="abf00-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf00-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="abf00-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="abf00-127">**AmbientAttributes.alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="abf00-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="abf00-128">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="abf00-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="abf00-129">**TEXT. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="abf00-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="abf00-130">**TEXT. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="abf00-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





