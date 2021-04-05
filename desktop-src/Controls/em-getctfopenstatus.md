---
title: Mensaje EM_GETCTFOPENSTATUS (RichEdit. h)
description: Determina si el teclado de servicios de texto (TSF) está abierto o cerrado.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996505"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="bf2fe-104">\_Mensaje GETCTFOPENSTATUS em</span><span class="sxs-lookup"><span data-stu-id="bf2fe-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="bf2fe-105">Determina si el teclado de servicios de texto (TSF) está abierto o cerrado.</span><span class="sxs-lookup"><span data-stu-id="bf2fe-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf2fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf2fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf2fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2fe-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bf2fe-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf2fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf2fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2fe-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bf2fe-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2fe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf2fe-111">Return value</span></span>

<span data-ttu-id="bf2fe-112">Si el teclado TSF está abierto, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="bf2fe-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="bf2fe-113">De lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="bf2fe-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2fe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf2fe-114">Requirements</span></span>



| <span data-ttu-id="bf2fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2fe-115">Requirement</span></span> | <span data-ttu-id="bf2fe-116">Value</span><span class="sxs-lookup"><span data-stu-id="bf2fe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2fe-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf2fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2fe-118">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf2fe-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf2fe-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf2fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2fe-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf2fe-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf2fe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf2fe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2fe-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2fe-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2fe-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf2fe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2fe-124">**\_SETCTFOPENSTATUS em**</span><span class="sxs-lookup"><span data-stu-id="bf2fe-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





