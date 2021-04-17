---
title: BOTÓN. permanente
description: El atributo de permanencia especifica o recupera un valor que indica si el botón es un botón de alternancia, es decir, si es un botón de dos Estados o de un solo Estado.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BOTÓN. Media Player de ventanas adhesivas
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698726"
---
# <a name="buttonsticky"></a><span data-ttu-id="3b98d-104">BOTÓN. permanente</span><span class="sxs-lookup"><span data-stu-id="3b98d-104">BUTTON.sticky</span></span>

<span data-ttu-id="3b98d-105">El atributo de **permanencia** especifica o recupera un valor que indica si el **botón** es un botón de alternancia, es decir, si es un **botón** de dos Estados o de un solo Estado.</span><span class="sxs-lookup"><span data-stu-id="3b98d-105">The **sticky** attribute specifies or retrieves a value indicating whether the **BUTTON** is a toggle, that is, whether it is a two-state or single-state **BUTTON**.</span></span>

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a><span data-ttu-id="3b98d-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="3b98d-106">Possible Values</span></span>

<span data-ttu-id="3b98d-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="3b98d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="3b98d-108">Value</span><span class="sxs-lookup"><span data-stu-id="3b98d-108">Value</span></span> | <span data-ttu-id="3b98d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b98d-109">Description</span></span>                        |
|-------|------------------------------------|
| <span data-ttu-id="3b98d-110">true</span><span class="sxs-lookup"><span data-stu-id="3b98d-110">true</span></span>  | <span data-ttu-id="3b98d-111">El **botón** es permanente.</span><span class="sxs-lookup"><span data-stu-id="3b98d-111">**BUTTON** is sticky.</span></span>              |
| <span data-ttu-id="3b98d-112">false</span><span class="sxs-lookup"><span data-stu-id="3b98d-112">false</span></span> | <span data-ttu-id="3b98d-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b98d-113">Default.</span></span> <span data-ttu-id="3b98d-114">El **botón** no es permanente.</span><span class="sxs-lookup"><span data-stu-id="3b98d-114">**BUTTON** is not sticky.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3b98d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b98d-115">Remarks</span></span>

<span data-ttu-id="3b98d-116">Si la **permanencia** está establecida en true, el **botón** cambiará al estado desactivado cuando se haga clic en él y permanecerá en ese estado hasta que se vuelva a hacer clic.</span><span class="sxs-lookup"><span data-stu-id="3b98d-116">If **sticky** is set to true, the **BUTTON** will change to the down state when clicked and will remain in that state until clicked again.</span></span> <span data-ttu-id="3b98d-117">Cuando el **botón** está en estado inactivo, el atributo **Down** será true y se mostrará el **downImage** .</span><span class="sxs-lookup"><span data-stu-id="3b98d-117">When the **BUTTON** is in the down state, the **down** attribute will be true and the **downImage** will be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b98d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b98d-118">Requirements</span></span>



| <span data-ttu-id="3b98d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b98d-119">Requirement</span></span> | <span data-ttu-id="3b98d-120">Value</span><span class="sxs-lookup"><span data-stu-id="3b98d-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3b98d-121">Versión</span><span class="sxs-lookup"><span data-stu-id="3b98d-121">Version</span></span><br/> | <span data-ttu-id="3b98d-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3b98d-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b98d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b98d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b98d-124">**Elemento BUTTON**</span><span class="sxs-lookup"><span data-stu-id="3b98d-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="3b98d-125">**BOTÓN. abajo**</span><span class="sxs-lookup"><span data-stu-id="3b98d-125">**BUTTON.down**</span></span>](button-down.md)
</dt> <dt>

[<span data-ttu-id="3b98d-126">**BUTTON. downImage**</span><span class="sxs-lookup"><span data-stu-id="3b98d-126">**BUTTON.downImage**</span></span>](button-downimage.md)
</dt> </dl>

 

 





