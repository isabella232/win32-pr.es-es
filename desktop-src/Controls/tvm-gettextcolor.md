---
title: Mensaje de TVM_GETTEXTCOLOR (commctrl. h)
description: Recupera el color de texto actual del control. Puede enviar este mensaje explícitamente o mediante la \_ macro GetTextColor de TreeView.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- TVM_GETTEXTCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079115"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="0a73e-105">\_Mensaje de GETTEXTCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="0a73e-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="0a73e-106">Recupera el color de texto actual del control.</span><span class="sxs-lookup"><span data-stu-id="0a73e-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="0a73e-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetTextColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="0a73e-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a73e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a73e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a73e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a73e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0a73e-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0a73e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0a73e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a73e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0a73e-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0a73e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a73e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a73e-113">Return value</span></span>

<span data-ttu-id="0a73e-114">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color del texto actual.</span><span class="sxs-lookup"><span data-stu-id="0a73e-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="0a73e-115">Si este valor es-1, el control usa el color del sistema para el color del texto.</span><span class="sxs-lookup"><span data-stu-id="0a73e-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a73e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a73e-116">Requirements</span></span>



| <span data-ttu-id="0a73e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a73e-117">Requirement</span></span> | <span data-ttu-id="0a73e-118">Value</span><span class="sxs-lookup"><span data-stu-id="0a73e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a73e-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a73e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0a73e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a73e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a73e-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a73e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0a73e-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a73e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a73e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a73e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a73e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a73e-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a73e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a73e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a73e-126">**TVM \_ SETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0a73e-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

