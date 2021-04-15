---
title: Mensaje de MCM_GETCURRENTVIEW (commctrl. h)
description: Obtiene la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492383"
---
# <a name="mcm_getcurrentview-message"></a><span data-ttu-id="488e6-105">Mensaje de MCM \_ GETCURRENTVIEW</span><span class="sxs-lookup"><span data-stu-id="488e6-105">MCM\_GETCURRENTVIEW message</span></span>

<span data-ttu-id="488e6-106">Obtiene la vista actual del calendario.</span><span class="sxs-lookup"><span data-stu-id="488e6-106">Gets the current view of the calendar.</span></span> <span data-ttu-id="488e6-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="488e6-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="488e6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="488e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="488e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="488e6-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="488e6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="488e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="488e6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="488e6-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="488e6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="488e6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="488e6-113">Return value</span></span>

<span data-ttu-id="488e6-114">Vista actual.</span><span class="sxs-lookup"><span data-stu-id="488e6-114">Current view.</span></span> <span data-ttu-id="488e6-115">Uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="488e6-115">One of the following values.</span></span>



| <span data-ttu-id="488e6-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="488e6-116">Return code</span></span>                                                                                  | <span data-ttu-id="488e6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="488e6-117">Description</span></span>              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="488e6-118"><dt>**MCMV \_ mes**</dt></span><span class="sxs-lookup"><span data-stu-id="488e6-118"><dt>**MCMV\_MONTH**</dt></span></span> </dl>   | <span data-ttu-id="488e6-119">Vista mensual.</span><span class="sxs-lookup"><span data-stu-id="488e6-119">Monthly view.</span></span><br/> |
| <dl> <span data-ttu-id="488e6-120"><dt>**MCMV \_ año**</dt></span><span class="sxs-lookup"><span data-stu-id="488e6-120"><dt>**MCMV\_YEAR**</dt></span></span> </dl>    | <span data-ttu-id="488e6-121">Vista anual.</span><span class="sxs-lookup"><span data-stu-id="488e6-121">Annual view.</span></span><br/>  |
| <dl> <span data-ttu-id="488e6-122"><dt>**década de MCMV \_**</dt></span><span class="sxs-lookup"><span data-stu-id="488e6-122"><dt>**MCMV\_DECADE**</dt></span></span> </dl>  | <span data-ttu-id="488e6-123">Vista de década.</span><span class="sxs-lookup"><span data-stu-id="488e6-123">Decade view.</span></span><br/>  |
| <dl> <span data-ttu-id="488e6-124"><dt>**\_siglo MCMV**</dt></span><span class="sxs-lookup"><span data-stu-id="488e6-124"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="488e6-125">Vista de siglo.</span><span class="sxs-lookup"><span data-stu-id="488e6-125">Century view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="488e6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="488e6-126">Requirements</span></span>



| <span data-ttu-id="488e6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="488e6-127">Requirement</span></span> | <span data-ttu-id="488e6-128">Value</span><span class="sxs-lookup"><span data-stu-id="488e6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="488e6-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="488e6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="488e6-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="488e6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="488e6-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="488e6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="488e6-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="488e6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="488e6-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="488e6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="488e6-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="488e6-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





