---
title: Mensaje de TCM_SETTOOLTIPS (commctrl. h)
description: Asigna un control de información sobre herramientas a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetToolTips.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801052"
---
# <a name="tcm_settooltips-message"></a><span data-ttu-id="dd14d-105">\_Mensaje SETTOOLTIPS de TCM</span><span class="sxs-lookup"><span data-stu-id="dd14d-105">TCM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="dd14d-106">Asigna un control de información sobre herramientas a un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="dd14d-106">Assigns a tooltip control to a tab control.</span></span> <span data-ttu-id="dd14d-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .</span><span class="sxs-lookup"><span data-stu-id="dd14d-107">You can send this message explicitly or by using the [**TabCtrl\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd14d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd14d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd14d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd14d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd14d-110">Identificador del control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="dd14d-110">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="dd14d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd14d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dd14d-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dd14d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd14d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd14d-113">Return value</span></span>

<span data-ttu-id="dd14d-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dd14d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd14d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd14d-115">Remarks</span></span>

<span data-ttu-id="dd14d-116">Puede recuperar el control de información sobre herramientas asociado a un control de ficha mediante el mensaje [**\_ GETTOOLTIPS de TCM**](tcm-gettooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="dd14d-116">You can retrieve the tooltip control associated with a tab control by using the [**TCM\_GETTOOLTIPS**](tcm-gettooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd14d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd14d-117">Requirements</span></span>



| <span data-ttu-id="dd14d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd14d-118">Requirement</span></span> | <span data-ttu-id="dd14d-119">Value</span><span class="sxs-lookup"><span data-stu-id="dd14d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd14d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd14d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd14d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dd14d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dd14d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd14d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd14d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd14d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd14d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd14d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd14d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd14d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





