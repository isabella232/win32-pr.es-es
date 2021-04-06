---
title: Mensaje de TVM_SETTEXTCOLOR (commctrl. h)
description: Establece el color del texto del control. Puede enviar este mensaje explícitamente o mediante la \_ macro SetTextColor de TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802648"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="bd96d-105">\_Mensaje de SETTEXTCOLOR TVM</span><span class="sxs-lookup"><span data-stu-id="bd96d-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="bd96d-106">Establece el color del texto del control.</span><span class="sxs-lookup"><span data-stu-id="bd96d-106">Sets the text color of the control.</span></span> <span data-ttu-id="bd96d-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="bd96d-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd96d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd96d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd96d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd96d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd96d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bd96d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd96d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd96d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd96d-112">Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que contiene el nuevo color de texto.</span><span class="sxs-lookup"><span data-stu-id="bd96d-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="bd96d-113">Si este argumento es-1, el control volverá a usar el color del sistema para el color del texto.</span><span class="sxs-lookup"><span data-stu-id="bd96d-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd96d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd96d-114">Return value</span></span>

<span data-ttu-id="bd96d-115">Devuelve un valor de **COLORREF** que representa el color del texto anterior.</span><span class="sxs-lookup"><span data-stu-id="bd96d-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="bd96d-116">Si este valor es-1, el control estaba usando el color del sistema para el color del texto.</span><span class="sxs-lookup"><span data-stu-id="bd96d-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd96d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd96d-117">Requirements</span></span>



| <span data-ttu-id="bd96d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd96d-118">Requirement</span></span> | <span data-ttu-id="bd96d-119">Value</span><span class="sxs-lookup"><span data-stu-id="bd96d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd96d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd96d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bd96d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bd96d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd96d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd96d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bd96d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd96d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd96d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd96d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd96d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd96d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd96d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd96d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd96d-127">**TVM \_ GETTEXTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bd96d-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

