---
title: Mensaje de TVM_GETBKCOLOR (commctrl. h)
description: Recupera el color de fondo actual del control. Puede enviar este mensaje explícitamente o mediante la \_ macro GetBkColor de TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658324"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="1a123-105">\_Mensaje de GETBKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="1a123-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="1a123-106">Recupera el color de fondo actual del control.</span><span class="sxs-lookup"><span data-stu-id="1a123-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="1a123-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetBkColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="1a123-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a123-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a123-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a123-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a123-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1a123-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1a123-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1a123-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a123-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1a123-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1a123-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a123-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a123-113">Return value</span></span>

<span data-ttu-id="1a123-114">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo actual.</span><span class="sxs-lookup"><span data-stu-id="1a123-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="1a123-115">Si este valor es-1, el control usa el color del sistema para el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="1a123-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a123-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a123-116">Requirements</span></span>



| <span data-ttu-id="1a123-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a123-117">Requirement</span></span> | <span data-ttu-id="1a123-118">Value</span><span class="sxs-lookup"><span data-stu-id="1a123-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a123-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a123-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1a123-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1a123-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a123-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a123-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1a123-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a123-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a123-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a123-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a123-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a123-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a123-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a123-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a123-126">**TVM \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="1a123-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

