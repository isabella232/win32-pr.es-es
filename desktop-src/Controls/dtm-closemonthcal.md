---
title: Mensaje de DTM_CLOSEMONTHCAL (commctrl. h)
description: Cierra un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro CloseMonthCal de fecha y hora \_ .
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078950"
---
# <a name="dtm_closemonthcal-message"></a><span data-ttu-id="d26c0-105">DTM \_ CLOSEMONTHCAL</span><span class="sxs-lookup"><span data-stu-id="d26c0-105">DTM\_CLOSEMONTHCAL message</span></span>

<span data-ttu-id="d26c0-106">Cierra un control de selector de fecha y hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="d26c0-106">Closes a date and time picker (DTP) control.</span></span> <span data-ttu-id="d26c0-107">Envíe este mensaje explícitamente o mediante la [**macro \_ CloseMonthCal de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .</span><span class="sxs-lookup"><span data-stu-id="d26c0-107">Send this message explicitly or by using the [**DateTime\_CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d26c0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d26c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d26c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d26c0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d26c0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d26c0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d26c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d26c0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d26c0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d26c0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d26c0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d26c0-113">Return value</span></span>

<span data-ttu-id="d26c0-114">Devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d26c0-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d26c0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d26c0-115">Remarks</span></span>

<span data-ttu-id="d26c0-116">Destruye el control y envía una notificación [DTN \_ primer plano](dtn-closeup.md) de que el control se está cerrando en lugar de que el control se esté abriendo (colocando como en la notificación de la [ \_ lista desplegable DTN](dtn-dropdown.md) ) en el elemento primario del control.</span><span class="sxs-lookup"><span data-stu-id="d26c0-116">Destroys the control and sends a [DTN\_CLOSEUP](dtn-closeup.md) notification that the control is closing as opposed to the control is opening (dropping-down as in the [DTN\_DROPDOWN](dtn-dropdown.md) notification) to the control's parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d26c0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d26c0-117">Requirements</span></span>



| <span data-ttu-id="d26c0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d26c0-118">Requirement</span></span> | <span data-ttu-id="d26c0-119">Value</span><span class="sxs-lookup"><span data-stu-id="d26c0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d26c0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d26c0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d26c0-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d26c0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d26c0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d26c0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d26c0-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d26c0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d26c0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d26c0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d26c0-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d26c0-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d26c0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d26c0-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d26c0-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d26c0-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d26c0-128">\_lista desplegable DTN</span><span class="sxs-lookup"><span data-stu-id="d26c0-128">DTN\_DROPDOWN</span></span>](dtn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="d26c0-129">DTN \_ primer plano</span><span class="sxs-lookup"><span data-stu-id="d26c0-129">DTN\_CLOSEUP</span></span>](dtn-closeup.md)
</dt> </dl>

 

 





