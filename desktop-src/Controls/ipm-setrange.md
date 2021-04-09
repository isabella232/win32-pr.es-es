---
title: Mensaje de IPM_SETRANGE (commctrl. h)
description: Establece el intervalo válido para el campo especificado en el control de dirección IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079620"
---
# <a name="ipm_setrange-message"></a><span data-ttu-id="6b23d-104">\_Mensaje IPM SetRange</span><span class="sxs-lookup"><span data-stu-id="6b23d-104">IPM\_SETRANGE message</span></span>

<span data-ttu-id="6b23d-105">Establece el intervalo válido para el campo especificado en el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="6b23d-105">Sets the valid range for the specified field in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b23d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b23d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b23d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b23d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b23d-108">Índice de campo basado en cero al que se aplicará el intervalo.</span><span class="sxs-lookup"><span data-stu-id="6b23d-108">A zero-based field index to which the range will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="6b23d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b23d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b23d-110">Un valor de **palabra** que contiene el límite inferior del intervalo en el byte de orden inferior y el límite superior del byte de orden superior.</span><span class="sxs-lookup"><span data-stu-id="6b23d-110">A **WORD** value that contains the lower limit of the range in the low-order byte and the upper limit in the high-order byte.</span></span> <span data-ttu-id="6b23d-111">Ambos valores son inclusivos.</span><span class="sxs-lookup"><span data-stu-id="6b23d-111">Both of these values are inclusive.</span></span> <span data-ttu-id="6b23d-112">La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) también se puede usar para crear el intervalo.</span><span class="sxs-lookup"><span data-stu-id="6b23d-112">The [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) macro can also be used to create the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b23d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b23d-113">Return value</span></span>

<span data-ttu-id="6b23d-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="6b23d-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b23d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b23d-115">Remarks</span></span>

<span data-ttu-id="6b23d-116">Si el usuario especifica un valor en el campo que está fuera de este intervalo, el control enviará la notificación [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="6b23d-116">If the user enters a value in the field that is outside of this range, the control will send the [IPN\_FIELDCHANGED](ipn-fieldchanged.md) notification with the entered value.</span></span> <span data-ttu-id="6b23d-117">Si el valor todavía está fuera del intervalo después de enviar la notificación, el control intentará cambiar el valor especificado al límite de intervalo más cercano.</span><span class="sxs-lookup"><span data-stu-id="6b23d-117">If the value is still outside of the range after sending the notification, the control will attempt to change the entered value to the closest range limit.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b23d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b23d-118">Requirements</span></span>



| <span data-ttu-id="6b23d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b23d-119">Requirement</span></span> | <span data-ttu-id="6b23d-120">Value</span><span class="sxs-lookup"><span data-stu-id="6b23d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b23d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b23d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b23d-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6b23d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b23d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b23d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b23d-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b23d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b23d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b23d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b23d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b23d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





