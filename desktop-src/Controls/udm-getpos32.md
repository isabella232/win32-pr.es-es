---
title: Mensaje de UDM_GETPOS32 (commctrl. h)
description: Devuelve la posición de 32 bits de un control de flechas.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489617"
---
# <a name="udm_getpos32-message"></a><span data-ttu-id="b0d43-104">\_Mensaje GETPOS32 UDM</span><span class="sxs-lookup"><span data-stu-id="b0d43-104">UDM\_GETPOS32 message</span></span>

<span data-ttu-id="b0d43-105">Devuelve la posición de 32 bits de un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="b0d43-105">Returns the 32-bit position of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0d43-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0d43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d43-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0d43-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d43-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b0d43-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b0d43-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0d43-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0d43-110">Puntero a un valor **booleano** que se establece en cero si el valor se recupera correctamente o es distinto de cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="b0d43-110">Pointer to a **BOOL** value that is set to zero if the value is successfully retrieved or nonzero if an error occurs.</span></span> <span data-ttu-id="b0d43-111">Si este parámetro se establece en **null**, no se registran los errores.</span><span class="sxs-lookup"><span data-stu-id="b0d43-111">If this parameter is set to **NULL**, errors are not reported.</span></span>

<span data-ttu-id="b0d43-112">Si se usa **UDM \_ GETPOS32** en una situación entre procesos, este parámetro debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b0d43-112">If **UDM\_GETPOS32** is used in a cross-process situation, this parameter must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d43-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0d43-113">Return value</span></span>

<span data-ttu-id="b0d43-114">Devuelve la posición de un control de flechas con una precisión de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b0d43-114">Returns the position of an up-down control with 32-bit precision.</span></span> <span data-ttu-id="b0d43-115">Las aplicaciones deben comprobar el valor *lParam* para determinar si el valor devuelto es válido.</span><span class="sxs-lookup"><span data-stu-id="b0d43-115">Applications must check the *lParam* value to determine whether the return value is valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d43-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0d43-116">Remarks</span></span>

<span data-ttu-id="b0d43-117">Al procesar este mensaje, el control de flechas actualiza su posición actual en función del título de la ventana relacionada.</span><span class="sxs-lookup"><span data-stu-id="b0d43-117">When it processes this message, the up-down control updates its current position based on the caption of the buddy window.</span></span> <span data-ttu-id="b0d43-118">Devuelve un error si no hay ninguna ventana relacionada o si el título especifica un valor que no es válido o está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b0d43-118">It returns an error if there is no buddy window or if the caption specifies an invalid or out-of-range value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d43-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0d43-119">Requirements</span></span>



| <span data-ttu-id="b0d43-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0d43-120">Requirement</span></span> | <span data-ttu-id="b0d43-121">Value</span><span class="sxs-lookup"><span data-stu-id="b0d43-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d43-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0d43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d43-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0d43-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0d43-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0d43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d43-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0d43-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0d43-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0d43-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0d43-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d43-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d43-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0d43-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0d43-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b0d43-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0d43-130">**UDM \_ GETPOS**</span><span class="sxs-lookup"><span data-stu-id="b0d43-130">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="b0d43-131">**UDM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="b0d43-131">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="b0d43-132">**UDM \_ SETPOS32**</span><span class="sxs-lookup"><span data-stu-id="b0d43-132">**UDM\_SETPOS32**</span></span>](udm-setpos32.md)
</dt> </dl>

 

 





