---
title: Mensaje EM_GETCTFMODEBIAS (RichEdit. h)
description: Obtiene los valores de sesgo del modo de marco de trabajo de servicios de texto para un control Rich Edit de Microsoft.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150406"
---
# <a name="em_getctfmodebias-message"></a><span data-ttu-id="577ee-104">\_Mensaje GETCTFMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="577ee-104">EM\_GETCTFMODEBIAS message</span></span>

<span data-ttu-id="577ee-105">Obtiene los valores de sesgo del modo de marco de trabajo de servicios de texto para un control Rich Edit de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="577ee-105">Gets the Text Services Framework mode bias values for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="577ee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="577ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577ee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="577ee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="577ee-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="577ee-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="577ee-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="577ee-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="577ee-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="577ee-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577ee-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="577ee-111">Return value</span></span>

<span data-ttu-id="577ee-112">Valor de diferencia del modo de marco de servicios de texto actual.</span><span class="sxs-lookup"><span data-stu-id="577ee-112">The current Text Services Framework mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="577ee-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="577ee-113">Remarks</span></span>

<span data-ttu-id="577ee-114">Para obtener la diferencia del modo IME, llame a [**em \_ GETIMEMODEBIAS**](em-getimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="577ee-114">To get the IME mode bias, call [**EM\_GETIMEMODEBIAS**](em-getimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="577ee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="577ee-115">Requirements</span></span>



| <span data-ttu-id="577ee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="577ee-116">Requirement</span></span> | <span data-ttu-id="577ee-117">Value</span><span class="sxs-lookup"><span data-stu-id="577ee-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="577ee-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="577ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="577ee-119">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="577ee-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="577ee-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="577ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="577ee-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="577ee-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="577ee-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="577ee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="577ee-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="577ee-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577ee-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="577ee-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="577ee-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="577ee-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="577ee-126">**\_SETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="577ee-126">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="577ee-127">**\_GETIMEMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="577ee-127">**EM\_GETIMEMODEBIAS**</span></span>](em-getimemodebias.md)
</dt> </dl>

 

 





