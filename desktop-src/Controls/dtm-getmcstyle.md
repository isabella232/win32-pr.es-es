---
title: Mensaje de DTM_GETMCSTYLE (commctrl. h)
description: Obtiene el estilo de un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro GetMonthCalStyle de fecha y hora \_ .
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cae82d271d0e9aece54046527dfa3bedcef657f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996756"
---
# <a name="dtm_getmcstyle-message"></a><span data-ttu-id="51005-105">DTM \_ GETMCSTYLE</span><span class="sxs-lookup"><span data-stu-id="51005-105">DTM\_GETMCSTYLE message</span></span>

<span data-ttu-id="51005-106">Obtiene el estilo de un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="51005-106">Gets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="51005-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetMonthCalStyle de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="51005-107">Send this message explicitly or by using the [**DateTime\_GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51005-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="51005-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51005-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51005-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51005-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="51005-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="51005-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51005-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="51005-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="51005-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51005-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="51005-113">Return value</span></span>

<span data-ttu-id="51005-114">Devuelve el valor de estilo del control.</span><span class="sxs-lookup"><span data-stu-id="51005-114">Returns the style value of the control.</span></span> <span data-ttu-id="51005-115">Para obtener más información, vea [estilos de control de calendario mensual](month-calendar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="51005-115">For more information see [Month Calendar Control Styles](month-calendar-control-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51005-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51005-116">Requirements</span></span>



| <span data-ttu-id="51005-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="51005-117">Requirement</span></span> | <span data-ttu-id="51005-118">Value</span><span class="sxs-lookup"><span data-stu-id="51005-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51005-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51005-119">Minimum supported client</span></span><br/> | <span data-ttu-id="51005-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="51005-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51005-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51005-121">Minimum supported server</span></span><br/> | <span data-ttu-id="51005-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="51005-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51005-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51005-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51005-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51005-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





