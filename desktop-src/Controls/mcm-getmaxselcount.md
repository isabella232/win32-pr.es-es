---
title: Mensaje de MCM_GETMAXSELCOUNT (commctrl. h)
description: Recupera el intervalo de fechas máximo que se puede seleccionar en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- MCM_GETMAXSELCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079526"
---
# <a name="mcm_getmaxselcount-message"></a><span data-ttu-id="b545d-105">Mensaje de MCM \_ GETMAXSELCOUNT</span><span class="sxs-lookup"><span data-stu-id="b545d-105">MCM\_GETMAXSELCOUNT message</span></span>

<span data-ttu-id="b545d-106">Recupera el intervalo de fechas máximo que se puede seleccionar en un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="b545d-106">Retrieves the maximum date range that can be selected in a month calendar control.</span></span> <span data-ttu-id="b545d-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="b545d-107">You can send this message explicitly or by using the [**MonthCal\_GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b545d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b545d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b545d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b545d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b545d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b545d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b545d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b545d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b545d-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b545d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b545d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b545d-113">Return value</span></span>

<span data-ttu-id="b545d-114">Devuelve un valor INT que representa el número total de días que se pueden seleccionar para el control.</span><span class="sxs-lookup"><span data-stu-id="b545d-114">Returns an INT value that represents the total number of days that can be selected for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b545d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b545d-115">Remarks</span></span>

<span data-ttu-id="b545d-116">Puede cambiar el intervalo de fechas máximo que se puede seleccionar mediante el mensaje de [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .</span><span class="sxs-lookup"><span data-stu-id="b545d-116">You can change the maximum date range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b545d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b545d-117">Requirements</span></span>



| <span data-ttu-id="b545d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b545d-118">Requirement</span></span> | <span data-ttu-id="b545d-119">Value</span><span class="sxs-lookup"><span data-stu-id="b545d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b545d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b545d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b545d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b545d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b545d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b545d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b545d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b545d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b545d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b545d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b545d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b545d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





