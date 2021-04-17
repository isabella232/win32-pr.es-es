---
title: Mensaje de WM_MENUSELECT (Winuser. h)
description: Se envía a la ventana propietaria de un menú cuando el usuario selecciona un elemento de menú.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714649"
---
# <a name="wm_menuselect-message"></a><span data-ttu-id="901c6-104">Mensaje de MENUSELECT de WM \_</span><span class="sxs-lookup"><span data-stu-id="901c6-104">WM\_MENUSELECT message</span></span>

<span data-ttu-id="901c6-105">Se envía a la ventana propietaria de un menú cuando el usuario selecciona un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="901c6-105">Sent to a menu's owner window when the user selects a menu item.</span></span>


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a><span data-ttu-id="901c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="901c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="901c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="901c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="901c6-108">La palabra de orden inferior especifica el elemento de menú o el índice de submenú.</span><span class="sxs-lookup"><span data-stu-id="901c6-108">The low-order word specifies the menu item or submenu index.</span></span> <span data-ttu-id="901c6-109">Si el elemento seleccionado es un elemento de comando, este parámetro contiene el identificador del elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="901c6-109">If the selected item is a command item, this parameter contains the identifier of the menu item.</span></span> <span data-ttu-id="901c6-110">Si el elemento seleccionado abre un menú desplegable o un submenú, este parámetro contiene el índice del menú desplegable o submenú en el menú principal, y el parámetro *lParam* contiene el identificador del menú principal (en el que se hace clic); Utilice la función [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) para obtener el identificador de menú del menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="901c6-110">If the selected item opens a drop-down menu or submenu, this parameter contains the index of the drop-down menu or submenu in the main menu, and the *lParam* parameter contains the handle to the main (clicked) menu; use the [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) function to get the menu handle to the drop-down menu or submenu.</span></span>

<span data-ttu-id="901c6-111">La palabra de orden superior especifica una o más marcas de menú.</span><span class="sxs-lookup"><span data-stu-id="901c6-111">The high-order word specifies one or more menu flags.</span></span> <span data-ttu-id="901c6-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="901c6-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="901c6-113">Value</span><span class="sxs-lookup"><span data-stu-id="901c6-113">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="901c6-114">Significado</span><span class="sxs-lookup"><span data-stu-id="901c6-114">Meaning</span></span>                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <span data-ttu-id="901c6-115"><dt>**MF \_ MAPA de bits**</dt> <dt>0x00000004L</dt></span><span class="sxs-lookup"><span data-stu-id="901c6-115"><dt>**MF\_BITMAP**</dt> <dt>0x00000004L</dt></span></span> </dl>                | <span data-ttu-id="901c6-116">El elemento muestra un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="901c6-116">Item displays a bitmap.</span></span><br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <span data-ttu-id="901c6-117"><dt>**MF \_**</dt> <dt>0x00000008L</dt> activado</span><span class="sxs-lookup"><span data-stu-id="901c6-117"><dt>**MF\_CHECKED**</dt> <dt>0x00000008L</dt></span></span> </dl>             | <span data-ttu-id="901c6-118">El elemento está activado.</span><span class="sxs-lookup"><span data-stu-id="901c6-118">Item is checked.</span></span><br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <span data-ttu-id="901c6-119"><dt>**MF \_ Deshabilitado**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="901c6-119"><dt>**MF\_DISABLED**</dt> <dt>0x00000002L</dt></span></span> </dl>          | <span data-ttu-id="901c6-120">El elemento está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="901c6-120">Item is disabled.</span></span><br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <span data-ttu-id="901c6-121"><dt>**MF \_ 0x00000001L ATENUAdo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="901c6-121"><dt>**MF\_GRAYED**</dt> <dt>0x00000001L</dt></span></span> </dl>                | <span data-ttu-id="901c6-122">El elemento está atenuado.</span><span class="sxs-lookup"><span data-stu-id="901c6-122">Item is grayed.</span></span><br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <span data-ttu-id="901c6-123"><dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt></span><span class="sxs-lookup"><span data-stu-id="901c6-123"><dt>**MF\_HILITE**</dt> <dt>0x00000080L</dt></span></span> </dl>                | <span data-ttu-id="901c6-124">El elemento está resaltado.</span><span class="sxs-lookup"><span data-stu-id="901c6-124">Item is highlighted.</span></span><br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <span data-ttu-id="901c6-125"><dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt></span><span class="sxs-lookup"><span data-stu-id="901c6-125"><dt>**MF\_MOUSESELECT**</dt> <dt>0x00008000L</dt></span></span> </dl> | <span data-ttu-id="901c6-126">El elemento se selecciona con el mouse.</span><span class="sxs-lookup"><span data-stu-id="901c6-126">Item is selected with the mouse.</span></span><br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <span data-ttu-id="901c6-127"><dt>**MF \_**</dt> <dt>0X00000100L</dt> de OWNERDRAW</span><span class="sxs-lookup"><span data-stu-id="901c6-127"><dt>**MF\_OWNERDRAW**</dt> <dt>0x00000100L</dt></span></span> </dl>       | <span data-ttu-id="901c6-128">El elemento es un elemento dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="901c6-128">Item is an owner-drawn item.</span></span><br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <span data-ttu-id="901c6-129"><dt>**MF \_**</dt> <dt>0x00000010L</dt> emergente</span><span class="sxs-lookup"><span data-stu-id="901c6-129"><dt>**MF\_POPUP**</dt> <dt>0x00000010L</dt></span></span> </dl>                   | <span data-ttu-id="901c6-130">Elemento abre un menú desplegable o un submenú.</span><span class="sxs-lookup"><span data-stu-id="901c6-130">Item opens a drop-down menu or submenu.</span></span><br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <span data-ttu-id="901c6-131"><dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt></span><span class="sxs-lookup"><span data-stu-id="901c6-131"><dt>**MF\_SYSMENU**</dt> <dt>0x00002000L</dt></span></span> </dl>             | <span data-ttu-id="901c6-132">El elemento se encuentra en el menú ventana.</span><span class="sxs-lookup"><span data-stu-id="901c6-132">Item is contained in the window menu.</span></span> <span data-ttu-id="901c6-133">El parámetro *lParam* contiene un identificador para el menú asociado al mensaje.</span><span class="sxs-lookup"><span data-stu-id="901c6-133">The *lParam* parameter contains a handle to the menu associated with the message.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="901c6-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="901c6-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="901c6-135">Identificador del menú en el que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="901c6-135">A handle to the menu that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="901c6-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="901c6-136">Return value</span></span>

