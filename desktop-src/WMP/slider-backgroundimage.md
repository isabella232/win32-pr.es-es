---
title: Control deslizante. backgroundImage
description: El atributo backgroundImage especifica o recupera la imagen de fondo del control deslizante.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Control deslizante. backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660218"
---
# <a name="sliderbackgroundimage"></a><span data-ttu-id="a106c-104">Control deslizante. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="a106c-104">SLIDER.backgroundImage</span></span>

<span data-ttu-id="a106c-105">El atributo **BackgroundImage** especifica o recupera la imagen de fondo del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="a106c-105">The **backgroundImage** attribute specifies or retrieves the background image of the slider.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="a106c-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a106c-106">Possible Values</span></span>

<span data-ttu-id="a106c-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="a106c-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a106c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a106c-108">Remarks</span></span>

<span data-ttu-id="a106c-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="a106c-109">This attribute is optional.</span></span> <span data-ttu-id="a106c-110">Al usar imágenes para construir un control deslizante, la **BackgroundImage** se usa para la imagen del control deslizante principal.</span><span class="sxs-lookup"><span data-stu-id="a106c-110">When using images to construct a slider, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="a106c-111">**ThumbImage** representa el control deslizante real y se puede desplazar mediante el mouse.</span><span class="sxs-lookup"><span data-stu-id="a106c-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="a106c-112">En el control deslizante **thumbImage** hay una línea invisible en la que se muestra la imagen de fondo en un lado de la línea y la imagen de primer plano se muestra en el otro lado.</span><span class="sxs-lookup"><span data-stu-id="a106c-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="a106c-113">Cuando el control deslizante **thumbImage** se mueve con el mouse, si la **diapositiva** está establecida en true, la imagen de primer plano se desliza como si lo extrajo el control deslizante para abarcar la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="a106c-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="a106c-114">Si **Slide** está establecido en false, la imagen de primer plano no se mueve, sino que se revela, como si el control deslizante fuera la imagen de fondo de la imagen de primer plano.</span><span class="sxs-lookup"><span data-stu-id="a106c-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="a106c-115">Si el atributo en **mosaico** está establecido en true y la imagen de fondo es más pequeña que el control deslizante, la imagen se organizará en mosaico horizontal o verticalmente según el atributo **Direction** .</span><span class="sxs-lookup"><span data-stu-id="a106c-115">If the **tiled** attribute is set to true and the background image is smaller than the slider control, the image will be tiled either horizontally or vertically depending on the **direction** attribute.</span></span> <span data-ttu-id="a106c-116">Si el atributo de **borde** se establece en un valor mayor que cero, el número especificado será el número de píxeles desde la izquierda, la derecha o la parte superior e inferior de la imagen (de nuevo, según el atributo de **Dirección** ) que se reservará para los bordes del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="a106c-116">If the **borderSize** attribute is set to a value greater than zero, the number specified will be the number of pixels from the left and right or top and bottom of the image (again, depending on the **direction** attribute) that will be reserved for the borders of the slider control.</span></span> <span data-ttu-id="a106c-117">En este caso, solo se usa la parte central de la imagen para colocar en mosaico el resto del control.</span><span class="sxs-lookup"><span data-stu-id="a106c-117">In this case, only the central portion of the image is used for tiling the remainder of the control.</span></span>

<span data-ttu-id="a106c-118">Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="a106c-118">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="a106c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a106c-119">Requirements</span></span>



| <span data-ttu-id="a106c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a106c-120">Requirement</span></span> | <span data-ttu-id="a106c-121">Value</span><span class="sxs-lookup"><span data-stu-id="a106c-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a106c-122">Versión</span><span class="sxs-lookup"><span data-stu-id="a106c-122">Version</span></span><br/> | <span data-ttu-id="a106c-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a106c-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a106c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a106c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a106c-125">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="a106c-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="a106c-126">**SLIDEr. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="a106c-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="a106c-127">**Control deslizante. Slide**</span><span class="sxs-lookup"><span data-stu-id="a106c-127">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="a106c-128">**SLIDEr. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="a106c-128">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> </dl>

 

 





