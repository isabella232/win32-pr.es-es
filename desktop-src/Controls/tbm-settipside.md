---
title: Mensaje de TBM_SETTIPSIDE (commctrl. h)
description: Coloca un control ToolTip utilizado por un control TrackBar. Los controles de barra de control que usan el estilo información sobre herramientas de TBS \_ muestran información sobre herramientas.
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- TBM_SETTIPSIDE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422115"
---
# <a name="tbm_settipside-message"></a><span data-ttu-id="e9ae0-105">TBM \_ SETTIPSIDE</span><span class="sxs-lookup"><span data-stu-id="e9ae0-105">TBM\_SETTIPSIDE message</span></span>

<span data-ttu-id="e9ae0-106">Coloca un control ToolTip utilizado por un control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-106">Positions a tooltip control used by a trackbar control.</span></span> <span data-ttu-id="e9ae0-107">Los controles de barra de control que usan el estilo [**\_ información**](trackbar-control-styles.md) sobre herramientas de TBS muestran información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-107">Trackbar controls that use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style display tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9ae0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9ae0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ae0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9ae0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ae0-110">Valor que representa la ubicación en la que se va a mostrar el control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-110">Value representing the location at which to display the tooltip control.</span></span> <span data-ttu-id="e9ae0-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e9ae0-111">This value can be one of the following:</span></span>



| <span data-ttu-id="e9ae0-112">Value</span><span class="sxs-lookup"><span data-stu-id="e9ae0-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="e9ae0-113">Significado</span><span class="sxs-lookup"><span data-stu-id="e9ae0-113">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <span data-ttu-id="e9ae0-114"><dt>**TBTS \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-114"><dt>**TBTS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="e9ae0-115">El control ToolTip se colocará sobre la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-115">The tooltip control will be positioned above the trackbar.</span></span> <span data-ttu-id="e9ae0-116">Esta marca se usa con trackbars horizontal.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-116">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <span data-ttu-id="e9ae0-117"><dt>**TBTS a la \_ izquierda**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-117"><dt>**TBTS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="e9ae0-118">El control ToolTip se colocará a la izquierda de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-118">The tooltip control will be positioned to the left of the trackbar.</span></span> <span data-ttu-id="e9ae0-119">Esta marca se usa con trackbars vertical.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-119">This flag is for use with vertical trackbars.</span></span><br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <span data-ttu-id="e9ae0-120"><dt>**TBTS \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-120"><dt>**TBTS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="e9ae0-121">El control ToolTip se colocará debajo de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-121">The tooltip control will be positioned below the trackbar.</span></span> <span data-ttu-id="e9ae0-122">Esta marca se usa con trackbars horizontal.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-122">This flag is for use with horizontal trackbars.</span></span><br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <span data-ttu-id="e9ae0-123"><dt>**TBTS \_ derecha**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-123"><dt>**TBTS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="e9ae0-124">El control ToolTip se colocará a la derecha de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-124">The tooltip control will be positioned to the right of the trackbar.</span></span> <span data-ttu-id="e9ae0-125">Esta marca se usa con trackbars vertical.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-125">This flag is for use with vertical trackbars.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e9ae0-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9ae0-126">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e9ae0-127">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-127">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ae0-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9ae0-128">Return value</span></span>

<span data-ttu-id="e9ae0-129">Devuelve un valor que representa la ubicación anterior del control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-129">Returns a value that represents the tooltip control's previous location.</span></span> <span data-ttu-id="e9ae0-130">El valor devuelto es igual a uno de los valores posibles de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="e9ae0-130">The return value equals one of the possible values for *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ae0-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ae0-131">Requirements</span></span>



| <span data-ttu-id="e9ae0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ae0-132">Requirement</span></span> | <span data-ttu-id="e9ae0-133">Value</span><span class="sxs-lookup"><span data-stu-id="e9ae0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ae0-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9ae0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ae0-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9ae0-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9ae0-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9ae0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ae0-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9ae0-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9ae0-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9ae0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ae0-139"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae0-139"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





