---
title: Mensaje de LVM_GETITEMCOUNT (commctrl. h)
description: Recupera el número de elementos de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemCount de ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803392"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="846e8-105">\_Mensaje GETITEMCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="846e8-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="846e8-106">Recupera el número de elementos de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="846e8-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="846e8-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemCount de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="846e8-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="846e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="846e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="846e8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="846e8-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="846e8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="846e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="846e8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="846e8-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="846e8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846e8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="846e8-113">Return value</span></span>

<span data-ttu-id="846e8-114">Devuelve el número de elementos.</span><span class="sxs-lookup"><span data-stu-id="846e8-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="846e8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="846e8-115">Requirements</span></span>



| <span data-ttu-id="846e8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="846e8-116">Requirement</span></span> | <span data-ttu-id="846e8-117">Value</span><span class="sxs-lookup"><span data-stu-id="846e8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="846e8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="846e8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="846e8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="846e8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="846e8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="846e8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="846e8-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="846e8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="846e8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="846e8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="846e8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="846e8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





