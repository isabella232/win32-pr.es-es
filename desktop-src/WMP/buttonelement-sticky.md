---
title: BUTTONELEMENT. adhesiva
description: El atributo de permanencia especifica o recupera un valor que indica si BUTTONELEMENT es un botón de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONELEMENT. Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699800"
---
# <a name="buttonelementsticky"></a><span data-ttu-id="396d1-104">BUTTONELEMENT. adhesiva</span><span class="sxs-lookup"><span data-stu-id="396d1-104">BUTTONELEMENT.sticky</span></span>

<span data-ttu-id="396d1-105">El atributo de **permanencia** especifica o recupera un valor que indica si **BUTTONELEMENT** es un botón de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.</span><span class="sxs-lookup"><span data-stu-id="396d1-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTONELEMENT** is a toggle, that is, whether it is a two-state or single-state button.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="396d1-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="396d1-106">Possible Values</span></span>

<span data-ttu-id="396d1-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="396d1-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="396d1-108">Value</span><span class="sxs-lookup"><span data-stu-id="396d1-108">Value</span></span> | <span data-ttu-id="396d1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="396d1-109">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="396d1-110">true</span><span class="sxs-lookup"><span data-stu-id="396d1-110">true</span></span>  | <span data-ttu-id="396d1-111">**BUTTONELEMENT** es permanente.</span><span class="sxs-lookup"><span data-stu-id="396d1-111">**BUTTONELEMENT** is sticky.</span></span>              |
| <span data-ttu-id="396d1-112">false</span><span class="sxs-lookup"><span data-stu-id="396d1-112">false</span></span> | <span data-ttu-id="396d1-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="396d1-113">Default.</span></span> <span data-ttu-id="396d1-114">**BUTTONELEMENT** no es permanente.</span><span class="sxs-lookup"><span data-stu-id="396d1-114">**BUTTONELEMENT** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="396d1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="396d1-115">Remarks</span></span>

<span data-ttu-id="396d1-116">Si el atributo de **permanencia** está establecido en true, el elemento de botón cambiará al estado desactivado cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic.</span><span class="sxs-lookup"><span data-stu-id="396d1-116">If the **sticky** attribute is set to true, the button element will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="396d1-117">Cuando el elemento de botón está inactivo, el atributo **Down** será true y se mostrará la parte adecuada del grupo de botones **downImage** .</span><span class="sxs-lookup"><span data-stu-id="396d1-117">When the button element is in the down state, the **down** attribute will be true and the appropriate portion of the button group **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="396d1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="396d1-118">Requirements</span></span>



| <span data-ttu-id="396d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="396d1-119">Requirement</span></span> | <span data-ttu-id="396d1-120">Value</span><span class="sxs-lookup"><span data-stu-id="396d1-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="396d1-121">Versión</span><span class="sxs-lookup"><span data-stu-id="396d1-121">Version</span></span><br/> | <span data-ttu-id="396d1-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="396d1-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="396d1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="396d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396d1-124">**BUTTONELEMENT (elemento)**</span><span class="sxs-lookup"><span data-stu-id="396d1-124">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="396d1-125">**BUTTONELEMENT. Down**</span><span class="sxs-lookup"><span data-stu-id="396d1-125">**BUTTONELEMENT.down**</span></span>](buttonelement-down.md)
</dt> <dt>

[<span data-ttu-id="396d1-126">**BUTTONGROUP.downImage**</span><span class="sxs-lookup"><span data-stu-id="396d1-126">**BUTTONGROUP.downImage**</span></span>](buttongroup-downimage.md)
</dt> </dl>

 

 





