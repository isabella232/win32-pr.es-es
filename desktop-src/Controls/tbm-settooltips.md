---
title: Mensaje de TBM_SETTOOLTIPS (commctrl. h)
description: Asigna un control ToolTip a un control TrackBar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- TBM_SETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489802"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="dd116-104">TBM \_ SETTOOLTIPS</span><span class="sxs-lookup"><span data-stu-id="dd116-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="dd116-105">Asigna un control ToolTip a un control TrackBar.</span><span class="sxs-lookup"><span data-stu-id="dd116-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd116-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd116-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd116-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd116-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd116-108">Identificador de un control de información sobre herramientas existente.</span><span class="sxs-lookup"><span data-stu-id="dd116-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="dd116-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd116-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd116-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd116-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd116-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd116-111">Return value</span></span>

<span data-ttu-id="dd116-112">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd116-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd116-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd116-113">Remarks</span></span>

<span data-ttu-id="dd116-114">Cuando se crea un control TrackBar con el estilo de [**\_ información sobre herramientas de TBS**](trackbar-control-styles.md) , se crea un control ToolTip predeterminado que aparece junto al control deslizante, que muestra la posición actual del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="dd116-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd116-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd116-115">Requirements</span></span>



| <span data-ttu-id="dd116-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd116-116">Requirement</span></span> | <span data-ttu-id="dd116-117">Value</span><span class="sxs-lookup"><span data-stu-id="dd116-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd116-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd116-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dd116-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd116-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd116-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd116-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dd116-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd116-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd116-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd116-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd116-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd116-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





