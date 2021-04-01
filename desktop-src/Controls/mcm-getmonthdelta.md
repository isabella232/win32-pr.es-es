---
title: Mensaje de MCM_GETMONTHDELTA (commctrl. h)
description: Recupera la tasa de desplazamiento para un control de calendario mensual. La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151279"
---
# <a name="mcm_getmonthdelta-message"></a><span data-ttu-id="75db8-106">Mensaje de MCM \_ GETMONTHDELTA</span><span class="sxs-lookup"><span data-stu-id="75db8-106">MCM\_GETMONTHDELTA message</span></span>

<span data-ttu-id="75db8-107">Recupera la tasa de desplazamiento para un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="75db8-107">Retrieves the scroll rate for a month calendar control.</span></span> <span data-ttu-id="75db8-108">La tasa de desplazamiento es el número de meses que el control mueve su presentación cuando el usuario hace clic en un botón de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="75db8-108">The scroll rate is the number of months that the control moves its display when the user clicks a scroll button.</span></span> <span data-ttu-id="75db8-109">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .</span><span class="sxs-lookup"><span data-stu-id="75db8-109">You can send this message explicitly or by using the [**MonthCal\_GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="75db8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75db8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75db8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75db8-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="75db8-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="75db8-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="75db8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75db8-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="75db8-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="75db8-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75db8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75db8-115">Return value</span></span>

<span data-ttu-id="75db8-116">Si la diferencia de mes se estableció previamente mediante el mensaje de [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , devuelve un valor int que representa la tasa de desplazamiento actual del calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="75db8-116">If the month delta was previously set using the [**MCM\_SETMONTHDELTA**](mcm-setmonthdelta.md) message, returns an INT value that represents the month calendar's current scroll rate.</span></span> <span data-ttu-id="75db8-117">Si la diferencia de mes no se estableció previamente con el mensaje de **MCM \_ SETMONTHDELTA** o si la diferencia de mes se restableció al valor predeterminado, devuelve un valor int que representa el número actual de meses visibles.</span><span class="sxs-lookup"><span data-stu-id="75db8-117">If the month delta was not previously set using the **MCM\_SETMONTHDELTA** message, or the month delta was reset to the default, returns an INT value that represents the current number of months visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="75db8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75db8-118">Requirements</span></span>



| <span data-ttu-id="75db8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="75db8-119">Requirement</span></span> | <span data-ttu-id="75db8-120">Value</span><span class="sxs-lookup"><span data-stu-id="75db8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75db8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75db8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="75db8-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="75db8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75db8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75db8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="75db8-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="75db8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75db8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75db8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="75db8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="75db8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





