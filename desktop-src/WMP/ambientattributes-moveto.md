---
title: AmbientAttributes. moveTo
description: El método moveTo mueve el control a una nueva ubicación en una velocidad lineal.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes. moveTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699581"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="e6521-104">AmbientAttributes. moveTo</span><span class="sxs-lookup"><span data-stu-id="e6521-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="e6521-105">El método **moveTo** mueve el control a una nueva ubicación en una velocidad lineal.</span><span class="sxs-lookup"><span data-stu-id="e6521-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="e6521-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6521-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6521-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span><span class="sxs-lookup"><span data-stu-id="e6521-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="e6521-108">**Número** (**largo**) que especifica el nuevo valor para el atributo **izquierdo** del control.</span><span class="sxs-lookup"><span data-stu-id="e6521-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="e6521-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span><span class="sxs-lookup"><span data-stu-id="e6521-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="e6521-110">**Número** (**largo**) que especifica el nuevo valor para el atributo **superior** del control.</span><span class="sxs-lookup"><span data-stu-id="e6521-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="e6521-111"><span id="time"></span><span id="TIME"></span>*tiempo*</span><span class="sxs-lookup"><span data-stu-id="e6521-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="e6521-112">**Número** (**largo**) que especifica el tiempo, en milisegundos, que tarda el control en moverse a su nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="e6521-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6521-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6521-113">Return Value</span></span>

<span data-ttu-id="e6521-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6521-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6521-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6521-115">Remarks</span></span>

<span data-ttu-id="e6521-116">Este método es útil para los elementos de la **subvista** animada (por ejemplo, si el usuario hace clic en una bandeja y los controles se deslizan hacia abajo).</span><span class="sxs-lookup"><span data-stu-id="e6521-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="e6521-117">Este método crea un movimiento lineal al mover el control.</span><span class="sxs-lookup"><span data-stu-id="e6521-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="e6521-118">Esto difiere de **Slider**, que crea un movimiento no lineal.</span><span class="sxs-lookup"><span data-stu-id="e6521-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6521-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6521-119">Requirements</span></span>



| <span data-ttu-id="e6521-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6521-120">Requirement</span></span> | <span data-ttu-id="e6521-121">Value</span><span class="sxs-lookup"><span data-stu-id="e6521-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e6521-122">Versión</span><span class="sxs-lookup"><span data-stu-id="e6521-122">Version</span></span><br/> | <span data-ttu-id="e6521-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e6521-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6521-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6521-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6521-125">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="e6521-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="e6521-126">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="e6521-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="e6521-127">**AmbientAttributes. slideto**</span><span class="sxs-lookup"><span data-stu-id="e6521-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="e6521-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="e6521-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





