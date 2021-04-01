---
title: Mensaje de MCM_GETCOLOR (commctrl. h)
description: Recupera el color para una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetColor.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150878"
---
# <a name="mcm_getcolor-message"></a><span data-ttu-id="4256a-105">Mensaje de GETCOLOR de MCM \_</span><span class="sxs-lookup"><span data-stu-id="4256a-105">MCM\_GETCOLOR message</span></span>

<span data-ttu-id="4256a-106">Recupera el color para una parte determinada de un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="4256a-106">Retrieves the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="4256a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) .</span><span class="sxs-lookup"><span data-stu-id="4256a-107">You can send this message explicitly or by using the [**MonthCal\_GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4256a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4256a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4256a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4256a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4256a-110">Valor de tipo **int** que especifica el color de calendario mensual que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4256a-110">Value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="4256a-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4256a-111">This value can be one of the following:</span></span>



| <span data-ttu-id="4256a-112">Value</span><span class="sxs-lookup"><span data-stu-id="4256a-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="4256a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="4256a-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="4256a-114"><dt>**Fondo de MCSC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="4256a-115">Recupera el color de fondo que se muestra entre meses.</span><span class="sxs-lookup"><span data-stu-id="4256a-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="4256a-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="4256a-117">Recupera el color de fondo que se muestra en el mes.</span><span class="sxs-lookup"><span data-stu-id="4256a-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="4256a-118"><dt>**\_texto MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="4256a-119">Recupera el color usado para mostrar el texto dentro de un mes.</span><span class="sxs-lookup"><span data-stu-id="4256a-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="4256a-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="4256a-121">Recupera el color de fondo que se muestra en el título del calendario.</span><span class="sxs-lookup"><span data-stu-id="4256a-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="4256a-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="4256a-123">Recupera el color usado para mostrar el texto dentro del título del calendario.</span><span class="sxs-lookup"><span data-stu-id="4256a-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="4256a-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="4256a-125">Recupera el color que se usa para mostrar el texto del día y el final del encabezado.</span><span class="sxs-lookup"><span data-stu-id="4256a-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="4256a-126">Los días de encabezado y final son los días desde los meses anterior y siguiente que aparecen en el calendario mensual actual.</span><span class="sxs-lookup"><span data-stu-id="4256a-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4256a-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4256a-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4256a-128">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4256a-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4256a-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4256a-129">Return value</span></span>

<span data-ttu-id="4256a-130">Devuelve un valor de **COLORREF** que representa la configuración de color para la parte especificada del control de calendario mensual si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4256a-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="4256a-131">De lo contrario, este mensaje devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="4256a-131">Otherwise, this message returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="4256a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4256a-132">Requirements</span></span>



| <span data-ttu-id="4256a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4256a-133">Requirement</span></span> | <span data-ttu-id="4256a-134">Value</span><span class="sxs-lookup"><span data-stu-id="4256a-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4256a-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4256a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4256a-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4256a-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4256a-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4256a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4256a-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4256a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4256a-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4256a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="4256a-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4256a-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





