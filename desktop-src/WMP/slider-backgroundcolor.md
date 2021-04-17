---
title: Control deslizante. backgroundColor
description: El atributo backgroundColor especifica o recupera el color de fondo del control deslizante.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- CONTROL SLIDEr. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660220"
---
# <a name="sliderbackgroundcolor"></a><span data-ttu-id="4f275-104">Control deslizante. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4f275-104">SLIDER.backgroundColor</span></span>

<span data-ttu-id="4f275-105">El atributo **BackgroundColor** especifica o recupera el color de fondo del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="4f275-105">The **backgroundColor** attribute specifies or retrieves the background color of the slider control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="4f275-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4f275-106">Possible Values</span></span>

<span data-ttu-id="4f275-107">Este atributo es una **cadena** de lectura/escritura que contiene cualquier valor de color de Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4f275-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="4f275-108">No tiene valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4f275-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f275-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f275-109">Remarks</span></span>

<span data-ttu-id="4f275-110">Un control deslizante básico se puede construir especificando **BackgroundColor** o **BackgroundImage**, y **foregroundColor** o **foregroundImage**.</span><span class="sxs-lookup"><span data-stu-id="4f275-110">A basic slider control can be constructed by specifying **backgroundColor** or **backgroundImage**, and **foregroundColor** or **foregroundImage**.</span></span>

<span data-ttu-id="4f275-111">Al usar los colores, las dimensiones del control deslizante definen el área rellenada por el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="4f275-111">When using the colors, the dimensions of the slider control define the area filled by the background color.</span></span> <span data-ttu-id="4f275-112">El color de primer plano cubre el color de fondo a medida que aumenta la posición del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="4f275-112">The foreground color covers the background color as the slider position increases.</span></span>

<span data-ttu-id="4f275-113">Para hacer un relleno de degradado del área ocupada por el color de fondo o de primer plano, especifique los atributos **backgroundEndColor** o **foregroundEndColor** .</span><span class="sxs-lookup"><span data-stu-id="4f275-113">To make a gradient fill of the area occupied by the background or foreground color, specify the **backgroundEndColor** or **foregroundEndColor** attributes.</span></span>

<span data-ttu-id="4f275-114">Vea *CUSTOMSLIDER*. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="4f275-114">See the *CUSTOMSLIDER*.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f275-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f275-115">Requirements</span></span>



| <span data-ttu-id="4f275-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f275-116">Requirement</span></span> | <span data-ttu-id="4f275-117">Value</span><span class="sxs-lookup"><span data-stu-id="4f275-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4f275-118">Versión</span><span class="sxs-lookup"><span data-stu-id="4f275-118">Version</span></span><br/> | <span data-ttu-id="4f275-119">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4f275-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f275-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f275-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f275-121">**Referencia de color**</span><span class="sxs-lookup"><span data-stu-id="4f275-121">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="4f275-122">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="4f275-122">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="4f275-123">**SLIDEr. backgroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="4f275-123">**SLIDER.backgroundEndColor**</span></span>](slider-backgroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="4f275-124">**Control deslizante. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="4f275-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="4f275-125">**SLIDEr. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="4f275-125">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="4f275-126">**SLIDEr. foregroundEndColor**</span><span class="sxs-lookup"><span data-stu-id="4f275-126">**SLIDER.foregroundEndColor**</span></span>](slider-foregroundendcolor.md)
</dt> <dt>

[<span data-ttu-id="4f275-127">**SLIDEr. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="4f275-127">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





