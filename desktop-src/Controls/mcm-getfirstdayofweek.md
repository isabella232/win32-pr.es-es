---
title: Mensaje de MCM_GETFIRSTDAYOFWEEK (commctrl. h)
description: Recupera el primer día de la semana de un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658237"
---
# <a name="mcm_getfirstdayofweek-message"></a><span data-ttu-id="2e3ad-105">Mensaje de MCM \_ GETFIRSTDAYOFWEEK</span><span class="sxs-lookup"><span data-stu-id="2e3ad-105">MCM\_GETFIRSTDAYOFWEEK message</span></span>

<span data-ttu-id="2e3ad-106">Recupera el primer día de la semana de un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-106">Retrieves the first day of the week for a month calendar control.</span></span> <span data-ttu-id="2e3ad-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .</span><span class="sxs-lookup"><span data-stu-id="2e3ad-107">You can send this message explicitly or by using the [**MonthCal\_GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e3ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e3ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e3ad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e3ad-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e3ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e3ad-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e3ad-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3ad-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e3ad-113">Return value</span></span>

<span data-ttu-id="2e3ad-114">Devuelve un valor **DWORD** que contiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-114">Returns a **DWORD** value that contains two values.</span></span> <span data-ttu-id="2e3ad-115">La palabra alta es un valor **booleano** que es distinto de cero si el primer día de la semana se establece en un valor distinto de IFIRSTDAYOFWEEK de configuración regional \_ , o bien cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-115">The high word is a **BOOL** value that is nonzero if the first day of the week is set to something other than LOCALE\_IFIRSTDAYOFWEEK, or zero otherwise.</span></span> <span data-ttu-id="2e3ad-116">La palabra baja es un valor INT que representa el primer día de la semana, donde 0 es el lunes, 1 es el martes, etc.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-116">The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3ad-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e3ad-117">Requirements</span></span>



| <span data-ttu-id="2e3ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e3ad-118">Requirement</span></span> | <span data-ttu-id="2e3ad-119">Value</span><span class="sxs-lookup"><span data-stu-id="2e3ad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ad-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e3ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3ad-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2e3ad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e3ad-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e3ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3ad-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e3ad-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e3ad-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e3ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e3ad-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ad-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





