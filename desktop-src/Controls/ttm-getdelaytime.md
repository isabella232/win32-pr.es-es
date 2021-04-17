---
title: Mensaje de TTM_GETDELAYTIME (commctrl. h)
description: Recupera las duraciones iniciales, emergentes y de visualización que se establecen actualmente para un control ToolTip.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658191"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="f52e7-104">TTM \_ GETDELAYTIME</span><span class="sxs-lookup"><span data-stu-id="f52e7-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="f52e7-105">Recupera las duraciones iniciales, emergentes y de visualización que se establecen actualmente para un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="f52e7-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f52e7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f52e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52e7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f52e7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f52e7-108">Marca que especifica el valor de duración que se recuperará.</span><span class="sxs-lookup"><span data-stu-id="f52e7-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="f52e7-109">Este parámetro puede tener uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="f52e7-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="f52e7-110">Value</span><span class="sxs-lookup"><span data-stu-id="f52e7-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="f52e7-111">Significado</span><span class="sxs-lookup"><span data-stu-id="f52e7-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="f52e7-112"><dt>**TTDT \_ AUTOPOP**</dt></span><span class="sxs-lookup"><span data-stu-id="f52e7-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="f52e7-113">Recupera la cantidad de tiempo que la ventana de información sobre herramientas permanece visible si el puntero es estacionario dentro del rectángulo delimitador de una herramienta.</span><span class="sxs-lookup"><span data-stu-id="f52e7-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="f52e7-114"><dt>**TTDT \_ inicial**</dt></span><span class="sxs-lookup"><span data-stu-id="f52e7-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="f52e7-115">Recupera la cantidad de tiempo que el puntero debe permanecer estacionario dentro del rectángulo delimitador de una herramienta antes de que aparezca la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="f52e7-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="f52e7-116"><dt>**TTDT \_ Mostrar**</dt></span><span class="sxs-lookup"><span data-stu-id="f52e7-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="f52e7-117">Recupere la cantidad de tiempo que se tarda en aparecer la siguiente ventana de información sobre herramientas cuando el puntero se desplaza de una herramienta a otra.</span><span class="sxs-lookup"><span data-stu-id="f52e7-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="f52e7-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f52e7-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f52e7-119">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f52e7-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52e7-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f52e7-120">Return value</span></span>

<span data-ttu-id="f52e7-121">Devuelve e INT con la duración especificada en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="f52e7-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52e7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52e7-122">Requirements</span></span>



| <span data-ttu-id="f52e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52e7-123">Requirement</span></span> | <span data-ttu-id="f52e7-124">Value</span><span class="sxs-lookup"><span data-stu-id="f52e7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f52e7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52e7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f52e7-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f52e7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f52e7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52e7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f52e7-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f52e7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f52e7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f52e7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52e7-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52e7-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f52e7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f52e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52e7-132">**TTM \_ SETDELAYTIME**</span><span class="sxs-lookup"><span data-stu-id="f52e7-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





