---
title: AmbientAttributes.moveSizeTo
description: El método moveSizeTo mueve el control y especifica un nuevo tamaño para el control en la nueva ubicación. El control se mueve y cambia de tamaño de manera animada en el período de tiempo especificado.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes. moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699434"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="0a1b3-105">AmbientAttributes.moveSizeTo</span><span class="sxs-lookup"><span data-stu-id="0a1b3-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="0a1b3-106">El método **moveSizeTo** mueve el control y especifica un nuevo tamaño para el control en la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="0a1b3-107">El control se mueve y cambia de tamaño de manera animada en el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="0a1b3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a1b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a1b3-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="0a1b3-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="0a1b3-110">**Número** (**largo**) que especifica el nuevo valor para el atributo **izquierdo** del control.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0a1b3-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="0a1b3-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="0a1b3-112">**Número** (**largo**) que especifica el nuevo valor para el atributo **superior** del control.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0a1b3-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span><span class="sxs-lookup"><span data-stu-id="0a1b3-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="0a1b3-114">**Número** (**largo**) que especifica el nuevo valor para el atributo de **ancho** del control.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0a1b3-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span><span class="sxs-lookup"><span data-stu-id="0a1b3-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="0a1b3-116">**Número** (**largo**) que especifica el nuevo valor para el atributo de **alto** del control.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="0a1b3-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="0a1b3-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="0a1b3-118">**Número** (**largo**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="0a1b3-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span><span class="sxs-lookup"><span data-stu-id="0a1b3-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="0a1b3-120">**Valor booleano** que especifica el tipo de movimiento que se crea al mover el control.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="0a1b3-121">Value</span><span class="sxs-lookup"><span data-stu-id="0a1b3-121">Value</span></span> | <span data-ttu-id="0a1b3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a1b3-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="0a1b3-123">true</span><span class="sxs-lookup"><span data-stu-id="0a1b3-123">true</span></span>  | <span data-ttu-id="0a1b3-124">El movimiento no es lineal (movimiento deslizante que acelera y desacelera).</span><span class="sxs-lookup"><span data-stu-id="0a1b3-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="0a1b3-125">false</span><span class="sxs-lookup"><span data-stu-id="0a1b3-125">false</span></span> | <span data-ttu-id="0a1b3-126">El movimiento es lineal.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a1b3-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a1b3-127">Return Value</span></span>

<span data-ttu-id="0a1b3-128">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a1b3-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a1b3-129">Remarks</span></span>

<span data-ttu-id="0a1b3-130">El movimiento del control puede ser lineal o no lineal.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="0a1b3-131">Movimiento lineal significa que el control se mueve a una velocidad constante a su nueva ubicación, desde el inicio y la detención brusca.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="0a1b3-132">Cuando se especifica un movimiento no lineal, se crea un movimiento deslizante que se acelera desde cero al principio del movimiento y se ralentiza hasta cero al final, lo que llega a una parada suave.</span><span class="sxs-lookup"><span data-stu-id="0a1b3-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a1b3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a1b3-133">Requirements</span></span>



| <span data-ttu-id="0a1b3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a1b3-134">Requirement</span></span> | <span data-ttu-id="0a1b3-135">Value</span><span class="sxs-lookup"><span data-stu-id="0a1b3-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="0a1b3-136">Versión</span><span class="sxs-lookup"><span data-stu-id="0a1b3-136">Version</span></span><br/> | <span data-ttu-id="0a1b3-137">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="0a1b3-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a1b3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a1b3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a1b3-139">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="0a1b3-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="0a1b3-140">**AmbientAttributes. Height**</span><span class="sxs-lookup"><span data-stu-id="0a1b3-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="0a1b3-141">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="0a1b3-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="0a1b3-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="0a1b3-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="0a1b3-143">**AmbientAttributes. width**</span><span class="sxs-lookup"><span data-stu-id="0a1b3-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





