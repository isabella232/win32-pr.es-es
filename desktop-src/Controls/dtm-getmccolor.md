---
title: Mensaje de DTM_GETMCCOLOR (commctrl. h)
description: Obtiene el color para una parte determinada del calendario mensual dentro de un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro GetMonthCalColor de fecha y hora \_ .
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- DTM_GETMCCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493348"
---
# <a name="dtm_getmccolor-message"></a><span data-ttu-id="9899d-105">DTM \_ GETMCCOLOR</span><span class="sxs-lookup"><span data-stu-id="9899d-105">DTM\_GETMCCOLOR message</span></span>

<span data-ttu-id="9899d-106">Obtiene el color para una parte determinada del calendario mensual dentro de un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="9899d-106">Gets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="9899d-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCalColor de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="9899d-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9899d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9899d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9899d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9899d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9899d-110">Valor de tipo **int** que especifica el color de calendario mensual que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9899d-110">A value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="9899d-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="9899d-111">This value can be one of the following:</span></span>



| <span data-ttu-id="9899d-112">Value</span><span class="sxs-lookup"><span data-stu-id="9899d-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="9899d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9899d-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="9899d-114"><dt>**Fondo de MCSC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="9899d-115">Recupera el color de fondo que se muestra entre meses.</span><span class="sxs-lookup"><span data-stu-id="9899d-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="9899d-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="9899d-117">Recupera el color de fondo que se muestra en el mes.</span><span class="sxs-lookup"><span data-stu-id="9899d-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="9899d-118"><dt>**\_texto MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="9899d-119">Recupera el color usado para mostrar el texto dentro de un mes.</span><span class="sxs-lookup"><span data-stu-id="9899d-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="9899d-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="9899d-121">Recupera el color de fondo que se muestra en el título del calendario.</span><span class="sxs-lookup"><span data-stu-id="9899d-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="9899d-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="9899d-123">Recupera el color usado para mostrar el texto dentro del título del calendario.</span><span class="sxs-lookup"><span data-stu-id="9899d-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="9899d-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="9899d-125">Recupera el color que se usa para mostrar el texto del día y el final del encabezado.</span><span class="sxs-lookup"><span data-stu-id="9899d-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="9899d-126">Los días de encabezado y final son los días desde los meses anterior y siguiente que aparecen en el calendario mensual actual.</span><span class="sxs-lookup"><span data-stu-id="9899d-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9899d-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9899d-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9899d-128">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9899d-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9899d-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9899d-129">Return value</span></span>

<span data-ttu-id="9899d-130">Devuelve un valor de **COLORREF** que representa la configuración de color para la parte especificada del control de calendario mensual si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="9899d-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="9899d-131">El mensaje devuelve-1 si no se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="9899d-131">The message returns -1 if unsuccessful.</span></span>

## <a name="requirements"></a><span data-ttu-id="9899d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9899d-132">Requirements</span></span>



| <span data-ttu-id="9899d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9899d-133">Requirement</span></span> | <span data-ttu-id="9899d-134">Value</span><span class="sxs-lookup"><span data-stu-id="9899d-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9899d-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9899d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9899d-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9899d-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9899d-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9899d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9899d-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9899d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9899d-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9899d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9899d-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9899d-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





