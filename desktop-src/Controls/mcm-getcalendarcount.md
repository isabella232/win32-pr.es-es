---
title: Mensaje de MCM_GETCALENDARCOUNT (commctrl. h)
description: Obtiene el número de calendarios que se muestran actualmente en el control de calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a3be9e9bcc5db8c1aab32cacbcc2ded82727af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150661"
---
# <a name="mcm_getcalendarcount-message"></a><span data-ttu-id="9e708-105">Mensaje de MCM \_ GETCALENDARCOUNT</span><span class="sxs-lookup"><span data-stu-id="9e708-105">MCM\_GETCALENDARCOUNT message</span></span>

<span data-ttu-id="9e708-106">Obtiene el número de calendarios que se muestran actualmente en el control de calendario.</span><span class="sxs-lookup"><span data-stu-id="9e708-106">Gets the number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="9e708-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .</span><span class="sxs-lookup"><span data-stu-id="9e708-107">You can send this message explicitly or by using the [**MonthCal\_GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e708-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e708-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e708-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e708-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e708-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e708-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e708-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e708-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e708-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9e708-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e708-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e708-113">Return value</span></span>

<span data-ttu-id="9e708-114">Número de calendarios que se muestran actualmente en el control de calendario.</span><span class="sxs-lookup"><span data-stu-id="9e708-114">Number of calendars currently displayed in the calendar control.</span></span> <span data-ttu-id="9e708-115">El número máximo de calendarios permitidos es 12.</span><span class="sxs-lookup"><span data-stu-id="9e708-115">The maximum number of allowed calendars is 12.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e708-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e708-116">Requirements</span></span>



| <span data-ttu-id="9e708-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e708-117">Requirement</span></span> | <span data-ttu-id="9e708-118">Value</span><span class="sxs-lookup"><span data-stu-id="9e708-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e708-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e708-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e708-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e708-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e708-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e708-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e708-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e708-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e708-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e708-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e708-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e708-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





