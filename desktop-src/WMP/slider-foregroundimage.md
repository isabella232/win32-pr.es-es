---
title: SLIDEr. foregroundImage
description: El atributo foregroundImage especifica o recupera la imagen de primer plano del control deslizante.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- CONTROL SLIDEr. foregroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661191"
---
# <a name="sliderforegroundimage"></a><span data-ttu-id="ad795-104">SLIDEr. foregroundImage</span><span class="sxs-lookup"><span data-stu-id="ad795-104">SLIDER.foregroundImage</span></span>

<span data-ttu-id="ad795-105">El atributo **foregroundImage** especifica o recupera la imagen de primer plano del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="ad795-105">The **foregroundImage** attribute specifies or retrieves the foreground image of the slider.</span></span>

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a><span data-ttu-id="ad795-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="ad795-106">Possible Values</span></span>

<span data-ttu-id="ad795-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="ad795-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad795-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ad795-108">Remarks</span></span>

<span data-ttu-id="ad795-109">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="ad795-109">This attribute is optional.</span></span> <span data-ttu-id="ad795-110">Al usar imágenes para construir un control deslizante, la **BackgroundImage** se usa para la imagen del control deslizante principal.</span><span class="sxs-lookup"><span data-stu-id="ad795-110">When using images to construct a slider control, the **backgroundImage** is used for the main slider image.</span></span> <span data-ttu-id="ad795-111">**ThumbImage** representa el control deslizante real y se puede desplazar mediante el mouse.</span><span class="sxs-lookup"><span data-stu-id="ad795-111">The **thumbImage** represents the actual slider and can be moved using the mouse.</span></span> <span data-ttu-id="ad795-112">En el control deslizante **thumbImage** hay una línea invisible en la que se muestra la imagen de fondo en un lado de la línea y la imagen de primer plano se muestra en el otro lado.</span><span class="sxs-lookup"><span data-stu-id="ad795-112">At the **thumbImage** slider there is an invisible line where the background image is displayed on one side of the line, and the foreground image is displayed on the other side.</span></span>

<span data-ttu-id="ad795-113">Cuando el control deslizante **thumbImage** se mueve con el mouse, si la **diapositiva** está establecida en true, la imagen de primer plano se desliza como si lo extrajo el control deslizante para abarcar la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="ad795-113">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="ad795-114">Si **Slide** está establecido en false, la imagen de primer plano no se mueve, sino que se revela, como si el control deslizante fuera la imagen de fondo de la imagen de primer plano.</span><span class="sxs-lookup"><span data-stu-id="ad795-114">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

<span data-ttu-id="ad795-115">Si el atributo en **mosaico** está establecido en true y la imagen de primer plano es menor que el área de primer plano del control deslizante, la imagen se organizará en mosaico horizontal o verticalmente, según el atributo **Direction** , para rellenar el espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="ad795-115">If the **tiled** attribute is set to true and the foreground image is smaller than the foreground area of the slider control, the image will be tiled either horizontally or vertically, depending on the **direction** attribute, to fill the available space.</span></span>

<span data-ttu-id="ad795-116">Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="ad795-116">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad795-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad795-117">Requirements</span></span>



| <span data-ttu-id="ad795-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad795-118">Requirement</span></span> | <span data-ttu-id="ad795-119">Value</span><span class="sxs-lookup"><span data-stu-id="ad795-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ad795-120">Versión</span><span class="sxs-lookup"><span data-stu-id="ad795-120">Version</span></span><br/> | <span data-ttu-id="ad795-121">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ad795-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad795-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad795-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad795-123">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="ad795-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="ad795-124">**Control deslizante. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="ad795-124">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="ad795-125">**Control deslizante. Slide**</span><span class="sxs-lookup"><span data-stu-id="ad795-125">**SLIDER.slide**</span></span>](slider-slide.md)
</dt> <dt>

[<span data-ttu-id="ad795-126">**SLIDEr. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="ad795-126">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="ad795-127">**Control deslizante. valor**</span><span class="sxs-lookup"><span data-stu-id="ad795-127">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





