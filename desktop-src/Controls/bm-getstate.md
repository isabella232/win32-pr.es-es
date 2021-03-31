---
title: Mensaje de BM_GETSTATE (Winuser. h)
description: Recupera el estado de un botón o una casilla. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button GetState.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995985"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="b36f0-105">\_Mensaje GETSTATE de BM</span><span class="sxs-lookup"><span data-stu-id="b36f0-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="b36f0-106">Recupera el estado de un botón o una casilla.</span><span class="sxs-lookup"><span data-stu-id="b36f0-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="b36f0-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .</span><span class="sxs-lookup"><span data-stu-id="b36f0-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b36f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b36f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b36f0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b36f0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b36f0-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b36f0-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b36f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b36f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b36f0-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b36f0-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b36f0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b36f0-113">Return value</span></span>

<span data-ttu-id="b36f0-114">El valor devuelto especifica el estado actual del botón.</span><span class="sxs-lookup"><span data-stu-id="b36f0-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="b36f0-115">Es una combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b36f0-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="b36f0-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b36f0-116">Return code</span></span>                                                                                        | <span data-ttu-id="b36f0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b36f0-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b36f0-118"><dt>**BST \_ comprobado**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="b36f0-119">El botón está activado.</span><span class="sxs-lookup"><span data-stu-id="b36f0-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="b36f0-120"><dt>**BST \_ DROPDOWNPUSHED**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="b36f0-121">[Windows Vista](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b36f0-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="b36f0-122">El botón está en el estado desplegable.</span><span class="sxs-lookup"><span data-stu-id="b36f0-122">The button is in the drop-down state.</span></span> <span data-ttu-id="b36f0-123">Solo se aplica si el botón tiene el estilo [**\_ desplegable TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b36f0-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="b36f0-124"><dt>**enfoque de BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="b36f0-125">El botón tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="b36f0-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="b36f0-126"><dt>**BST \_ activo**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="b36f0-127">El botón está activo; es decir, el mouse se mantiene sobre él.</span><span class="sxs-lookup"><span data-stu-id="b36f0-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="b36f0-128"><dt>**BST \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="b36f0-129">El estado del botón es indeterminado.</span><span class="sxs-lookup"><span data-stu-id="b36f0-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="b36f0-130">Solo se aplica si el botón tiene el estilo [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b36f0-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="b36f0-131"><dt>**BST \_ insertado**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="b36f0-132">El botón se muestra en el estado insertado.</span><span class="sxs-lookup"><span data-stu-id="b36f0-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="b36f0-133"><dt>**BST \_ DESactivado**</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="b36f0-134">Sin estado especial.</span><span class="sxs-lookup"><span data-stu-id="b36f0-134">No special state.</span></span> <span data-ttu-id="b36f0-135">Equivalente a cero.</span><span class="sxs-lookup"><span data-stu-id="b36f0-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="b36f0-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b36f0-136">Requirements</span></span>



| <span data-ttu-id="b36f0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b36f0-137">Requirement</span></span> | <span data-ttu-id="b36f0-138">Value</span><span class="sxs-lookup"><span data-stu-id="b36f0-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b36f0-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b36f0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b36f0-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b36f0-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b36f0-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b36f0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b36f0-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b36f0-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b36f0-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b36f0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b36f0-144"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b36f0-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b36f0-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="b36f0-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="b36f0-146">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b36f0-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b36f0-147">**\_GETCHECK BM**</span><span class="sxs-lookup"><span data-stu-id="b36f0-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="b36f0-148">**BM \_ SETSTATE**</span><span class="sxs-lookup"><span data-stu-id="b36f0-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





