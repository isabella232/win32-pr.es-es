---
title: Mensaje de HDM_SETFILTERCHANGETIMEOUT (commctrl. h)
description: Establece el intervalo de tiempo de espera entre el momento en que se produce un cambio en los atributos de filtro y el envío de una notificación de FILTERCHANGE de HDN \_ . Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetFilterChangeTimeout.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079621"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="e9b3f-105">HDM \_ SETFILTERCHANGETIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e9b3f-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="e9b3f-106">Establece el intervalo de tiempo de espera entre el momento en que se produce un cambio en los atributos de filtro y el envío de una notificación de [ \_ FILTERCHANGE de HDN](hdn-filterchange.md) .</span><span class="sxs-lookup"><span data-stu-id="e9b3f-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="e9b3f-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .</span><span class="sxs-lookup"><span data-stu-id="e9b3f-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9b3f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9b3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9b3f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e9b3f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e9b3f-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e9b3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9b3f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e9b3f-112">El valor del tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9b3f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9b3f-113">Return value</span></span>

<span data-ttu-id="e9b3f-114">Devuelve el índice del control de filtro que se está modificando.</span><span class="sxs-lookup"><span data-stu-id="e9b3f-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9b3f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9b3f-115">Requirements</span></span>



| <span data-ttu-id="e9b3f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9b3f-116">Requirement</span></span> | <span data-ttu-id="e9b3f-117">Value</span><span class="sxs-lookup"><span data-stu-id="e9b3f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9b3f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9b3f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e9b3f-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e9b3f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9b3f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9b3f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e9b3f-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9b3f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9b3f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9b3f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9b3f-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9b3f-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9b3f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9b3f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9b3f-125">HDN \_ FILTERCHANGE</span><span class="sxs-lookup"><span data-stu-id="e9b3f-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