<span data-ttu-id="901c6-137">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="901c6-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="901c6-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="901c6-138">Remarks</span></span>

<span data-ttu-id="901c6-139">Si la palabra de orden superior de *wParam* contiene 0xFFFF y el parámetro *lParam* contiene **null**, el sistema ha cerrado el menú.</span><span class="sxs-lookup"><span data-stu-id="901c6-139">If the high-order word of *wParam* contains 0xFFFF and the *lParam* parameter contains **NULL**, the system has closed the menu.</span></span>

<span data-ttu-id="901c6-140">No use el valor 1 para la palabra de orden superior de *wParam*, ya que este valor se especifica como (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span><span class="sxs-lookup"><span data-stu-id="901c6-140">Do not use the value  1 for the high-order word of *wParam*, because this value is specified as (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*).</span></span> <span data-ttu-id="901c6-141">Si el valor es 0xFFFF, se interpretaría como 0x0000FFFF, no como 1, debido a la conversión a **uint**.</span><span class="sxs-lookup"><span data-stu-id="901c6-141">If the value is 0xFFFF, it would be interpreted as 0x0000FFFF, not  1, because of the cast to a **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="901c6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="901c6-142">Requirements</span></span>



| <span data-ttu-id="901c6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="901c6-143">Requirement</span></span> | <span data-ttu-id="901c6-144">Value</span><span class="sxs-lookup"><span data-stu-id="901c6-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="901c6-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="901c6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="901c6-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="901c6-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="901c6-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="901c6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="901c6-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="901c6-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="901c6-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="901c6-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="901c6-150"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="901c6-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="901c6-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="901c6-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="901c6-152">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="901c6-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="901c6-153">**GetSubMenu**</span><span class="sxs-lookup"><span data-stu-id="901c6-153">**GetSubMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

<span data-ttu-id="901c6-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="901c6-154">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="901c6-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="901c6-155">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="901c6-156">**Vista**</span><span class="sxs-lookup"><span data-stu-id="901c6-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="901c6-157">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="901c6-157">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

