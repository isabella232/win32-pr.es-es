---
title: Estilos de control de calendario mensual (CommCtrl. h)
description: Las constantes de estilo siguientes se usan al crear controles de calendario mensual.
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649715"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="37f1e-103">Estilos de control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="37f1e-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="37f1e-104">Las constantes de estilo siguientes se usan al crear controles de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="37f1e-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="37f1e-105">Constante</span><span class="sxs-lookup"><span data-stu-id="37f1e-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="37f1e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="37f1e-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="37f1e-107"><dt>**MCS \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="37f1e-108">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="37f1e-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="37f1e-109">El calendario mensual envía notificaciones de [MCN \_ GETDAYSTATE](mcn-getdaystate.md) para solicitar información acerca de los días que se deben mostrar en negrita.</span><span class="sxs-lookup"><span data-stu-id="37f1e-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="37f1e-110"><dt>**MCS \_ MULTIselect**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="37f1e-111">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="37f1e-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="37f1e-112">El calendario mensual permite al usuario seleccionar un intervalo de fechas en el control.</span><span class="sxs-lookup"><span data-stu-id="37f1e-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="37f1e-113">De forma predeterminada, el intervalo máximo es de una semana.</span><span class="sxs-lookup"><span data-stu-id="37f1e-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="37f1e-114">Puede cambiar el intervalo máximo que se puede seleccionar mediante el mensaje de [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="37f1e-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="37f1e-115"><dt>**MCS \_ WEEKNUMBERS**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="37f1e-116">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="37f1e-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="37f1e-117">El control de calendario mensual muestra los números de semana (1-52) a la izquierda de cada fila de días.</span><span class="sxs-lookup"><span data-stu-id="37f1e-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="37f1e-118">La semana 1 se define como la primera semana que contiene al menos cuatro días.</span><span class="sxs-lookup"><span data-stu-id="37f1e-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="37f1e-119"><dt>**MCS \_ NOTODAYCIRCLE**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="37f1e-120">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="37f1e-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="37f1e-121">El control de calendario mensual no rodea la fecha "hoy".</span><span class="sxs-lookup"><span data-stu-id="37f1e-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="37f1e-122"><dt>**MCS en la \_ actualidad**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="37f1e-123">[Versión 4,70](common-control-versions.md). El control de calendario mensual no muestra la fecha "hoy" en la parte inferior del control.</span><span class="sxs-lookup"><span data-stu-id="37f1e-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="37f1e-124"><dt>**MCS \_ NOTRAILINGDATES**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="37f1e-125">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="37f1e-125">**Windows Vista.**</span></span> <span data-ttu-id="37f1e-126">Las fechas de los meses anterior y siguiente no se muestran en el calendario del mes actual.</span><span class="sxs-lookup"><span data-stu-id="37f1e-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="37f1e-127"><dt>**MCS \_ SHORTDAYSOFWEEK**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="37f1e-128">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="37f1e-128">**Windows Vista.**</span></span> <span data-ttu-id="37f1e-129">Los nombres de los días cortos se muestran en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="37f1e-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="37f1e-130"><dt>**MCS \_ NOSELCHANGEONNAV**</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="37f1e-131">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="37f1e-131">**Windows Vista.**</span></span> <span data-ttu-id="37f1e-132">La selección no cambia cuando el usuario navega a la siguiente o anterior en el calendario.</span><span class="sxs-lookup"><span data-stu-id="37f1e-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="37f1e-133">Esto permite al usuario seleccionar un intervalo mayor que visible.</span><span class="sxs-lookup"><span data-stu-id="37f1e-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="37f1e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f1e-134">Requirements</span></span>



| <span data-ttu-id="37f1e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f1e-135">Requirement</span></span> | <span data-ttu-id="37f1e-136">Value</span><span class="sxs-lookup"><span data-stu-id="37f1e-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37f1e-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37f1e-137">Header</span></span><br/> | <dl> <span data-ttu-id="37f1e-138"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37f1e-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





