---
title: Mensaje de PGM_GETDROPTARGET (commctrl. h)
description: Recupera el puntero de interfaz IDropTarget de un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetDropTarget de buscapersonas \_ .
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491789"
---
# <a name="pgm_getdroptarget-message"></a><span data-ttu-id="cf179-105">\_Mensaje GETDROPTARGET PGM</span><span class="sxs-lookup"><span data-stu-id="cf179-105">PGM\_GETDROPTARGET message</span></span>

<span data-ttu-id="cf179-106">Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación.</span><span class="sxs-lookup"><span data-stu-id="cf179-106">Retrieves a pager control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span> <span data-ttu-id="cf179-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetDropTarget de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="cf179-107">You can send this message explicitly or use the [**Pager\_GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf179-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf179-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf179-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cf179-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cf179-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cf179-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf179-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf179-112">Puntero a un puntero [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recibe el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="cf179-112">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="cf179-113">Es responsabilidad del autor de la llamada llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en este puntero cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="cf179-113">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf179-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf179-114">Return value</span></span>

<span data-ttu-id="cf179-115">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf179-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf179-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf179-116">Requirements</span></span>



| <span data-ttu-id="cf179-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf179-117">Requirement</span></span> | <span data-ttu-id="cf179-118">Value</span><span class="sxs-lookup"><span data-stu-id="cf179-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf179-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf179-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf179-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf179-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf179-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf179-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf179-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf179-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf179-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf179-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf179-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf179-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

