---
title: Mensaje de MCM_GETCALID (commctrl. h)
description: Obtiene el identificador de calendario para el control de calendario determinado. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb4a780d5107a7761d7dcac9b27a7cb01f3de744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150405"
---
# <a name="mcm_getcalid-message"></a><span data-ttu-id="d062a-105">Mensaje de MCM \_ GETCALID</span><span class="sxs-lookup"><span data-stu-id="d062a-105">MCM\_GETCALID message</span></span>

<span data-ttu-id="d062a-106">Obtiene el identificador de calendario para el control de calendario determinado.</span><span class="sxs-lookup"><span data-stu-id="d062a-106">Gets the calendar ID for the given calendar control.</span></span> <span data-ttu-id="d062a-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .</span><span class="sxs-lookup"><span data-stu-id="d062a-107">You can send this message explicitly or by using the [**MonthCal\_GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d062a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d062a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d062a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d062a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d062a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d062a-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d062a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d062a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d062a-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d062a-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d062a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d062a-113">Return value</span></span>

<span data-ttu-id="d062a-114">IDENTIFICADOR del calendario actual.</span><span class="sxs-lookup"><span data-stu-id="d062a-114">ID of the current calendar.</span></span> <span data-ttu-id="d062a-115">Una de las constantes de los [identificadores de calendario](/windows/desktop/Intl/calendar-identifiers) .</span><span class="sxs-lookup"><span data-stu-id="d062a-115">One of the [Calendar Identifiers](/windows/desktop/Intl/calendar-identifiers) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="d062a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d062a-116">Requirements</span></span>



| <span data-ttu-id="d062a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d062a-117">Requirement</span></span> | <span data-ttu-id="d062a-118">Value</span><span class="sxs-lookup"><span data-stu-id="d062a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d062a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d062a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d062a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d062a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d062a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d062a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d062a-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d062a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d062a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d062a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d062a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d062a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

