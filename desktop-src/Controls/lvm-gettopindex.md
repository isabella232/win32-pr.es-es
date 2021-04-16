---
title: Mensaje de LVM_GETTOPINDEX (commctrl. h)
description: Recupera el índice del elemento visible más alto cuando está en la vista de lista o informe. Puede enviar este mensaje explícitamente o mediante la \_ macro GetTopIndex de ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- LVM_GETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658335"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="035db-105">\_Mensaje GETTOPINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="035db-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="035db-106">Recupera el índice del elemento visible más alto cuando está en la vista de lista o informe.</span><span class="sxs-lookup"><span data-stu-id="035db-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="035db-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetTopIndex de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .</span><span class="sxs-lookup"><span data-stu-id="035db-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="035db-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="035db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="035db-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="035db-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="035db-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="035db-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="035db-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="035db-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="035db-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="035db-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="035db-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="035db-113">Return value</span></span>

<span data-ttu-id="035db-114">Devuelve el índice del elemento si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="035db-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="035db-115">Devuelve cero si el control de vista de lista está en la vista de icono o de iconos pequeños, o si el control de vista de lista está en la vista de detalles con los grupos habilitados.</span><span class="sxs-lookup"><span data-stu-id="035db-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="035db-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="035db-116">Requirements</span></span>



| <span data-ttu-id="035db-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="035db-117">Requirement</span></span> | <span data-ttu-id="035db-118">Value</span><span class="sxs-lookup"><span data-stu-id="035db-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="035db-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="035db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="035db-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="035db-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="035db-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="035db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="035db-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="035db-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="035db-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="035db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="035db-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="035db-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





