---
title: Mensaje de WM_COMPAREITEM (Winuser. h)
description: Se envía para determinar la posición relativa de un nuevo elemento en la lista ordenada de un cuadro combinado dibujado por el propietario o un cuadro de lista.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489005"
---
# <a name="wm_compareitem-message"></a><span data-ttu-id="208c6-104">Mensaje de COMPAREITEM de WM \_</span><span class="sxs-lookup"><span data-stu-id="208c6-104">WM\_COMPAREITEM message</span></span>

<span data-ttu-id="208c6-105">Se envía para determinar la posición relativa de un nuevo elemento en la lista ordenada de un cuadro combinado dibujado por el propietario o un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="208c6-105">Sent to determine the relative position of a new item in the sorted list of an owner-drawn combo box or list box.</span></span> <span data-ttu-id="208c6-106">Cada vez que la aplicación agrega un nuevo elemento, el sistema envía este mensaje al propietario de un cuadro combinado o un cuadro de lista creado con el estilo de [**\_ ordenación**](list-box-styles.md) [**CBS \_**](combo-box-styles.md) o lbs.</span><span class="sxs-lookup"><span data-stu-id="208c6-106">Whenever the application adds a new item, the system sends this message to the owner of a combo box or list box created with the [**CBS\_SORT**](combo-box-styles.md) or [**LBS\_SORT**](list-box-styles.md) style.</span></span>


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="208c6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="208c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="208c6-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="208c6-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="208c6-109">Especifica el identificador del control que envió el mensaje de **\_ COMPAREITEM de WM** .</span><span class="sxs-lookup"><span data-stu-id="208c6-109">Specifies the identifier of the control that sent the **WM\_COMPAREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="208c6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="208c6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="208c6-111">Puntero a una estructura [**compareitemstruct (**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) que contiene los identificadores y los datos proporcionados por la aplicación para dos elementos en el cuadro combinado o de lista.</span><span class="sxs-lookup"><span data-stu-id="208c6-111">Pointer to a [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure that contains the identifiers and application-supplied data for two items in the combo or list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="208c6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="208c6-112">Return value</span></span>

<span data-ttu-id="208c6-113">El valor devuelto indica la posición relativa de los dos elementos.</span><span class="sxs-lookup"><span data-stu-id="208c6-113">The return value indicates the relative position of the two items.</span></span> <span data-ttu-id="208c6-114">Puede ser cualquiera de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="208c6-114">It may be any of the values shown in the following table.</span></span>



| <span data-ttu-id="208c6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="208c6-115">Return code</span></span>                                                                          | <span data-ttu-id="208c6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="208c6-116">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="208c6-117"><dt>**Value**</dt></span><span class="sxs-lookup"><span data-stu-id="208c6-117"><dt>**Value**</dt></span></span> </dl> | <span data-ttu-id="208c6-118">Significado</span><span class="sxs-lookup"><span data-stu-id="208c6-118">Meaning</span></span><br/>                                           |
| <dl> <span data-ttu-id="208c6-119"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="208c6-119"><dt>**-1**</dt></span></span> </dl>    | <span data-ttu-id="208c6-120">El elemento 1 precede al elemento 2 en el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="208c6-120">Item 1 precedes item 2 in the sorted order.</span></span><br/>       |
| <dl> <span data-ttu-id="208c6-121"><dt>**0,1**</dt></span><span class="sxs-lookup"><span data-stu-id="208c6-121"><dt>**0**</dt></span></span> </dl>     | <span data-ttu-id="208c6-122">Los elementos 1 y 2 son equivalentes en el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="208c6-122">Items 1 and 2 are equivalent in the sorted order.</span></span><br/> |
| <dl> <span data-ttu-id="208c6-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="208c6-123"><dt>**1**</dt></span></span> </dl>     | <span data-ttu-id="208c6-124">El elemento 1 sigue el elemento 2 en el criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="208c6-124">Item 1 follows item 2 in the sorted order.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="208c6-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="208c6-125">Remarks</span></span>

<span data-ttu-id="208c6-126">Cuando el propietario de un cuadro combinado dibujado por el propietario o un cuadro de lista recibe este mensaje, el propietario devuelve un valor que indica cuál de los elementos especificados por la estructura [**compareitemstruct (**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) aparecerá antes que el otro.</span><span class="sxs-lookup"><span data-stu-id="208c6-126">When the owner of an owner-drawn combo box or list box receives this message, the owner returns a value indicating which of the items specified by the [**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) structure will appear before the other.</span></span> <span data-ttu-id="208c6-127">Normalmente, el sistema envía este mensaje varias veces hasta que determina la posición exacta del nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="208c6-127">Typically, the system sends this message several times until it determines the exact position for the new item.</span></span>

<span data-ttu-id="208c6-128">Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente.</span><span class="sxs-lookup"><span data-stu-id="208c6-128">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="208c6-129">\_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .</span><span class="sxs-lookup"><span data-stu-id="208c6-129">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="208c6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="208c6-130">Requirements</span></span>



| <span data-ttu-id="208c6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="208c6-131">Requirement</span></span> | <span data-ttu-id="208c6-132">Value</span><span class="sxs-lookup"><span data-stu-id="208c6-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208c6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="208c6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="208c6-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="208c6-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="208c6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="208c6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="208c6-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="208c6-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="208c6-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="208c6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="208c6-138"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="208c6-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="208c6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="208c6-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="208c6-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="208c6-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="208c6-141">**COMPAREITEMSTRUCT (**</span><span class="sxs-lookup"><span data-stu-id="208c6-141">**COMPAREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

<span data-ttu-id="208c6-142">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="208c6-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="208c6-143">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="208c6-143">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

