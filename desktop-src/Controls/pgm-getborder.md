---
title: Mensaje de PGM_GETBORDER (commctrl. h)
description: Recupera el tamaño actual del borde para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetBorder de buscapersonas \_ .
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658260"
---
# <a name="pgm_getborder-message"></a><span data-ttu-id="db770-105">\_Mensaje GETBORDER PGM</span><span class="sxs-lookup"><span data-stu-id="db770-105">PGM\_GETBORDER message</span></span>

<span data-ttu-id="db770-106">Recupera el tamaño actual del borde para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="db770-106">Retrieves the current border size for the pager control.</span></span> <span data-ttu-id="db770-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetBorder de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .</span><span class="sxs-lookup"><span data-stu-id="db770-107">You can send this message explicitly or use the [**Pager\_GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="db770-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db770-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db770-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db770-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="db770-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db770-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="db770-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db770-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="db770-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="db770-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db770-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db770-113">Return value</span></span>

<span data-ttu-id="db770-114">Devuelve un valor INT que contiene el tamaño actual del borde, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="db770-114">Returns an INT value that contains the current border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="db770-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db770-115">Requirements</span></span>



| <span data-ttu-id="db770-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="db770-116">Requirement</span></span> | <span data-ttu-id="db770-117">Value</span><span class="sxs-lookup"><span data-stu-id="db770-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db770-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db770-118">Minimum supported client</span></span><br/> | <span data-ttu-id="db770-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db770-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db770-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db770-120">Minimum supported server</span></span><br/> | <span data-ttu-id="db770-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="db770-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db770-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db770-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="db770-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db770-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db770-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="db770-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db770-125">**\_SETBORDER PGM**</span><span class="sxs-lookup"><span data-stu-id="db770-125">**PGM\_SETBORDER**</span></span>](pgm-setborder.md)
</dt> </dl>

 

 





