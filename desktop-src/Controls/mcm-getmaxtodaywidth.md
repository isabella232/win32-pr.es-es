---
title: Mensaje de MCM_GETMAXTODAYWIDTH (commctrl. h)
description: Recupera el ancho máximo del 0034; actualmente \ 0034; cadena en un control de calendario mensual. Esto incluye el texto de la etiqueta y el texto de la fecha. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- MCM_GETMAXTODAYWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802515"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="68b7e-106">Mensaje de MCM \_ GETMAXTODAYWIDTH</span><span class="sxs-lookup"><span data-stu-id="68b7e-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="68b7e-107">Recupera el ancho máximo de la cadena "Today" en un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="68b7e-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="68b7e-108">Esto incluye el texto de la etiqueta y el texto de la fecha.</span><span class="sxs-lookup"><span data-stu-id="68b7e-108">This includes the label text and the date text.</span></span> <span data-ttu-id="68b7e-109">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .</span><span class="sxs-lookup"><span data-stu-id="68b7e-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68b7e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68b7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b7e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68b7e-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="68b7e-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="68b7e-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="68b7e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68b7e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="68b7e-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="68b7e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b7e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68b7e-115">Return value</span></span>

<span data-ttu-id="68b7e-116">Devuelve el ancho de la cadena "Today", en píxeles.</span><span class="sxs-lookup"><span data-stu-id="68b7e-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b7e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b7e-117">Requirements</span></span>



| <span data-ttu-id="68b7e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b7e-118">Requirement</span></span> | <span data-ttu-id="68b7e-119">Value</span><span class="sxs-lookup"><span data-stu-id="68b7e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68b7e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68b7e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="68b7e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68b7e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68b7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68b7e-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="68b7e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68b7e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68b7e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b7e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b7e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





