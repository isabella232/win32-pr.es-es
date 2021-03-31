---
title: Mensaje de EM_GETMARGINS (Winuser. h)
description: Obtiene el ancho de los márgenes izquierdo y derecho de un control de edición.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801375"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="57b52-104">\_Mensaje GETMARGINS em</span><span class="sxs-lookup"><span data-stu-id="57b52-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="57b52-105">Obtiene el ancho de los márgenes izquierdo y derecho de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="57b52-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="57b52-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57b52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b52-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57b52-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57b52-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="57b52-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="57b52-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57b52-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57b52-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="57b52-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b52-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57b52-111">Return value</span></span>

<span data-ttu-id="57b52-112">Devuelve el ancho del margen izquierdo en el LOWORD y el ancho del margen derecho en el HIWORD.</span><span class="sxs-lookup"><span data-stu-id="57b52-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b52-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57b52-113">Remarks</span></span>

<span data-ttu-id="57b52-114">**Edición enriquecida:** No se admite el mensaje **\_ GETMARGINS em** .</span><span class="sxs-lookup"><span data-stu-id="57b52-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b52-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57b52-115">Requirements</span></span>



| <span data-ttu-id="57b52-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b52-116">Requirement</span></span> | <span data-ttu-id="57b52-117">Value</span><span class="sxs-lookup"><span data-stu-id="57b52-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b52-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57b52-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57b52-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="57b52-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="57b52-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57b52-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57b52-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="57b52-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57b52-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57b52-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b52-123"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57b52-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b52-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="57b52-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b52-125">**\_SETMARGINS em**</span><span class="sxs-lookup"><span data-stu-id="57b52-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





