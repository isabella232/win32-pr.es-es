---
title: Mensaje de TCM_GETCURFOCUS (commctrl. h)
description: Devuelve el índice del elemento que tiene el foco en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetCurFocus.
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996964"
---
# <a name="tcm_getcurfocus-message"></a><span data-ttu-id="78f3f-105">\_Mensaje GETCURFOCUS de TCM</span><span class="sxs-lookup"><span data-stu-id="78f3f-105">TCM\_GETCURFOCUS message</span></span>

<span data-ttu-id="78f3f-106">Devuelve el índice del elemento que tiene el foco en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="78f3f-106">Returns the index of the item that has the focus in a tab control.</span></span> <span data-ttu-id="78f3f-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="78f3f-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="78f3f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78f3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f3f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78f3f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="78f3f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="78f3f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="78f3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78f3f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="78f3f-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="78f3f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f3f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78f3f-113">Return value</span></span>

<span data-ttu-id="78f3f-114">Devuelve el índice del elemento de pestaña que tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="78f3f-114">Returns the index of the tab item that has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="78f3f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78f3f-115">Remarks</span></span>

<span data-ttu-id="78f3f-116">El elemento que tiene el foco puede ser diferente del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="78f3f-116">The item that has the focus may be different than the selected item.</span></span>

## <a name="requirements"></a><span data-ttu-id="78f3f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78f3f-117">Requirements</span></span>



| <span data-ttu-id="78f3f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f3f-118">Requirement</span></span> | <span data-ttu-id="78f3f-119">Value</span><span class="sxs-lookup"><span data-stu-id="78f3f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78f3f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78f3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78f3f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="78f3f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78f3f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78f3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78f3f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="78f3f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78f3f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78f3f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="78f3f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78f3f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





