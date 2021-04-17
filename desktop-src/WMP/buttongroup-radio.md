---
title: BUTTONGROUP. radio
description: El atributo de radio especifica o recupera un valor que indica si BUTTONGROUP se compone de botones de radio.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP. radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699946"
---
# <a name="buttongroupradio"></a><span data-ttu-id="866b2-104">BUTTONGROUP. radio</span><span class="sxs-lookup"><span data-stu-id="866b2-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="866b2-105">El atributo de **radio** especifica o recupera un valor que indica si **BUTTONGROUP** se compone de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="866b2-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="866b2-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="866b2-106">Possible Values</span></span>

<span data-ttu-id="866b2-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="866b2-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="866b2-108">Value</span><span class="sxs-lookup"><span data-stu-id="866b2-108">Value</span></span> | <span data-ttu-id="866b2-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="866b2-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="866b2-110">true</span><span class="sxs-lookup"><span data-stu-id="866b2-110">true</span></span>  | <span data-ttu-id="866b2-111">**BUTTONGROUP** es el estilo de radio.</span><span class="sxs-lookup"><span data-stu-id="866b2-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="866b2-112">false</span><span class="sxs-lookup"><span data-stu-id="866b2-112">false</span></span> | <span data-ttu-id="866b2-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="866b2-113">Default.</span></span> <span data-ttu-id="866b2-114">**BUTTONGROUP** no es el estilo de radio.</span><span class="sxs-lookup"><span data-stu-id="866b2-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="866b2-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="866b2-115">Remarks</span></span>

<span data-ttu-id="866b2-116">Si el valor de **radio** está establecido en true, todos los elementos **BUTTONELEMENT** del **BUTTONGROUP** serán persistentes, pero solo un botón a la vez estará en estado desactivado.</span><span class="sxs-lookup"><span data-stu-id="866b2-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="866b2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="866b2-117">Requirements</span></span>



| <span data-ttu-id="866b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="866b2-118">Requirement</span></span> | <span data-ttu-id="866b2-119">Value</span><span class="sxs-lookup"><span data-stu-id="866b2-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="866b2-120">Versión</span><span class="sxs-lookup"><span data-stu-id="866b2-120">Version</span></span><br/> | <span data-ttu-id="866b2-121">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="866b2-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="866b2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="866b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866b2-123">**BUTTONELEMENT. adhesiva**</span><span class="sxs-lookup"><span data-stu-id="866b2-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="866b2-124">**Elemento BUTTONGROUP**</span><span class="sxs-lookup"><span data-stu-id="866b2-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





