---
title: Mensaje de TCM_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador del control de información sobre herramientas asociado a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150971"
---
# <a name="tcm_gettooltips-message"></a><span data-ttu-id="b3486-105">\_Mensaje GETTOOLTIPS de TCM</span><span class="sxs-lookup"><span data-stu-id="b3486-105">TCM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="b3486-106">Recupera el identificador del control de información sobre herramientas asociado a un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="b3486-106">Retrieves the handle to the tooltip control associated with a tab control.</span></span> <span data-ttu-id="b3486-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .</span><span class="sxs-lookup"><span data-stu-id="b3486-107">You can send this message explicitly or by using the [**TabCtrl\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3486-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3486-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3486-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3486-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3486-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b3486-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3486-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3486-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b3486-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b3486-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3486-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3486-113">Return value</span></span>

<span data-ttu-id="b3486-114">Devuelve el identificador del control de información sobre herramientas si se realiza correctamente o **null** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b3486-114">Returns the handle to the tooltip control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3486-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3486-115">Remarks</span></span>

<span data-ttu-id="b3486-116">Un control de ficha crea un control de información sobre herramientas si tiene el estilo [**\_ información sobre herramientas de TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b3486-116">A tab control creates a tooltip control if it has the [**TCS\_TOOLTIPS**](tab-control-styles.md) style.</span></span> <span data-ttu-id="b3486-117">También puede asignar un control de información sobre herramientas a un control de ficha mediante el mensaje [**\_ SETTOOLTIPS de TCM**](tcm-settooltips.md) .</span><span class="sxs-lookup"><span data-stu-id="b3486-117">You can also assign a tooltip control to a tab control by using the [**TCM\_SETTOOLTIPS**](tcm-settooltips.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3486-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3486-118">Requirements</span></span>



| <span data-ttu-id="b3486-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3486-119">Requirement</span></span> | <span data-ttu-id="b3486-120">Value</span><span class="sxs-lookup"><span data-stu-id="b3486-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3486-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3486-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b3486-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3486-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3486-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3486-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b3486-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3486-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3486-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3486-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3486-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3486-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





