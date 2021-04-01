---
description: Establece el texto de una ventana.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Mensaje de WM_SETTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817683"
---
# <a name="wm_settext-message"></a><span data-ttu-id="d892a-103">Mensaje de WM \_ SETTEXT</span><span class="sxs-lookup"><span data-stu-id="d892a-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="d892a-104">Establece el texto de una ventana.</span><span class="sxs-lookup"><span data-stu-id="d892a-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="d892a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d892a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d892a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d892a-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d892a-107">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d892a-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d892a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d892a-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d892a-109">Puntero a una cadena terminada en null que es el texto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d892a-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d892a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d892a-110">Return value</span></span>

<span data-ttu-id="d892a-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d892a-111">Type: **LRESULT**</span></span>

<span data-ttu-id="d892a-112">El valor devuelto es **true** si se establece el texto.</span><span class="sxs-lookup"><span data-stu-id="d892a-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="d892a-113">Es **false** (para un control de edición), **lb \_ ERRSPACE** (para un cuadro de lista) o **CB \_ ERRSPACE** (para un cuadro combinado) si no hay suficiente espacio disponible para establecer el texto en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="d892a-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="d892a-114">Es un **\_ error CB** si este mensaje se envía a un cuadro combinado sin un control de edición.</span><span class="sxs-lookup"><span data-stu-id="d892a-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d892a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d892a-115">Remarks</span></span>

<span data-ttu-id="d892a-116">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece y muestra el texto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d892a-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="d892a-117">Para un control de edición, el texto es el contenido del control de edición.</span><span class="sxs-lookup"><span data-stu-id="d892a-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="d892a-118">En el caso de un cuadro combinado, el texto es el contenido de la parte del control de edición del cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="d892a-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="d892a-119">En el caso de un botón, el texto es el nombre del botón.</span><span class="sxs-lookup"><span data-stu-id="d892a-119">For a button, the text is the button name.</span></span> <span data-ttu-id="d892a-120">Para otras ventanas, el texto es el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="d892a-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="d892a-121">Este mensaje no cambia la selección actual en el cuadro de lista de un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="d892a-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="d892a-122">Una aplicación debe usar el mensaje [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) para seleccionar el elemento en un cuadro de lista que coincida con el texto del control de edición.</span><span class="sxs-lookup"><span data-stu-id="d892a-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d892a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d892a-123">Requirements</span></span>



| <span data-ttu-id="d892a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d892a-124">Requirement</span></span> | <span data-ttu-id="d892a-125">Value</span><span class="sxs-lookup"><span data-stu-id="d892a-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d892a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d892a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d892a-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d892a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d892a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d892a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d892a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d892a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d892a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d892a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d892a-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d892a-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d892a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d892a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="d892a-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d892a-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d892a-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d892a-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d892a-135">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d892a-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="d892a-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d892a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d892a-137">Windows</span><span class="sxs-lookup"><span data-stu-id="d892a-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="d892a-138">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d892a-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d892a-139">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="d892a-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
