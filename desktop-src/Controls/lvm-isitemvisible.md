---
title: Mensaje de LVM_ISITEMVISIBLE (commctrl. h)
description: Indica si un elemento del control de vista de lista está visible. Envíe este mensaje explícitamente o mediante la \_ macro IsItemVisible de ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905498"
---
# <a name="lvm_isitemvisible-message"></a><span data-ttu-id="bfec9-105">\_Mensaje ISITEMVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="bfec9-105">LVM\_ISITEMVISIBLE message</span></span>

<span data-ttu-id="bfec9-106">Indica si un elemento del control de vista de lista está visible.</span><span class="sxs-lookup"><span data-stu-id="bfec9-106">Indicates if an item in the list-view control is visible.</span></span> <span data-ttu-id="bfec9-107">Envíe este mensaje explícitamente o mediante la [**macro \_ IsItemVisible de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .</span><span class="sxs-lookup"><span data-stu-id="bfec9-107">Send this message explicitly or by using the [**ListView\_IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bfec9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfec9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfec9-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bfec9-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfec9-110">Índice del elemento en el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="bfec9-110">An index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="bfec9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfec9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bfec9-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bfec9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfec9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfec9-113">Return value</span></span>

<span data-ttu-id="bfec9-114">Devuelve **true** si está visible o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bfec9-114">Returns **TRUE** if visible, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfec9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfec9-115">Requirements</span></span>



| <span data-ttu-id="bfec9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfec9-116">Requirement</span></span> | <span data-ttu-id="bfec9-117">Value</span><span class="sxs-lookup"><span data-stu-id="bfec9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfec9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfec9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bfec9-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bfec9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfec9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfec9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bfec9-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfec9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfec9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfec9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfec9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfec9-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





