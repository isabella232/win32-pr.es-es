---
title: Mensaje de MCM_SETSELRANGE (commctrl. h)
description: Establece la selección de un control de calendario mensual en un intervalo de fechas determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078933"
---
# <a name="mcm_setselrange-message"></a><span data-ttu-id="f2f72-105">Mensaje de MCM \_ SETSELRANGE</span><span class="sxs-lookup"><span data-stu-id="f2f72-105">MCM\_SETSELRANGE message</span></span>

<span data-ttu-id="f2f72-106">Establece la selección de un control de calendario mensual en un intervalo de fechas determinado.</span><span class="sxs-lookup"><span data-stu-id="f2f72-106">Sets the selection for a month calendar control to a given date range.</span></span> <span data-ttu-id="f2f72-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .</span><span class="sxs-lookup"><span data-stu-id="f2f72-107">You can send this message explicitly or by using the [**MonthCal\_SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2f72-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f72-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2f72-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2f72-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f2f72-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2f72-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2f72-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2f72-112">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contienen información de fecha que representa los límites de la selección.</span><span class="sxs-lookup"><span data-stu-id="f2f72-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain date information representing the selection limits.</span></span> <span data-ttu-id="f2f72-113">La primera fecha seleccionada se debe especificar en *lpSysTimeArray* \[ 0 \] y la última fecha seleccionada debe especificarse en *lpSysTimeArray* \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="f2f72-113">The first selected date must be specified in *lpSysTimeArray*\[0\], and the last selected date must be specified in *lpSysTimeArray*\[1\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f72-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f72-114">Return value</span></span>

<span data-ttu-id="f2f72-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f2f72-115">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="f2f72-116">Se producirá un error en este mensaje si se aplica a un control de calendario mensual que no use el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f72-116">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f72-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f72-117">Requirements</span></span>



| <span data-ttu-id="f2f72-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f72-118">Requirement</span></span> | <span data-ttu-id="f2f72-119">Value</span><span class="sxs-lookup"><span data-stu-id="f2f72-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f72-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f72-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f72-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2f72-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f2f72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f72-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f2f72-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2f72-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f72-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2f72-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f72-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2f72-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f72-127">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="f2f72-127">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

