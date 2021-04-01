---
title: Mensaje de MCM_SETCURRENTVIEW (commctrl. h)
description: Establece la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997028"
---
# <a name="mcm_setcurrentview-message"></a><span data-ttu-id="52c13-105">Mensaje de MCM \_ SETCURRENTVIEW</span><span class="sxs-lookup"><span data-stu-id="52c13-105">MCM\_SETCURRENTVIEW message</span></span>

<span data-ttu-id="52c13-106">Establece la vista actual del calendario.</span><span class="sxs-lookup"><span data-stu-id="52c13-106">Sets the current view of the calendar.</span></span> <span data-ttu-id="52c13-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) .</span><span class="sxs-lookup"><span data-stu-id="52c13-107">You can send this message explicitly or by using the [**MonthCal\_SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="52c13-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52c13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c13-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52c13-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52c13-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="52c13-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="52c13-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52c13-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52c13-112">Nueva vista.</span><span class="sxs-lookup"><span data-stu-id="52c13-112">New view.</span></span> <span data-ttu-id="52c13-113">Una de las constantes siguientes.</span><span class="sxs-lookup"><span data-stu-id="52c13-113">One of the following constants.</span></span>



| <span data-ttu-id="52c13-114">Value</span><span class="sxs-lookup"><span data-stu-id="52c13-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="52c13-115">Significado</span><span class="sxs-lookup"><span data-stu-id="52c13-115">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <span data-ttu-id="52c13-116"><dt>**MCMV \_ mes**</dt></span><span class="sxs-lookup"><span data-stu-id="52c13-116"><dt>**MCMV\_MONTH**</dt></span></span> </dl>       | <span data-ttu-id="52c13-117">Vista mensual.</span><span class="sxs-lookup"><span data-stu-id="52c13-117">Monthly view.</span></span><br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <span data-ttu-id="52c13-118"><dt>**MCMV \_ año**</dt></span><span class="sxs-lookup"><span data-stu-id="52c13-118"><dt>**MCMV\_YEAR**</dt></span></span> </dl>          | <span data-ttu-id="52c13-119">Vista anual.</span><span class="sxs-lookup"><span data-stu-id="52c13-119">Annual view.</span></span><br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <span data-ttu-id="52c13-120"><dt>**década de MCMV \_**</dt></span><span class="sxs-lookup"><span data-stu-id="52c13-120"><dt>**MCMV\_DECADE**</dt></span></span> </dl>    | <span data-ttu-id="52c13-121">Vista de década.</span><span class="sxs-lookup"><span data-stu-id="52c13-121">Decade view.</span></span><br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <span data-ttu-id="52c13-122"><dt>**\_siglo MCMV**</dt></span><span class="sxs-lookup"><span data-stu-id="52c13-122"><dt>**MCMV\_CENTURY**</dt></span></span> </dl> | <span data-ttu-id="52c13-123">Vista de siglo.</span><span class="sxs-lookup"><span data-stu-id="52c13-123">Century view.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c13-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52c13-124">Return value</span></span>

<span data-ttu-id="52c13-125">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="52c13-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c13-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52c13-126">Requirements</span></span>



| <span data-ttu-id="52c13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c13-127">Requirement</span></span> | <span data-ttu-id="52c13-128">Value</span><span class="sxs-lookup"><span data-stu-id="52c13-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52c13-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52c13-129">Minimum supported client</span></span><br/> | <span data-ttu-id="52c13-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="52c13-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52c13-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52c13-131">Minimum supported server</span></span><br/> | <span data-ttu-id="52c13-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="52c13-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52c13-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52c13-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="52c13-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c13-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





