---
title: Mensaje de TVM_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo del control. Puede enviar este mensaje explícitamente o mediante la \_ macro SetBkColor de TreeView.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905349"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="0bc86-105">\_Mensaje de SETBKCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="0bc86-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="0bc86-106">Establece el color de fondo del control.</span><span class="sxs-lookup"><span data-stu-id="0bc86-106">Sets the background color of the control.</span></span> <span data-ttu-id="0bc86-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetBkColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="0bc86-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0bc86-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bc86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc86-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bc86-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0bc86-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0bc86-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0bc86-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bc86-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bc86-112">Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que contiene el nuevo color de fondo.</span><span class="sxs-lookup"><span data-stu-id="0bc86-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="0bc86-113">Si este valor es-1, el control volverá a usar el color del sistema para el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="0bc86-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc86-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bc86-114">Return value</span></span>

<span data-ttu-id="0bc86-115">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo anterior.</span><span class="sxs-lookup"><span data-stu-id="0bc86-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="0bc86-116">Si este valor es-1, el control estaba usando el color del sistema para el color de fondo.</span><span class="sxs-lookup"><span data-stu-id="0bc86-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc86-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bc86-117">Requirements</span></span>



| <span data-ttu-id="0bc86-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bc86-118">Requirement</span></span> | <span data-ttu-id="0bc86-119">Value</span><span class="sxs-lookup"><span data-stu-id="0bc86-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc86-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bc86-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0bc86-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0bc86-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0bc86-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bc86-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0bc86-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0bc86-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0bc86-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bc86-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bc86-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bc86-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bc86-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bc86-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc86-127">**TVM \_ GETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0bc86-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

