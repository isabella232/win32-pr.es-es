---
title: Mensaje de TTM_ADDTOOL (commctrl. h)
description: Registra una herramienta con un control ToolTip.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- TTM_ADDTOOL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658193"
---
# <a name="ttm_addtool-message"></a><span data-ttu-id="5d029-104">TTM \_ ADDTOOL</span><span class="sxs-lookup"><span data-stu-id="5d029-104">TTM\_ADDTOOL message</span></span>

<span data-ttu-id="5d029-105">Registra una herramienta con un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="5d029-105">Registers a tool with a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d029-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d029-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d029-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d029-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d029-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5d029-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5d029-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d029-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d029-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que contiene información que el control ToolTip necesita para mostrar texto para la herramienta.</span><span class="sxs-lookup"><span data-stu-id="5d029-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure containing information that the tooltip control needs to display text for the tool.</span></span> <span data-ttu-id="5d029-111">El miembro **cbSize** de esta estructura se debe rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d029-111">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d029-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d029-112">Return value</span></span>

<span data-ttu-id="5d029-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5d029-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d029-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d029-114">Requirements</span></span>



| <span data-ttu-id="5d029-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d029-115">Requirement</span></span> | <span data-ttu-id="5d029-116">Value</span><span class="sxs-lookup"><span data-stu-id="5d029-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d029-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d029-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5d029-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5d029-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d029-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d029-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5d029-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d029-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d029-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d029-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d029-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d029-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5d029-123">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="5d029-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5d029-124">**TTM \_ ADDTOOLW** (Unicode) y **TTM \_ ADDTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5d029-124">**TTM\_ADDTOOLW** (Unicode) and **TTM\_ADDTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="5d029-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d029-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d029-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5d029-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5d029-127">**TTM \_ DELTOOL**</span><span class="sxs-lookup"><span data-stu-id="5d029-127">**TTM\_DELTOOL**</span></span>](ttm-deltool.md)
</dt> <dt>

<span data-ttu-id="5d029-128">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5d029-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5d029-129">Acerca de los controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="5d029-129">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





