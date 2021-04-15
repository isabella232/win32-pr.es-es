---
title: Mensaje de LVM_GETFOCUSEDGROUP (commctrl. h)
description: Obtiene el grupo que tiene el foco. Envíe este mensaje explícitamente o mediante la \_ macro GetFocusedGroup de ListView.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489058"
---
# <a name="lvm_getfocusedgroup-message"></a><span data-ttu-id="87855-105">\_Mensaje GETFOCUSEDGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="87855-105">LVM\_GETFOCUSEDGROUP message</span></span>

<span data-ttu-id="87855-106">Obtiene el grupo que tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="87855-106">Gets the group that has the focus.</span></span> <span data-ttu-id="87855-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetFocusedGroup de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) .</span><span class="sxs-lookup"><span data-stu-id="87855-107">Send this message explicitly or by using the [**ListView\_GetFocusedGroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="87855-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87855-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87855-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="87855-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="87855-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="87855-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="87855-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="87855-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="87855-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="87855-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87855-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87855-113">Return value</span></span>

<span data-ttu-id="87855-114">Devuelve el índice del grupo con el estado de LVGS \_ enfocado, o-1 si no hay ningún grupo con el estado de LVGS \_ centrado.</span><span class="sxs-lookup"><span data-stu-id="87855-114">Returns the index of the group with state of LVGS\_FOCUSED, or -1 if there is no group with state of LVGS\_FOCUSED.</span></span>

## <a name="requirements"></a><span data-ttu-id="87855-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87855-115">Requirements</span></span>



| <span data-ttu-id="87855-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="87855-116">Requirement</span></span> | <span data-ttu-id="87855-117">Value</span><span class="sxs-lookup"><span data-stu-id="87855-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87855-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87855-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87855-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="87855-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="87855-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87855-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87855-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="87855-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87855-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87855-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="87855-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="87855-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





