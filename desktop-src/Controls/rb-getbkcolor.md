---
title: Mensaje de RB_GETBKCOLOR (commctrl. h)
description: Recupera el color de fondo predeterminado de un control rebar.
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- RB_GETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0c6f2348dfa54dc02ddc40658fd1289885ff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491765"
---
# <a name="rb_getbkcolor-message"></a><span data-ttu-id="9e761-104">Mensaje de GETBKCOLOR de RB \_</span><span class="sxs-lookup"><span data-stu-id="9e761-104">RB\_GETBKCOLOR message</span></span>

<span data-ttu-id="9e761-105">Recupera el color de fondo predeterminado de un control rebar.</span><span class="sxs-lookup"><span data-stu-id="9e761-105">Retrieves a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e761-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e761-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e761-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e761-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e761-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e761-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e761-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9e761-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e761-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e761-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e761-111">Return value</span></span>

<span data-ttu-id="9e761-112">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="9e761-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represent the current default background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e761-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e761-113">Requirements</span></span>



| <span data-ttu-id="9e761-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e761-114">Requirement</span></span> | <span data-ttu-id="9e761-115">Value</span><span class="sxs-lookup"><span data-stu-id="9e761-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e761-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e761-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9e761-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e761-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e761-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e761-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9e761-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e761-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e761-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e761-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e761-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e761-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e761-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e761-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e761-123">**\_SETBKCOLOR RB**</span><span class="sxs-lookup"><span data-stu-id="9e761-123">**RB\_SETBKCOLOR**</span></span>](rb-setbkcolor.md)
</dt> </dl>

 

