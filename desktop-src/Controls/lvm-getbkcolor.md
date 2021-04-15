---
title: Mensaje de LVM_GETBKCOLOR (commctrl. h)
description: Obtiene el color de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetBkColor de ListView.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- LVM_GETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489076"
---
# <a name="lvm_getbkcolor-message"></a><span data-ttu-id="1b59f-105">\_Mensaje GETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="1b59f-105">LVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="1b59f-106">Obtiene el color de fondo de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1b59f-106">Gets the background color of a list-view control.</span></span> <span data-ttu-id="1b59f-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetBkColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="1b59f-107">You can send this message explicitly or by using the [**ListView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b59f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b59f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b59f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b59f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b59f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1b59f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b59f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b59f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b59f-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1b59f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b59f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b59f-113">Return value</span></span>

<span data-ttu-id="1b59f-114">Devuelve el color de fondo del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="1b59f-114">Returns the background color of the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b59f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b59f-115">Requirements</span></span>



| <span data-ttu-id="1b59f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b59f-116">Requirement</span></span> | <span data-ttu-id="1b59f-117">Value</span><span class="sxs-lookup"><span data-stu-id="1b59f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b59f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b59f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b59f-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b59f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b59f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b59f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b59f-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b59f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b59f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b59f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b59f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b59f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





