---
title: Mensaje de MCM_SIZERECTTOMIN (commctrl. h)
description: Calcula cuántos calendarios caben en el rectángulo especificado y, a continuación, devuelve el tamaño mínimo que debe tener un rectángulo para ajustarse a ese número de calendarios. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151053"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="a131f-105">Mensaje de MCM \_ SIZERECTTOMIN</span><span class="sxs-lookup"><span data-stu-id="a131f-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="a131f-106">Calcula cuántos calendarios caben en el rectángulo especificado y, a continuación, devuelve el tamaño mínimo que debe tener un rectángulo para ajustarse a ese número de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a131f-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="a131f-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .</span><span class="sxs-lookup"><span data-stu-id="a131f-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a131f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a131f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a131f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a131f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a131f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a131f-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a131f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a131f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a131f-112">En la entrada, contiene un puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que describe una región que es mayor o igual que el tamaño necesario para ajustarse al número deseado de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a131f-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="a131f-113">Cuando esta función devuelve un valor, contiene la estructura **Rect** mínima que se ajusta a este número de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a131f-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a131f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a131f-114">Return value</span></span>

<span data-ttu-id="a131f-115">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="a131f-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="a131f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a131f-116">Requirements</span></span>



| <span data-ttu-id="a131f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a131f-117">Requirement</span></span> | <span data-ttu-id="a131f-118">Value</span><span class="sxs-lookup"><span data-stu-id="a131f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a131f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a131f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a131f-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a131f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a131f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a131f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a131f-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a131f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a131f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a131f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a131f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a131f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

