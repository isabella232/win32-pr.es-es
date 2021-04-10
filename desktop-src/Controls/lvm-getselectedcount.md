---
title: Mensaje de LVM_GETSELECTEDCOUNT (commctrl. h)
description: Determina el número de elementos seleccionados en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetSelectedCount de ListView.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- LVM_GETSELECTEDCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905504"
---
# <a name="lvm_getselectedcount-message"></a><span data-ttu-id="d4a50-105">\_Mensaje GETSELECTEDCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="d4a50-105">LVM\_GETSELECTEDCOUNT message</span></span>

<span data-ttu-id="d4a50-106">Determina el número de elementos seleccionados en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="d4a50-106">Determines the number of selected items in a list-view control.</span></span> <span data-ttu-id="d4a50-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetSelectedCount de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .</span><span class="sxs-lookup"><span data-stu-id="d4a50-107">You can send this message explicitly or by using the [**ListView\_GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4a50-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4a50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a50-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4a50-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4a50-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d4a50-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4a50-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4a50-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4a50-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d4a50-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4a50-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4a50-113">Return value</span></span>

<span data-ttu-id="d4a50-114">Devuelve el número de elementos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="d4a50-114">Returns the number of selected items.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4a50-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4a50-115">Requirements</span></span>



| <span data-ttu-id="d4a50-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4a50-116">Requirement</span></span> | <span data-ttu-id="d4a50-117">Value</span><span class="sxs-lookup"><span data-stu-id="d4a50-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a50-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4a50-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4a50-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d4a50-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4a50-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4a50-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4a50-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4a50-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4a50-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4a50-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4a50-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a50-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





