---
title: Mensaje de BM_SETCHECK (Winuser. h)
description: Establece el estado de activación de un botón o casilla de radio. Puede enviar este mensaje explícitamente o mediante el botón \_ SetCheck macro.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078952"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="5857a-105">\_Mensaje SETCHECK de BM</span><span class="sxs-lookup"><span data-stu-id="5857a-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="5857a-106">Establece el estado de activación de un botón o casilla de radio.</span><span class="sxs-lookup"><span data-stu-id="5857a-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="5857a-107">Puede enviar este mensaje explícitamente o mediante el [**botón \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span><span class="sxs-lookup"><span data-stu-id="5857a-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5857a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5857a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5857a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5857a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5857a-110">El estado de comprobación.</span><span class="sxs-lookup"><span data-stu-id="5857a-110">The check state.</span></span> <span data-ttu-id="5857a-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5857a-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5857a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5857a-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="5857a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5857a-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="5857a-114"><dt>**BST \_ comprobado**</dt></span><span class="sxs-lookup"><span data-stu-id="5857a-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="5857a-115">Establece el estado del botón en activado.</span><span class="sxs-lookup"><span data-stu-id="5857a-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="5857a-116"><dt>**BST \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="5857a-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="5857a-117">Establece el estado del botón en atenuado, lo que indica un estado indeterminado.</span><span class="sxs-lookup"><span data-stu-id="5857a-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="5857a-118">Use este valor solo si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5857a-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="5857a-119"><dt>**BST \_ DESactivado**</dt></span><span class="sxs-lookup"><span data-stu-id="5857a-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="5857a-120">Establece el estado del botón en desactivado.</span><span class="sxs-lookup"><span data-stu-id="5857a-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="5857a-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5857a-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5857a-122">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5857a-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5857a-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5857a-123">Return value</span></span>

<span data-ttu-id="5857a-124">Este mensaje siempre devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5857a-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5857a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5857a-125">Remarks</span></span>

<span data-ttu-id="5857a-126">El **mensaje \_ SETCHECK de BM** no tiene ningún efecto en los botones de la instalación.</span><span class="sxs-lookup"><span data-stu-id="5857a-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="5857a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5857a-127">Requirements</span></span>



| <span data-ttu-id="5857a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5857a-128">Requirement</span></span> | <span data-ttu-id="5857a-129">Value</span><span class="sxs-lookup"><span data-stu-id="5857a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5857a-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5857a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5857a-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5857a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5857a-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5857a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5857a-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5857a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5857a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5857a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5857a-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5857a-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5857a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5857a-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="5857a-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5857a-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5857a-138">**\_GETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="5857a-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="5857a-139">**\_GETSTATE BM**</span><span class="sxs-lookup"><span data-stu-id="5857a-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="5857a-140">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="5857a-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





