---
title: Mensaje EM_SETUNDOLIMIT (RichEdit. h)
description: Establece el número máximo de acciones que pueden almacenarse en la cola de deshacer de un control Rich Edit.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996556"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="ef27d-104">\_Mensaje SETUNDOLIMIT em</span><span class="sxs-lookup"><span data-stu-id="ef27d-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="ef27d-105">Establece el número máximo de acciones que pueden almacenarse en la cola de deshacer de un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ef27d-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ef27d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef27d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef27d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ef27d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef27d-108">Especifica el número máximo de acciones que se pueden almacenar en la cola de deshacer.</span><span class="sxs-lookup"><span data-stu-id="ef27d-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="ef27d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ef27d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ef27d-110">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ef27d-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef27d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef27d-111">Return value</span></span>

<span data-ttu-id="ef27d-112">El valor devuelto es el nuevo número máximo de acciones de deshacer para el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ef27d-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="ef27d-113">Este valor puede ser menor que *wParam* si la memoria es limitada.</span><span class="sxs-lookup"><span data-stu-id="ef27d-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef27d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef27d-114">Remarks</span></span>

<span data-ttu-id="ef27d-115">De forma predeterminada, el número máximo de acciones en la cola de deshacer es 100.</span><span class="sxs-lookup"><span data-stu-id="ef27d-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="ef27d-116">Si aumenta este número, debe haber suficiente memoria disponible para acomodar el nuevo número.</span><span class="sxs-lookup"><span data-stu-id="ef27d-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="ef27d-117">Para mejorar el rendimiento, establezca el límite en el menor valor posible.</span><span class="sxs-lookup"><span data-stu-id="ef27d-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="ef27d-118">Al establecer el límite en cero, se deshabilita la característica **Deshacer** .</span><span class="sxs-lookup"><span data-stu-id="ef27d-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef27d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef27d-119">Requirements</span></span>



| <span data-ttu-id="ef27d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef27d-120">Requirement</span></span> | <span data-ttu-id="ef27d-121">Value</span><span class="sxs-lookup"><span data-stu-id="ef27d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef27d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef27d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef27d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef27d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ef27d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef27d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef27d-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef27d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef27d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef27d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef27d-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef27d-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef27d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef27d-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef27d-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ef27d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ef27d-130">**de \_ em**</span><span class="sxs-lookup"><span data-stu-id="ef27d-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="ef27d-131">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="ef27d-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="ef27d-132">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="ef27d-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="ef27d-133">**rehacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="ef27d-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="ef27d-134">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="ef27d-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





