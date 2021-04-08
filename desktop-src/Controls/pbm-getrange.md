---
title: Mensaje de PBM_GETRANGE (commctrl. h)
description: Recupera información sobre los límites máximo y mínimo actuales de un control de barra de progreso determinado.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- PBM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996738"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="ef8eb-104">Mensaje de GETRANGE de PBM \_</span><span class="sxs-lookup"><span data-stu-id="ef8eb-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="ef8eb-105">Recupera información sobre los límites máximo y mínimo actuales de un control de barra de progreso determinado.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef8eb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef8eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8eb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef8eb-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef8eb-108">Valor de marca que especifica el valor de límite que se va a usar como valor devuelto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="ef8eb-109">Este parámetro puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ef8eb-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="ef8eb-110">Value</span><span class="sxs-lookup"><span data-stu-id="ef8eb-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="ef8eb-111">Significado</span><span class="sxs-lookup"><span data-stu-id="ef8eb-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="ef8eb-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ef8eb-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="ef8eb-113">Devuelve el límite inferior.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="ef8eb-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ef8eb-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="ef8eb-115">Devuelve el límite superior.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ef8eb-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef8eb-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef8eb-117">Puntero a una estructura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que se va a rellenar con los límites máximo y mínimo del control de barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="ef8eb-118">Si este parámetro se establece en **null**, el control devolverá solo el límite especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8eb-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef8eb-119">Return value</span></span>

<span data-ttu-id="ef8eb-120">Devuelve un valor INT que representa el valor de límite especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="ef8eb-121">Si *lParam* no es **null**, *lParam* debe apuntar a una estructura [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) que se va a rellenar con ambos valores de límite.</span><span class="sxs-lookup"><span data-stu-id="ef8eb-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8eb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef8eb-122">Requirements</span></span>



| <span data-ttu-id="ef8eb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef8eb-123">Requirement</span></span> | <span data-ttu-id="ef8eb-124">Value</span><span class="sxs-lookup"><span data-stu-id="ef8eb-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8eb-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef8eb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8eb-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef8eb-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef8eb-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef8eb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8eb-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef8eb-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef8eb-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef8eb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef8eb-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef8eb-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





