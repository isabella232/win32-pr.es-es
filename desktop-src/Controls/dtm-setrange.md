---
title: Mensaje de DTM_SETRANGE (commctrl. h)
description: Establece las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la \_ macro DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803068"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="e2fdd-105">\_Mensaje de SetRange DTM</span><span class="sxs-lookup"><span data-stu-id="e2fdd-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="e2fdd-106">Establece las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="e2fdd-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="e2fdd-107">Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .</span><span class="sxs-lookup"><span data-stu-id="e2fdd-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2fdd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2fdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fdd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2fdd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fdd-110">Valor que especifica los valores de intervalo válidos.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="e2fdd-111">Este parámetro puede ser una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e2fdd-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="e2fdd-112">Value</span><span class="sxs-lookup"><span data-stu-id="e2fdd-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="e2fdd-113">Significado</span><span class="sxs-lookup"><span data-stu-id="e2fdd-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="e2fdd-114"><dt>**GDTR \_ mín.**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fdd-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="e2fdd-115">El primer elemento de la matriz de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) es válido y se utilizará para establecer la hora mínima permitida del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="e2fdd-116"><dt>**GDTR \_ máx.**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fdd-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="e2fdd-117">El segundo elemento de la matriz de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) es válido y se utilizará para establecer la hora máxima permitida del sistema.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e2fdd-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2fdd-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fdd-119">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="e2fdd-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="e2fdd-120">El primer elemento de la matriz **SYSTEMTIME** contiene el tiempo mínimo permitido.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="e2fdd-121">El segundo elemento de la matriz **SYSTEMTIME** contiene el tiempo máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="e2fdd-122">No es necesario rellenar un elemento de matriz que no se especifica en el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e2fdd-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fdd-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2fdd-123">Return value</span></span>

<span data-ttu-id="e2fdd-124">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2fdd-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2fdd-125">Remarks</span></span>

<span data-ttu-id="e2fdd-126">En el selector de fecha y hora solo se muestran las fechas y horas que se encuentran dentro del intervalo especificado, lo que impide que el usuario seleccione una fecha y hora fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="e2fdd-127">Si el [**mensaje \_ SETSYSTEMTIME de DTM**](dtm-setsystemtime.md) especifica una fecha y una hora que están fuera del intervalo, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e2fdd-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fdd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2fdd-128">Requirements</span></span>



| <span data-ttu-id="e2fdd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2fdd-129">Requirement</span></span> | <span data-ttu-id="e2fdd-130">Value</span><span class="sxs-lookup"><span data-stu-id="e2fdd-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fdd-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2fdd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e2fdd-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2fdd-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2fdd-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2fdd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e2fdd-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2fdd-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2fdd-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2fdd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2fdd-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2fdd-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

