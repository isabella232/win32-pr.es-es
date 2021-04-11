---
title: Mensaje de HDM_CLEARFILTER (commctrl. h)
description: Borra el filtro de un control de encabezado determinado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header ClearFilter.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150556"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="0648a-105">HDM \_ CLEARFILTER</span><span class="sxs-lookup"><span data-stu-id="0648a-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="0648a-106">Borra el filtro de un control de encabezado determinado.</span><span class="sxs-lookup"><span data-stu-id="0648a-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="0648a-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .</span><span class="sxs-lookup"><span data-stu-id="0648a-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0648a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0648a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0648a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0648a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0648a-110">Un valor de columna que indica qué filtro se va a borrar.</span><span class="sxs-lookup"><span data-stu-id="0648a-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="0648a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0648a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0648a-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0648a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0648a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0648a-113">Return value</span></span>

<span data-ttu-id="0648a-114">Devuelve un entero.</span><span class="sxs-lookup"><span data-stu-id="0648a-114">Returns an integer.</span></span> <span data-ttu-id="0648a-115">**LRESULT** se convierte en un entero que indica **true**(1) o **false**(0).</span><span class="sxs-lookup"><span data-stu-id="0648a-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="0648a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0648a-116">Remarks</span></span>

<span data-ttu-id="0648a-117">Si el valor de la columna se especifica como-1, se borran todos los filtros y la notificación de [ \_ FILTERCHANGE de HDN](hdn-filterchange.md) se envía solo una vez.</span><span class="sxs-lookup"><span data-stu-id="0648a-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="0648a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0648a-118">Requirements</span></span>



| <span data-ttu-id="0648a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0648a-119">Requirement</span></span> | <span data-ttu-id="0648a-120">Value</span><span class="sxs-lookup"><span data-stu-id="0648a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0648a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0648a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0648a-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0648a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0648a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0648a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0648a-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0648a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0648a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0648a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0648a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0648a-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0648a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0648a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0648a-128">**Encabezado \_ ClearAllFilters**</span><span class="sxs-lookup"><span data-stu-id="0648a-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





