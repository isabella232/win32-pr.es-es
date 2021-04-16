---
title: Mensaje de TBM_GETSELSTART (commctrl. h)
description: Recupera la posición inicial del intervalo de selección actual en una barra de inicio.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- TBM_GETSELSTART controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af796c57adb3615241a8f5b702ff58062468509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658200"
---
# <a name="tbm_getselstart-message"></a><span data-ttu-id="d1957-104">TBM \_ GETSELSTART</span><span class="sxs-lookup"><span data-stu-id="d1957-104">TBM\_GETSELSTART message</span></span>

<span data-ttu-id="d1957-105">Recupera la posición inicial del intervalo de selección actual en una barra de inicio.</span><span class="sxs-lookup"><span data-stu-id="d1957-105">Retrieves the starting position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1957-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1957-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1957-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d1957-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d1957-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d1957-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1957-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1957-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d1957-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1957-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1957-111">Return value</span></span>

<span data-ttu-id="d1957-112">Devuelve un valor de 32 bits que especifica la posición inicial del intervalo de selección actual.</span><span class="sxs-lookup"><span data-stu-id="d1957-112">Returns a 32-bit value that specifies the starting position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1957-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1957-113">Remarks</span></span>

<span data-ttu-id="d1957-114">Una barra de nivel solo puede tener un intervalo de selección si se especificó el estilo [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) al crearlo.</span><span class="sxs-lookup"><span data-stu-id="d1957-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1957-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1957-115">Requirements</span></span>



| <span data-ttu-id="d1957-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1957-116">Requirement</span></span> | <span data-ttu-id="d1957-117">Value</span><span class="sxs-lookup"><span data-stu-id="d1957-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1957-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1957-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1957-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d1957-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1957-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1957-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1957-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1957-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1957-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1957-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1957-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1957-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1957-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1957-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1957-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d1957-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1957-126">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="d1957-126">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="d1957-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="d1957-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="d1957-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="d1957-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="d1957-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="d1957-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





