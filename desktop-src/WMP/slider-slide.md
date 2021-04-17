---
title: Control deslizante. Slide
description: El atributo de diapositiva especifica o recupera un valor que indica si la imagen de primer plano se desplaza sobre la imagen de fondo o se revela gradualmente en una posición estática sobre la imagen de fondo.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Control deslizante. Slide Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660999"
---
# <a name="sliderslide"></a><span data-ttu-id="6c18a-104">Control deslizante. Slide</span><span class="sxs-lookup"><span data-stu-id="6c18a-104">SLIDER.slide</span></span>

<span data-ttu-id="6c18a-105">El atributo de **diapositiva** especifica o recupera un valor que indica si la imagen de primer plano se desplaza sobre la imagen de fondo o se revela gradualmente en una posición estática sobre la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="6c18a-105">The **slide** attribute specifies or retrieves a value indicating whether the foreground image slides over the background image or is gradually revealed in a static position over the background image.</span></span>

``` syntax
        elementID.slide
```

## <a name="possible-values"></a><span data-ttu-id="6c18a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6c18a-106">Possible Values</span></span>

<span data-ttu-id="6c18a-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="6c18a-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="6c18a-108">Value</span><span class="sxs-lookup"><span data-stu-id="6c18a-108">Value</span></span> | <span data-ttu-id="6c18a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c18a-109">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="6c18a-110">true</span><span class="sxs-lookup"><span data-stu-id="6c18a-110">true</span></span>  | <span data-ttu-id="6c18a-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6c18a-111">Default.</span></span> <span data-ttu-id="6c18a-112">La imagen de primer plano se desliza sobre la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="6c18a-112">The foreground image slides over the background image.</span></span>      |
| <span data-ttu-id="6c18a-113">false</span><span class="sxs-lookup"><span data-stu-id="6c18a-113">false</span></span> | <span data-ttu-id="6c18a-114">La imagen de primer plano se revela en el lugar de la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="6c18a-114">The foreground image is revealed in place over the background image.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c18a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c18a-115">Remarks</span></span>

<span data-ttu-id="6c18a-116">Cuando el control deslizante **thumbImage** se mueve con el mouse, si la **diapositiva** está establecida en true, la imagen de primer plano se desliza como si lo extrajo el control deslizante para abarcar la imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="6c18a-116">When the **thumbImage** slider is moved with the mouse, if **slide** is set to true, the foreground image slides along as if being pulled by the slider to cover the background image.</span></span> <span data-ttu-id="6c18a-117">Si **Slide** está establecido en false, la imagen de primer plano no se mueve, sino que se revela, como si el control deslizante fuera la imagen de fondo de la imagen de primer plano.</span><span class="sxs-lookup"><span data-stu-id="6c18a-117">If **slide** is set to false, the foreground image does not move, but is revealed in place, as if the slider is moving the background image off the foreground image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c18a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c18a-118">Requirements</span></span>



| <span data-ttu-id="6c18a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c18a-119">Requirement</span></span> | <span data-ttu-id="6c18a-120">Value</span><span class="sxs-lookup"><span data-stu-id="6c18a-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6c18a-121">Versión</span><span class="sxs-lookup"><span data-stu-id="6c18a-121">Version</span></span><br/> | <span data-ttu-id="6c18a-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="6c18a-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c18a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c18a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c18a-124">**Elemento SLIDEr**</span><span class="sxs-lookup"><span data-stu-id="6c18a-124">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="6c18a-125">**Control deslizante. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="6c18a-125">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> <dt>

[<span data-ttu-id="6c18a-126">**SLIDEr. foregroundImage**</span><span class="sxs-lookup"><span data-stu-id="6c18a-126">**SLIDER.foregroundImage**</span></span>](slider-foregroundimage.md)
</dt> </dl>

 

 





