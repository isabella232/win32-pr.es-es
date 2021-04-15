---
title: Mensaje de DTM_GETRANGE (commctrl. h)
description: Obtiene las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro GetRange de fecha y hora \_ .
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491825"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="059f7-105">DTM \_ GETRANGE</span><span class="sxs-lookup"><span data-stu-id="059f7-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="059f7-106">Obtiene las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="059f7-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="059f7-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetRange de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .</span><span class="sxs-lookup"><span data-stu-id="059f7-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="059f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="059f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="059f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="059f7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="059f7-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="059f7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="059f7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="059f7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="059f7-112">Puntero a una matriz de dos elementos de estructuras [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="059f7-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="059f7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="059f7-113">Return value</span></span>

<span data-ttu-id="059f7-114">Devuelve un valor **DWORD** que es una combinación de GDTR \_ min o GDTR \_ Max.</span><span class="sxs-lookup"><span data-stu-id="059f7-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="059f7-115">El primer elemento de la matriz [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contiene el tiempo mínimo permitido si \_ se establece GDTR min.</span><span class="sxs-lookup"><span data-stu-id="059f7-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="059f7-116">El segundo elemento de la matriz **SYSTEMTIME** contiene el tiempo máximo permitido si \_ se establece GDTR Max.</span><span class="sxs-lookup"><span data-stu-id="059f7-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="059f7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="059f7-117">Remarks</span></span>

<span data-ttu-id="059f7-118">En el selector de fecha y hora solo se muestran las fechas y horas que se encuentran dentro del intervalo especificado, lo que impide que el usuario seleccione una fecha y hora fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="059f7-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="059f7-119">Si el [**mensaje \_ SETSYSTEMTIME de DTM**](dtm-setsystemtime.md) especifica una fecha y una hora que están fuera del intervalo, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="059f7-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="059f7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="059f7-120">Requirements</span></span>



| <span data-ttu-id="059f7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="059f7-121">Requirement</span></span> | <span data-ttu-id="059f7-122">Value</span><span class="sxs-lookup"><span data-stu-id="059f7-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="059f7-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="059f7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="059f7-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="059f7-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="059f7-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="059f7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="059f7-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="059f7-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="059f7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="059f7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="059f7-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="059f7-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

