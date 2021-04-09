---
title: Mensaje de MCM_SETCALID (commctrl. h)
description: Establece el identificador de calendario para el control de calendario determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCALID.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- MCM_SETCALID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079005"
---
# <a name="mcm_setcalid-message"></a><span data-ttu-id="cc992-105">Mensaje de MCM \_ SETCALID</span><span class="sxs-lookup"><span data-stu-id="cc992-105">MCM\_SETCALID message</span></span>

<span data-ttu-id="cc992-106">Establece el identificador de calendario para el control de calendario determinado.</span><span class="sxs-lookup"><span data-stu-id="cc992-106">Sets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="cc992-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) .</span><span class="sxs-lookup"><span data-stu-id="cc992-107">You can send this message explicitly or by using the [**MonthCal\_SetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cc992-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc992-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc992-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc992-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc992-110">IDENTIFICADOR del calendario.</span><span class="sxs-lookup"><span data-stu-id="cc992-110">The calendar ID.</span></span> <span data-ttu-id="cc992-111">Una de las constantes de los [identificadores de calendario](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="cc992-111">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

</dd> <dt>

<span data-ttu-id="cc992-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc992-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc992-113">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cc992-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc992-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc992-114">Return value</span></span>

<span data-ttu-id="cc992-115">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="cc992-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc992-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc992-116">Requirements</span></span>



| <span data-ttu-id="cc992-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc992-117">Requirement</span></span> | <span data-ttu-id="cc992-118">Value</span><span class="sxs-lookup"><span data-stu-id="cc992-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc992-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc992-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc992-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cc992-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc992-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc992-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc992-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc992-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc992-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc992-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc992-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc992-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

