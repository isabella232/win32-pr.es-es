---
title: Mensaje de MCM_SETCOLOR (commctrl. h)
description: Establece el color para una parte determinada de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetColor.
ms.assetid: 4ceb7b0e-82be-474a-a163-7e71356818c0
keywords:
- MCM_SETCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476aafd8356359cf6b4313f4b945253af6b493c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151055"
---
# <a name="mcm_setcolor-message"></a><span data-ttu-id="fbc49-105">Mensaje de MCM \_ SETCOLOR</span><span class="sxs-lookup"><span data-stu-id="fbc49-105">MCM\_SETCOLOR message</span></span>

<span data-ttu-id="fbc49-106">Establece el color para una parte determinada de un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="fbc49-106">Sets the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="fbc49-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) .</span><span class="sxs-lookup"><span data-stu-id="fbc49-107">You can send this message explicitly or by using the [**MonthCal\_SetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fbc49-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbc49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc49-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fbc49-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbc49-110">Valor de tipo **int** que especifica el color de calendario mensual que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="fbc49-110">Value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="fbc49-111">Este valor puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fbc49-111">This value can be one of the following:</span></span>



| <span data-ttu-id="fbc49-112">Value</span><span class="sxs-lookup"><span data-stu-id="fbc49-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="fbc49-113">Significado</span><span class="sxs-lookup"><span data-stu-id="fbc49-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="fbc49-114"><dt>**Fondo de MCSC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="fbc49-115">Establecer el color de fondo que se muestra entre meses.</span><span class="sxs-lookup"><span data-stu-id="fbc49-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="fbc49-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="fbc49-117">Establece el color de fondo que se muestra en el mes.</span><span class="sxs-lookup"><span data-stu-id="fbc49-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="fbc49-118"><dt>**\_texto MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="fbc49-119">Establece el color usado para mostrar el texto dentro de un mes.</span><span class="sxs-lookup"><span data-stu-id="fbc49-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="fbc49-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="fbc49-121">Establezca el color de fondo que se muestra en el título del calendario.</span><span class="sxs-lookup"><span data-stu-id="fbc49-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="fbc49-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="fbc49-123">Establece el color utilizado para mostrar texto en el título del calendario.</span><span class="sxs-lookup"><span data-stu-id="fbc49-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="fbc49-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="fbc49-125">Establezca el color usado para mostrar el texto del día del encabezado y el de los días finales.</span><span class="sxs-lookup"><span data-stu-id="fbc49-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="fbc49-126">Los días de encabezado y final son los días desde los meses anterior y siguiente que aparecen en el calendario mensual actual.</span><span class="sxs-lookup"><span data-stu-id="fbc49-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fbc49-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fbc49-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fbc49-128">Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color que se establecerá para el área especificada del calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="fbc49-128">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc49-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbc49-129">Return value</span></span>

<span data-ttu-id="fbc49-130">Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa la configuración de color anterior para la parte especificada del control de calendario mensual si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="fbc49-130">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="fbc49-131">De lo contrario, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="fbc49-131">Otherwise, the return is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbc49-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbc49-132">Remarks</span></span>

<span data-ttu-id="fbc49-133">Si los estilos visuales están activos, este mensaje no tiene ningún efecto excepto cuando *wParam* es MCSC \_ background.</span><span class="sxs-lookup"><span data-stu-id="fbc49-133">If visual styles are active, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc49-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc49-134">Requirements</span></span>



| <span data-ttu-id="fbc49-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc49-135">Requirement</span></span> | <span data-ttu-id="fbc49-136">Value</span><span class="sxs-lookup"><span data-stu-id="fbc49-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc49-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc49-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc49-138">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fbc49-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fbc49-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc49-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc49-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbc49-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbc49-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbc49-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc49-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc49-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

