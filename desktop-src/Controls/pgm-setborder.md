---
title: Mensaje de PGM_SETBORDER (commctrl. h)
description: Establece el tamaño actual del borde para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro SetBorder de buscapersonas \_ .
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079268"
---
# <a name="pgm_setborder-message"></a><span data-ttu-id="2dc69-105">\_Mensaje SETBORDER PGM</span><span class="sxs-lookup"><span data-stu-id="2dc69-105">PGM\_SETBORDER message</span></span>

<span data-ttu-id="2dc69-106">Establece el tamaño actual del borde para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="2dc69-106">Sets the current border size for the pager control.</span></span> <span data-ttu-id="2dc69-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetBorder de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) .</span><span class="sxs-lookup"><span data-stu-id="2dc69-107">You can send this message explicitly or use the [**Pager\_SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2dc69-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dc69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2dc69-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2dc69-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2dc69-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2dc69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2dc69-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dc69-112">Nuevo tamaño del borde, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2dc69-112">New size of the border, in pixels.</span></span> <span data-ttu-id="2dc69-113">Este valor no debe ser mayor que el botón de buscapersonas o menor que cero.</span><span class="sxs-lookup"><span data-stu-id="2dc69-113">This value should not be larger than the pager button or less than zero.</span></span> <span data-ttu-id="2dc69-114">Si *lParam* es demasiado grande, el borde se dibujará con el mismo tamaño que el botón.</span><span class="sxs-lookup"><span data-stu-id="2dc69-114">If *lParam* is too large, the border will be drawn the same size as the button.</span></span> <span data-ttu-id="2dc69-115">Si *lParam* es negativo, el tamaño del borde se establecerá en cero.</span><span class="sxs-lookup"><span data-stu-id="2dc69-115">If *lParam* is negative, the border size will be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc69-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dc69-116">Return value</span></span>

<span data-ttu-id="2dc69-117">Devuelve un valor INT que contiene el tamaño de borde anterior, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="2dc69-117">Returns an INT value that contains the previous border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc69-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dc69-118">Requirements</span></span>



| <span data-ttu-id="2dc69-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dc69-119">Requirement</span></span> | <span data-ttu-id="2dc69-120">Value</span><span class="sxs-lookup"><span data-stu-id="2dc69-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc69-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc69-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2dc69-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2dc69-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dc69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc69-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dc69-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2dc69-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dc69-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dc69-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc69-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





