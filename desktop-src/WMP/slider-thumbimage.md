---
title: SLIDEr. thumbImage
description: El atributo thumbImage especifica o recupera la imagen que se utilizará para representar la posición actual del control deslizante.
ms.assetid: 3aa69188-3443-483c-81a9-bf22832509d8
keywords:
- CONTROL SLIDEr. thumbImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.thumbImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b798dfbae24fe2cef3669d2fb372966e47254026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700103"
---
# <a name="sliderthumbimage"></a><span data-ttu-id="48ae8-104">SLIDEr. thumbImage</span><span class="sxs-lookup"><span data-stu-id="48ae8-104">SLIDER.thumbImage</span></span>

<span data-ttu-id="48ae8-105">El atributo **thumbImage** especifica o recupera la imagen que se utilizará para representar la posición actual del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="48ae8-105">The **thumbImage** attribute specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>

``` syntax
        elementID.thumbImage
```

## <a name="possible-values"></a><span data-ttu-id="48ae8-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="48ae8-106">Possible Values</span></span>

<span data-ttu-id="48ae8-107">Este atributo es una **cadena** de lectura/escritura que contiene el nombre de un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="48ae8-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="48ae8-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48ae8-108">Remarks</span></span>

<span data-ttu-id="48ae8-109">**ThumbImage** especifica la imagen que se usará para representar la posición actual, así como el modo de indicar que el usuario puede realizar una acción con el control.</span><span class="sxs-lookup"><span data-stu-id="48ae8-109">The **thumbImage** specifies the image that will be used to represent current position, as well as indicate that the user can take action with the control.</span></span> <span data-ttu-id="48ae8-110">Si no se especifica ninguna imagen Thumb, el control deslizante no es interactivo.</span><span class="sxs-lookup"><span data-stu-id="48ae8-110">If no thumb image is specified, the slider is non-interactive.</span></span>

<span data-ttu-id="48ae8-111">La imagen Thumb está centrada en la dimensión estrecha del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="48ae8-111">The thumb image is centered in the narrow dimension of the slider control.</span></span> <span data-ttu-id="48ae8-112">Si la imagen Thumb es más estrecha que el control, la imagen aparece en medio del fondo.</span><span class="sxs-lookup"><span data-stu-id="48ae8-112">If the thumb image is narrower than the control, the image appears in the middle of the background.</span></span> <span data-ttu-id="48ae8-113">Si la imagen de Thumb es mayor que el control, los extremos de la imagen se cortan.</span><span class="sxs-lookup"><span data-stu-id="48ae8-113">If the thumb image is larger than the control, the ends of the image are cut off.</span></span>

<span data-ttu-id="48ae8-114">La posición del control deslizante se especifica mediante el centro de la imagen de Thumb.</span><span class="sxs-lookup"><span data-stu-id="48ae8-114">The position of the slider is specified by the center of the thumb image.</span></span> <span data-ttu-id="48ae8-115">Si el valor de **borde** es cero, solo la mitad de la imagen Thumb estará visible en las posiciones del control deslizante inicial y final.</span><span class="sxs-lookup"><span data-stu-id="48ae8-115">If **borderSize** is zero, only half the thumb image will be visible at the beginning and end slider positions.</span></span> <span data-ttu-id="48ae8-116">Para evitarlo, establezca el valor de **borde** en un valor mayor o igual que la mitad del ancho de la imagen de control de posición (o la mitad del alto si la **Dirección** está establecida en "vertical").</span><span class="sxs-lookup"><span data-stu-id="48ae8-116">To prevent this, set **borderSize** to a value greater than or equal to half the width of the thumb image (or half the height if **direction** is set to "vertical").</span></span>

<span data-ttu-id="48ae8-117">Los formatos admitidos son BMP, JPG, PNG y GIF (sin incluir los GIF animados).</span><span class="sxs-lookup"><span data-stu-id="48ae8-117">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

<span data-ttu-id="48ae8-118">Vea **CUSTOMSLIDER**. atributo [positionImage](customslider-positionimage.md) para un ejemplo que muestra cómo se utilizan los atributos del elemento **Slider** .</span><span class="sxs-lookup"><span data-stu-id="48ae8-118">See the **CUSTOMSLIDER**.[positionImage](customslider-positionimage.md) attribute for a sample illustrating how the attributes of the **SLIDER** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="48ae8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48ae8-119">Requirements</span></span>



| <span data-ttu-id="48ae8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48ae8-120">Requirement</span></span> | <span data-ttu-id="48ae8-121">Value</span><span class="sxs-lookup"><span data-stu-id="48ae8-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="48ae8-122">Versión</span><span class="sxs-lookup"><span data-stu-id="48ae8-122">Version</span></span><br/> | <span data-ttu-id="48ae8-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="48ae8-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48ae8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="48ae8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48ae8-125">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="48ae8-125">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="48ae8-126">**SLIDEr. Border**</span><span class="sxs-lookup"><span data-stu-id="48ae8-126">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="48ae8-127">**Control deslizante. Direction**</span><span class="sxs-lookup"><span data-stu-id="48ae8-127">**SLIDER.direction**</span></span>](slider-direction.md)
</dt> </dl>

 

 





