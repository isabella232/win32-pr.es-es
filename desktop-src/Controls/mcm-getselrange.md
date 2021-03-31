---
title: Mensaje de MCM_GETSELRANGE (commctrl. h)
description: Recupera información de fecha que representa los límites superior e inferior del intervalo de fechas seleccionado actualmente por el usuario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996215"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="ceacd-105">Mensaje de MCM \_ GETSELRANGE</span><span class="sxs-lookup"><span data-stu-id="ceacd-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="ceacd-106">Recupera información de fecha que representa los límites superior e inferior del intervalo de fechas seleccionado actualmente por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ceacd-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="ceacd-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .</span><span class="sxs-lookup"><span data-stu-id="ceacd-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ceacd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ceacd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceacd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ceacd-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ceacd-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ceacd-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ceacd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ceacd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceacd-112">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que recibirá los límites inferior y superior de la selección del usuario.</span><span class="sxs-lookup"><span data-stu-id="ceacd-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="ceacd-113">Los límites inferior y superior se colocan en *lprgSysTimeArray* \[ 0 \] y *lprgSysTimeArray* \[ 1 \] , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ceacd-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="ceacd-114">Este parámetro debe ser una dirección válida y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="ceacd-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceacd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ceacd-115">Return value</span></span>

<span data-ttu-id="ceacd-116">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="ceacd-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="ceacd-117">**MCM \_ GETSELRANGE** producirá un error si se aplica a un control de calendario mensual que no use el estilo [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ceacd-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceacd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceacd-118">Requirements</span></span>



| <span data-ttu-id="ceacd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceacd-119">Requirement</span></span> | <span data-ttu-id="ceacd-120">Value</span><span class="sxs-lookup"><span data-stu-id="ceacd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ceacd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ceacd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ceacd-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ceacd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ceacd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ceacd-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ceacd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ceacd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ceacd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceacd-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ceacd-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceacd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ceacd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceacd-128">Horas en el control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="ceacd-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

