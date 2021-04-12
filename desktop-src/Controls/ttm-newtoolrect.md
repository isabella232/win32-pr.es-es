---
title: Mensaje de TTM_NEWTOOLRECT (commctrl. h)
description: Establece un nuevo rectángulo delimitador para una herramienta.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490672"
---
# <a name="ttm_newtoolrect-message"></a><span data-ttu-id="2f3fe-104">TTM \_ NEWTOOLRECT</span><span class="sxs-lookup"><span data-stu-id="2f3fe-104">TTM\_NEWTOOLRECT message</span></span>

<span data-ttu-id="2f3fe-105">Establece un nuevo rectángulo delimitador para una herramienta.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-105">Sets a new bounding rectangle for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f3fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f3fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f3fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f3fe-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2f3fe-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2f3fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f3fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f3fe-110">Puntero a una estructura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2f3fe-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="2f3fe-111">Los miembros **hWnd** y **uId** identifican una herramienta y el miembro **Rect** especifica el nuevo rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-111">The **hwnd** and **uId** members identify a tool, and the **rect** member specifies the new bounding rectangle.</span></span> <span data-ttu-id="2f3fe-112">El miembro **cbSize** de esta estructura se debe rellenar antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-112">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f3fe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f3fe-113">Return value</span></span>

<span data-ttu-id="2f3fe-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3fe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f3fe-115">Requirements</span></span>



| <span data-ttu-id="2f3fe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f3fe-116">Requirement</span></span> | <span data-ttu-id="2f3fe-117">Value</span><span class="sxs-lookup"><span data-stu-id="2f3fe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3fe-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f3fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3fe-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2f3fe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f3fe-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f3fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3fe-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f3fe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f3fe-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f3fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f3fe-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3fe-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2f3fe-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="2f3fe-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2f3fe-125">**TTM \_ NEWTOOLRECTW** (Unicode) y **TTM \_ NEWTOOLRECTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2f3fe-125">**TTM\_NEWTOOLRECTW** (Unicode) and **TTM\_NEWTOOLRECTA** (ANSI)</span></span><br/>           |



 

 





