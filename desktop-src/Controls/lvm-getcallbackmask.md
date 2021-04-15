---
title: Mensaje de LVM_GETCALLBACKMASK (commctrl. h)
description: Obtiene la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetCallbackMask de ListView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489070"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="0cda2-105">\_Mensaje GETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="0cda2-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="0cda2-106">Obtiene la máscara de devolución de llamada para un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="0cda2-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="0cda2-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetCallbackMask de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="0cda2-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0cda2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cda2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cda2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0cda2-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0cda2-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0cda2-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0cda2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0cda2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0cda2-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0cda2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cda2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cda2-113">Return value</span></span>

<span data-ttu-id="0cda2-114">Devuelve la máscara de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0cda2-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cda2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cda2-115">Requirements</span></span>



| <span data-ttu-id="0cda2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cda2-116">Requirement</span></span> | <span data-ttu-id="0cda2-117">Value</span><span class="sxs-lookup"><span data-stu-id="0cda2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cda2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cda2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0cda2-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0cda2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0cda2-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cda2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0cda2-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cda2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cda2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cda2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cda2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cda2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





