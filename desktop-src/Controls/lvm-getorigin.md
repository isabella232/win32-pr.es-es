---
title: Mensaje de LVM_GETORIGIN (commctrl. h)
description: Recupera el origen de la vista actual para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetOrigin de ListView.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150891"
---
# <a name="lvm_getorigin-message"></a><span data-ttu-id="f2269-105">\_Mensaje GETORIGIN LVM</span><span class="sxs-lookup"><span data-stu-id="f2269-105">LVM\_GETORIGIN message</span></span>

<span data-ttu-id="f2269-106">Recupera el origen de la vista actual para un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f2269-106">Retrieves the current view origin for a list-view control.</span></span> <span data-ttu-id="f2269-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetOrigin de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .</span><span class="sxs-lookup"><span data-stu-id="f2269-107">You can send this message explicitly or by using the [**ListView\_GetOrigin**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2269-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2269-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2269-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2269-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2269-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2269-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2269-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2269-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2269-112">Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que recibe el origen de la vista.</span><span class="sxs-lookup"><span data-stu-id="f2269-112">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the view origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2269-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2269-113">Return value</span></span>

<span data-ttu-id="f2269-114">Devuelve **true** si es correcto, o **false** si la vista actual es una lista o una vista de informe.</span><span class="sxs-lookup"><span data-stu-id="f2269-114">Returns **TRUE** if successful, or **FALSE** if the current view is list or report view.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2269-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2269-115">Requirements</span></span>



| <span data-ttu-id="f2269-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2269-116">Requirement</span></span> | <span data-ttu-id="f2269-117">Value</span><span class="sxs-lookup"><span data-stu-id="f2269-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2269-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2269-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2269-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2269-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2269-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2269-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2269-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2269-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2269-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2269-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2269-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2269-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

