---
title: Mensaje de TTM_DELTOOL (commctrl. h)
description: Quita una herramienta de un control ToolTip.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658192"
---
# <a name="ttm_deltool-message"></a><span data-ttu-id="ffd15-104">TTM \_ DELTOOL</span><span class="sxs-lookup"><span data-stu-id="ffd15-104">TTM\_DELTOOL message</span></span>

<span data-ttu-id="ffd15-105">Quita una herramienta de un control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="ffd15-105">Removes a tool from a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ffd15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffd15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd15-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ffd15-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ffd15-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ffd15-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ffd15-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffd15-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd15-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ffd15-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="ffd15-111">Los miembros **hWnd** y **uId** identifican la herramienta que se va a quitar y el miembro **cbSize** debe especificar el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="ffd15-111">The **hwnd** and **uId** members identify the tool to remove, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="ffd15-112">Se omiten todos los demás miembros.</span><span class="sxs-lookup"><span data-stu-id="ffd15-112">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd15-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffd15-113">Return value</span></span>

<span data-ttu-id="ffd15-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ffd15-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd15-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffd15-115">Requirements</span></span>



| <span data-ttu-id="ffd15-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffd15-116">Requirement</span></span> | <span data-ttu-id="ffd15-117">Value</span><span class="sxs-lookup"><span data-stu-id="ffd15-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd15-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd15-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ffd15-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ffd15-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffd15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd15-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffd15-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffd15-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffd15-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd15-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd15-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ffd15-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ffd15-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ffd15-125">**TTM \_ DELTOOLW** (Unicode) y **TTM \_ DELTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ffd15-125">**TTM\_DELTOOLW** (Unicode) and **TTM\_DELTOOLA** (ANSI)</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="ffd15-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffd15-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ffd15-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ffd15-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd15-128">**TTM \_ ADDTOOL**</span><span class="sxs-lookup"><span data-stu-id="ffd15-128">**TTM\_ADDTOOL**</span></span>](ttm-addtool.md)
</dt> <dt>

<span data-ttu-id="ffd15-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ffd15-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ffd15-130">Acerca de los controles ToolTip</span><span class="sxs-lookup"><span data-stu-id="ffd15-130">About Tooltip Controls</span></span>](tooltip-controls.md)
</dt> </dl>

 

 





