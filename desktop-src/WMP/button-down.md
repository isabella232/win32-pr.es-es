---
title: BOTÓN. abajo
description: El atributo Down especifica o recupera un valor que indica si el botón está en la posición arriba o abajo.
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- BOTÓN. bajar ventanas Media Player
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699766"
---
# <a name="buttondown"></a><span data-ttu-id="a0d9d-104">BOTÓN. abajo</span><span class="sxs-lookup"><span data-stu-id="a0d9d-104">BUTTON.down</span></span>

<span data-ttu-id="a0d9d-105">El atributo **Down** especifica o recupera un valor que indica si el **botón** está en la posición arriba o abajo.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-105">The **down** attribute specifies or retrieves a value indicating whether the **BUTTON** is in the up or down position.</span></span>

``` syntax
        elementID.down
```

## <a name="possible-values"></a><span data-ttu-id="a0d9d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="a0d9d-106">Possible Values</span></span>

<span data-ttu-id="a0d9d-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a0d9d-108">Value</span><span class="sxs-lookup"><span data-stu-id="a0d9d-108">Value</span></span> | <span data-ttu-id="a0d9d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0d9d-109">Description</span></span>                                                   |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="a0d9d-110">true</span><span class="sxs-lookup"><span data-stu-id="a0d9d-110">true</span></span>  | <span data-ttu-id="a0d9d-111">Indica que el **botón** está en la posición hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-111">Indicates that the **BUTTON** is in the down position.</span></span>        |
| <span data-ttu-id="a0d9d-112">false</span><span class="sxs-lookup"><span data-stu-id="a0d9d-112">false</span></span> | <span data-ttu-id="a0d9d-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-113">Default.</span></span> <span data-ttu-id="a0d9d-114">Indica que el **botón** está en la posición arriba.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-114">Indicates that the **BUTTON** is in the up position.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a0d9d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0d9d-115">Remarks</span></span>

<span data-ttu-id="a0d9d-116">Para que un **botón** permanezca en la posición hacia abajo **, se** debe establecer en true.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-116">For a **BUTTON** to remain in the down position, **sticky** must be set to true.</span></span> <span data-ttu-id="a0d9d-117">De forma predeterminada, la **permanencia** es falsa y se omitirá cualquier intento **de establecer en** true.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-117">By default, **sticky** is false, and any attempt to set **down** to true will be ignored.</span></span>

<span data-ttu-id="a0d9d-118">Si se especifica un valor no válido, se mantiene el estado anterior.</span><span class="sxs-lookup"><span data-stu-id="a0d9d-118">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0d9d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d9d-119">Requirements</span></span>



| <span data-ttu-id="a0d9d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d9d-120">Requirement</span></span> | <span data-ttu-id="a0d9d-121">Value</span><span class="sxs-lookup"><span data-stu-id="a0d9d-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a0d9d-122">Versión</span><span class="sxs-lookup"><span data-stu-id="a0d9d-122">Version</span></span><br/> | <span data-ttu-id="a0d9d-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a0d9d-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a0d9d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0d9d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d9d-125">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-125">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="a0d9d-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> <dt>

[<span data-ttu-id="a0d9d-127">**BUTTON. downToolTip**</span><span class="sxs-lookup"><span data-stu-id="a0d9d-127">**BUTTON.downToolTip**</span></span>](button-downtooltip.md)
</dt> </dl>

 

 





