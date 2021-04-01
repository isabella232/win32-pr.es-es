---
title: Mensaje de LVM_GETTEXTBKCOLOR (commctrl. h)
description: Recupera el color de fondo del texto de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetTextBkColor de ListView.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- LVM_GETTEXTBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996909"
---
# <a name="lvm_gettextbkcolor-message"></a><span data-ttu-id="110ba-105">\_Mensaje GETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="110ba-105">LVM\_GETTEXTBKCOLOR message</span></span>

<span data-ttu-id="110ba-106">Recupera el color de fondo del texto de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="110ba-106">Retrieves the text background color of a list-view control.</span></span> <span data-ttu-id="110ba-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetTextBkColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="110ba-107">You can send this message explicitly or by using the [**ListView\_GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="110ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="110ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="110ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="110ba-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="110ba-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="110ba-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="110ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="110ba-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="110ba-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="110ba-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="110ba-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="110ba-113">Return value</span></span>

<span data-ttu-id="110ba-114">Devuelve el color de fondo del texto.</span><span class="sxs-lookup"><span data-stu-id="110ba-114">Returns the background color of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="110ba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="110ba-115">Requirements</span></span>



| <span data-ttu-id="110ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="110ba-116">Requirement</span></span> | <span data-ttu-id="110ba-117">Value</span><span class="sxs-lookup"><span data-stu-id="110ba-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="110ba-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="110ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="110ba-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="110ba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="110ba-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="110ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="110ba-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="110ba-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="110ba-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="110ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="110ba-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="110ba-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





