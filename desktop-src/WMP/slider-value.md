---
title: Control deslizante. valor
description: El atributo value especifica o recupera la posición actual del control deslizante. | Control deslizante. valor
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Control deslizante. Value Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660547"
---
# <a name="slidervalue"></a><span data-ttu-id="ae372-105">Control deslizante. valor</span><span class="sxs-lookup"><span data-stu-id="ae372-105">SLIDER.value</span></span>

<span data-ttu-id="ae372-106">El atributo **Value** especifica o recupera la posición actual del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="ae372-106">The **value** attribute specifies or retrieves the current position of the slider.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="ae372-107">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="ae372-107">Possible Values</span></span>

<span data-ttu-id="ae372-108">Este atributo es un **número** de lectura/escritura (**float**) con un valor predeterminado de **min**.</span><span class="sxs-lookup"><span data-stu-id="ae372-108">This attribute is a read/write **Number** (**float**) with a default value of **min**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae372-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae372-109">Remarks</span></span>

<span data-ttu-id="ae372-110">El **valor** siempre debe ser mayor o igual que **min** y menor o igual que **Max**. Si especifica un valor fuera de este intervalo, el **valor** y la posición del control deslizante no cambian.</span><span class="sxs-lookup"><span data-stu-id="ae372-110">The **value** should always be greater than or equal to **min** and less than or equal to **max**. If you specify a value outside this range, **value** and the position of the slider are not changed.</span></span>

<span data-ttu-id="ae372-111">Vea **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="ae372-111">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae372-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae372-112">Requirements</span></span>



| <span data-ttu-id="ae372-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae372-113">Requirement</span></span> | <span data-ttu-id="ae372-114">Value</span><span class="sxs-lookup"><span data-stu-id="ae372-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ae372-115">Versión</span><span class="sxs-lookup"><span data-stu-id="ae372-115">Version</span></span><br/> | <span data-ttu-id="ae372-116">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ae372-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae372-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae372-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae372-118">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="ae372-118">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="ae372-119">**SLIDEr. min**</span><span class="sxs-lookup"><span data-stu-id="ae372-119">**SLIDER.min**</span></span>](slider-min.md)
</dt> </dl>

 

 





