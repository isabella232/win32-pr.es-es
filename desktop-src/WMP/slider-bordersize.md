---
title: SLIDEr. Border
description: El atributo de borde especifica o recupera el ancho del borde en píxeles.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Control deslizante. bordes de Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660896"
---
# <a name="sliderbordersize"></a><span data-ttu-id="94ad4-104">SLIDEr. Border</span><span class="sxs-lookup"><span data-stu-id="94ad4-104">SLIDER.borderSize</span></span>

<span data-ttu-id="94ad4-105">El atributo de **borde** especifica o recupera el ancho del borde en píxeles.</span><span class="sxs-lookup"><span data-stu-id="94ad4-105">The **borderSize** attribute specifies or retrieves the border width in pixels.</span></span>

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a><span data-ttu-id="94ad4-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="94ad4-106">Possible Values</span></span>

<span data-ttu-id="94ad4-107">Este atributo es un **número** de lectura y escritura (**Long**) que representa el ancho del borde en píxeles.</span><span class="sxs-lookup"><span data-stu-id="94ad4-107">This attribute is a read/write **Number** (**long**) representing the border width in pixels.</span></span> <span data-ttu-id="94ad4-108">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="94ad4-108">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="94ad4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94ad4-109">Remarks</span></span>

<span data-ttu-id="94ad4-110">Este atributo define un desplazamiento desde el principio y el final del control deslizante que es, desde la izquierda y la derecha si el atributo **Direction** se establece en "horizontal" y desde la parte superior e inferior si se establece en "vertical".</span><span class="sxs-lookup"><span data-stu-id="94ad4-110">This attribute defines an offset from the beginning and end of the slider control that is, from the left and right if the **direction** attribute is set to "horizontal", and from the top and bottom if it is set to "vertical".</span></span> <span data-ttu-id="94ad4-111">Estas posiciones de desplazamiento dictan las posiciones mínima y máxima del control deslizante, más allá del que no se aplicará el color de primer plano o la imagen.</span><span class="sxs-lookup"><span data-stu-id="94ad4-111">These offset positions dictate the minimum and maximum positions of the slider thumb, beyond which the foreground color or image will not be applied.</span></span>

<span data-ttu-id="94ad4-112">Si se usa una imagen de fondo con el atributo en **mosaico** establecido en true, el desplazamiento se aplica a la imagen, lo que indica la cantidad de la imagen (desde la izquierda y la derecha o desde la parte superior e inferior) que se va a usar para los bordes inicial y final del control deslizante, con la parte central de la imagen que se coloca en mosaico en el resto.</span><span class="sxs-lookup"><span data-stu-id="94ad4-112">If a background image is used with the **tiled** attribute set to true, the offset is applied to the image, dictating the amount of the image (either from the left and right or from the top and bottom) to be used for the beginning and end borders of the slider control, with the central portion of the image being tiled throughout the remainder.</span></span> <span data-ttu-id="94ad4-113">De esta manera, se puede usar una imagen de fondo pequeña para cubrir la longitud total de un control deslizante más grande.</span><span class="sxs-lookup"><span data-stu-id="94ad4-113">In this way, a small background image can be used to cover the full length of a larger slider control.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ad4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94ad4-114">Requirements</span></span>



| <span data-ttu-id="94ad4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ad4-115">Requirement</span></span> | <span data-ttu-id="94ad4-116">Value</span><span class="sxs-lookup"><span data-stu-id="94ad4-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="94ad4-117">Versión</span><span class="sxs-lookup"><span data-stu-id="94ad4-117">Version</span></span><br/> | <span data-ttu-id="94ad4-118">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="94ad4-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94ad4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="94ad4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ad4-120">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="94ad4-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="94ad4-121">**SLIDEr. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="94ad4-121">**SLIDER.foregroundColor**</span></span>](slider-foregroundcolor.md)
</dt> <dt>

[<span data-ttu-id="94ad4-122">**SLIDEr. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="94ad4-122">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> <dt>

[<span data-ttu-id="94ad4-123">**SLIDEr. thumbImage**</span><span class="sxs-lookup"><span data-stu-id="94ad4-123">**SLIDER.thumbImage**</span></span>](slider-thumbimage.md)
</dt> <dt>

[<span data-ttu-id="94ad4-124">**Control deslizante. en mosaico**</span><span class="sxs-lookup"><span data-stu-id="94ad4-124">**SLIDER.tiled**</span></span>](slider-tiled.md)
</dt> </dl>

 

 





