---
title: AmbientAttributes. slideto
description: El método Slider mueve el control a una nueva ubicación. El control se mueve de forma no lineal en el período de tiempo especificado.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes. slideto Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700198"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="c1029-105">AmbientAttributes. slideto</span><span class="sxs-lookup"><span data-stu-id="c1029-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="c1029-106">El método **Slider** mueve el control a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="c1029-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="c1029-107">El control se mueve de forma no lineal en el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="c1029-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="c1029-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1029-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1029-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="c1029-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="c1029-110">**Número** (**largo**) que especifica el nuevo valor para el atributo **izquierdo** del control.</span><span class="sxs-lookup"><span data-stu-id="c1029-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="c1029-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="c1029-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="c1029-112">**Número** (**largo**) que especifica el nuevo valor para el atributo **superior** del control.</span><span class="sxs-lookup"><span data-stu-id="c1029-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="c1029-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="c1029-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="c1029-114">**Número** (**largo**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="c1029-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1029-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1029-115">Return Value</span></span>

<span data-ttu-id="c1029-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c1029-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1029-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1029-117">Remarks</span></span>

<span data-ttu-id="c1029-118">Este método es diferente de **moveTo**, que crea un movimiento lineal al mover el control.</span><span class="sxs-lookup"><span data-stu-id="c1029-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="c1029-119">El movimiento no lineal creado por este método es un movimiento deslizante que se acelera a partir de una velocidad de cero al principio del movimiento y se ralentiza a cero al final, lo que llega a una parada suave.</span><span class="sxs-lookup"><span data-stu-id="c1029-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1029-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1029-120">Requirements</span></span>



| <span data-ttu-id="c1029-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1029-121">Requirement</span></span> | <span data-ttu-id="c1029-122">Value</span><span class="sxs-lookup"><span data-stu-id="c1029-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="c1029-123">Versión</span><span class="sxs-lookup"><span data-stu-id="c1029-123">Version</span></span><br/> | <span data-ttu-id="c1029-124">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c1029-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1029-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1029-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1029-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="c1029-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1029-127">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="c1029-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="c1029-128">**AmbientAttributes. moveTo**</span><span class="sxs-lookup"><span data-stu-id="c1029-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="c1029-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="c1029-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





