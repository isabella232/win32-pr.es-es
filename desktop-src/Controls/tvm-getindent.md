---
title: Mensaje de TVM_GETINDENT (commctrl. h)
description: Recupera la cantidad, en píxeles, a la que se aplica sangría a los elementos secundarios respecto a sus elementos primarios. Puede enviar este mensaje explícitamente o mediante la \_ macro GetIndent de TreeView.
ms.assetid: 4109714e-94a3-4c88-96e7-b4b8ec67f4a1
keywords:
- TVM_GETINDENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33775341adc47d84ead9a633d7d31b16ffc4a723
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905583"
---
# <a name="tvm_getindent-message"></a><span data-ttu-id="913d1-105">\_Mensaje de GETINDENT TVM</span><span class="sxs-lookup"><span data-stu-id="913d1-105">TVM\_GETINDENT message</span></span>

<span data-ttu-id="913d1-106">Recupera la cantidad, en píxeles, a la que se aplica sangría a los elementos secundarios respecto a sus elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="913d1-106">Retrieves the amount, in pixels, that child items are indented relative to their parent items.</span></span> <span data-ttu-id="913d1-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetIndent de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) .</span><span class="sxs-lookup"><span data-stu-id="913d1-107">You can send this message explicitly or by using the [**TreeView\_GetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="913d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="913d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="913d1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="913d1-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="913d1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="913d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="913d1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="913d1-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="913d1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913d1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="913d1-113">Return value</span></span>

<span data-ttu-id="913d1-114">Devuelve la cantidad de sangría.</span><span class="sxs-lookup"><span data-stu-id="913d1-114">Returns the amount of indentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="913d1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913d1-115">Requirements</span></span>



| <span data-ttu-id="913d1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="913d1-116">Requirement</span></span> | <span data-ttu-id="913d1-117">Value</span><span class="sxs-lookup"><span data-stu-id="913d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="913d1-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="913d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="913d1-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="913d1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="913d1-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="913d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="913d1-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="913d1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="913d1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="913d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="913d1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="913d1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





