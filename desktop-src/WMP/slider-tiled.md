---
title: Control deslizante. en mosaico
description: El atributo en mosaico especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del control deslizante.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Control deslizante. ventanas en mosaico Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660615"
---
# <a name="slidertiled"></a><span data-ttu-id="c80fb-104">Control deslizante. en mosaico</span><span class="sxs-lookup"><span data-stu-id="c80fb-104">SLIDER.tiled</span></span>

<span data-ttu-id="c80fb-105">El atributo en **mosaico** especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="c80fb-105">The **tiled** attribute specifies or retrieves a value indicating whether the slider image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="c80fb-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="c80fb-106">Possible Values</span></span>

<span data-ttu-id="c80fb-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="c80fb-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c80fb-108">Value</span><span class="sxs-lookup"><span data-stu-id="c80fb-108">Value</span></span> | <span data-ttu-id="c80fb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c80fb-109">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80fb-110">true</span><span class="sxs-lookup"><span data-stu-id="c80fb-110">true</span></span>  | <span data-ttu-id="c80fb-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c80fb-111">Default.</span></span> <span data-ttu-id="c80fb-112">El mapa de bits de la imagen se repetirá hasta que rellene toda la región del control.</span><span class="sxs-lookup"><span data-stu-id="c80fb-112">The image bitmap will be repeated until it fills the entire region of the control.</span></span> |
| <span data-ttu-id="c80fb-113">false</span><span class="sxs-lookup"><span data-stu-id="c80fb-113">false</span></span> | <span data-ttu-id="c80fb-114">La imagen no se mostrará en mosaico.</span><span class="sxs-lookup"><span data-stu-id="c80fb-114">The image will not be tiled.</span></span>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="c80fb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c80fb-115">Remarks</span></span>

<span data-ttu-id="c80fb-116">Este atributo solo se aplica si usa imágenes de primer plano y de fondo para definir un control deslizante.</span><span class="sxs-lookup"><span data-stu-id="c80fb-116">This attribute applies only if you are using foreground and background images to define a slider control.</span></span> <span data-ttu-id="c80fb-117">Si las imágenes son más pequeñas que el área definida del control deslizante y el atributo en **mosaico** está establecido en true, las imágenes se repetirán hasta que rellenen toda la longitud del control.</span><span class="sxs-lookup"><span data-stu-id="c80fb-117">If the images are smaller than the defined area of the slider, and the **tiled** attribute is set to true, the images will be repeated until they fill the entire length of the control.</span></span>

<span data-ttu-id="c80fb-118">Puede que desee utilizar este atributo junto con el atributo de **borde** .</span><span class="sxs-lookup"><span data-stu-id="c80fb-118">You may wish to use this attribute in conjunction with the **borderSize** attribute.</span></span> <span data-ttu-id="c80fb-119">El atributo **borde** le permite definir un borde que no se repite durante el mosaico.</span><span class="sxs-lookup"><span data-stu-id="c80fb-119">The **borderSize** attribute allows you to define a border that is not repeated during tiling.</span></span>

## <a name="requirements"></a><span data-ttu-id="c80fb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c80fb-120">Requirements</span></span>



| <span data-ttu-id="c80fb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c80fb-121">Requirement</span></span> | <span data-ttu-id="c80fb-122">Value</span><span class="sxs-lookup"><span data-stu-id="c80fb-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c80fb-123">Versión</span><span class="sxs-lookup"><span data-stu-id="c80fb-123">Version</span></span><br/> | <span data-ttu-id="c80fb-124">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c80fb-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c80fb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c80fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80fb-126">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="c80fb-126">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="c80fb-127">**Control deslizante. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="c80fb-127">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="c80fb-128">**SLIDEr. Border**</span><span class="sxs-lookup"><span data-stu-id="c80fb-128">**SLIDER.borderSize**</span></span>](slider-bordersize.md)
</dt> <dt>

[<span data-ttu-id="c80fb-129">**SLIDEr. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="c80fb-129">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





