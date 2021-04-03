---
title: Mensaje de LVM_GETITEMPOSITION (commctrl. h)
description: Recupera la posición de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemPosition de ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905508"
---
# <a name="lvm_getitemposition-message"></a><span data-ttu-id="c69ce-105">\_Mensaje GETITEMPOSITION LVM</span><span class="sxs-lookup"><span data-stu-id="c69ce-105">LVM\_GETITEMPOSITION message</span></span>

<span data-ttu-id="c69ce-106">Recupera la posición de un elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="c69ce-106">Retrieves the position of a list-view item.</span></span> <span data-ttu-id="c69ce-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemPosition de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .</span><span class="sxs-lookup"><span data-stu-id="c69ce-107">You can send this message explicitly or by using the [**ListView\_GetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c69ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c69ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c69ce-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c69ce-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c69ce-110">Índice del elemento de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="c69ce-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="c69ce-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c69ce-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c69ce-112">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que recibe la posición de la esquina superior izquierda del elemento, en coordenadas de la vista.</span><span class="sxs-lookup"><span data-stu-id="c69ce-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the position of the item's upper-left corner, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c69ce-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c69ce-113">Return value</span></span>

<span data-ttu-id="c69ce-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c69ce-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c69ce-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c69ce-115">Requirements</span></span>



| <span data-ttu-id="c69ce-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c69ce-116">Requirement</span></span> | <span data-ttu-id="c69ce-117">Value</span><span class="sxs-lookup"><span data-stu-id="c69ce-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c69ce-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c69ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c69ce-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c69ce-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c69ce-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c69ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c69ce-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c69ce-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c69ce-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c69ce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c69ce-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c69ce-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

