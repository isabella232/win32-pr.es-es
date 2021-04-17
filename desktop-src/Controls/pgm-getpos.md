---
title: Mensaje de PGM_GETPOS (commctrl. h)
description: Recupera la posición de desplazamiento actual del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro getPos de buscapersonas \_ .
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658258"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="18dca-105">\_Mensaje GETPOS PGM</span><span class="sxs-lookup"><span data-stu-id="18dca-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="18dca-106">Recupera la posición de desplazamiento actual del control de paginación.</span><span class="sxs-lookup"><span data-stu-id="18dca-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="18dca-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ getPos de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .</span><span class="sxs-lookup"><span data-stu-id="18dca-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="18dca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18dca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18dca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="18dca-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="18dca-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="18dca-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="18dca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="18dca-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="18dca-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="18dca-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18dca-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18dca-113">Return value</span></span>

<span data-ttu-id="18dca-114">Devuelve un valor INT que contiene la posición de desplazamiento actual, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="18dca-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="18dca-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18dca-115">Requirements</span></span>



| <span data-ttu-id="18dca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18dca-116">Requirement</span></span> | <span data-ttu-id="18dca-117">Value</span><span class="sxs-lookup"><span data-stu-id="18dca-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18dca-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18dca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18dca-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="18dca-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18dca-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18dca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18dca-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="18dca-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18dca-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="18dca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18dca-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18dca-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





