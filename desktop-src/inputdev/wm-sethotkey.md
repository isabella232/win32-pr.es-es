---
title: Mensaje de WM_SETHOTKEY (Winuser. h)
description: Se envía a una ventana para asociar una tecla de acceso rápido a la ventana. Cuando el usuario presiona la tecla de acceso rápido, el sistema activa la ventana.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Entrada de mouse y teclado de mensaje de WM_SETHOTKEY
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "103820375"
---
# <a name="wm_sethotkey-message"></a><span data-ttu-id="4c763-105">Mensaje de SETHOTKEY de WM \_</span><span class="sxs-lookup"><span data-stu-id="4c763-105">WM\_SETHOTKEY message</span></span>

<span data-ttu-id="4c763-106">Se envía a una ventana para asociar una tecla de acceso rápido a la ventana.</span><span class="sxs-lookup"><span data-stu-id="4c763-106">Sent to a window to associate a hot key with the window.</span></span> <span data-ttu-id="4c763-107">Cuando el usuario presiona la tecla de acceso rápido, el sistema activa la ventana.</span><span class="sxs-lookup"><span data-stu-id="4c763-107">When the user presses the hot key, the system activates the window.</span></span>


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a><span data-ttu-id="4c763-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c763-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c763-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c763-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c763-110">La palabra de orden inferior especifica el código de la clave virtual que se va a asociar a la ventana.</span><span class="sxs-lookup"><span data-stu-id="4c763-110">The low-order word specifies the virtual-key code to associate with the window.</span></span>

<span data-ttu-id="4c763-111">La palabra de orden superior puede ser uno o varios de los valores siguientes de CommCtrl. h.</span><span class="sxs-lookup"><span data-stu-id="4c763-111">The high-order word can be one or more of the following values from CommCtrl.h.</span></span>

<span data-ttu-id="4c763-112">Si se establece el valor de *wParam* en **null** , se quita la tecla de acceso rápido asociada a una ventana.</span><span class="sxs-lookup"><span data-stu-id="4c763-112">Setting *wParam* to **NULL** removes the hot key associated with a window.</span></span>



| <span data-ttu-id="4c763-113">Value</span><span class="sxs-lookup"><span data-stu-id="4c763-113">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="4c763-114">Significado</span><span class="sxs-lookup"><span data-stu-id="4c763-114">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <span data-ttu-id="4c763-115"><dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-115"><dt>**HOTKEYF\_ALT**</dt> <dt>0x04</dt></span></span> </dl>             | <span data-ttu-id="4c763-116">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="4c763-116">ALT key</span></span><br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <span data-ttu-id="4c763-117"><dt>**HOTKEYF \_ CONTROL**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-117"><dt>**HOTKEYF\_CONTROL**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="4c763-118">Tecla CTRL</span><span class="sxs-lookup"><span data-stu-id="4c763-118">CTRL key</span></span><br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <span data-ttu-id="4c763-119"><dt>**HOTKEYF \_ EXT**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-119"><dt>**HOTKEYF\_EXT**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="4c763-120">Clave extendida</span><span class="sxs-lookup"><span data-stu-id="4c763-120">Extended key</span></span><br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <span data-ttu-id="4c763-121"><dt>**HOTKEYF \_ Mayús**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-121"><dt>**HOTKEYF\_SHIFT**</dt> <dt>0x01</dt></span></span> </dl>       | <span data-ttu-id="4c763-122">Tecla Mayús</span><span class="sxs-lookup"><span data-stu-id="4c763-122">SHIFT key</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="4c763-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c763-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c763-124">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4c763-124">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c763-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c763-125">Return value</span></span>

<span data-ttu-id="4c763-126">El valor devuelto es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4c763-126">The return value is one of the following.</span></span>



| <span data-ttu-id="4c763-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c763-127">Return value</span></span>                                                                  | <span data-ttu-id="4c763-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c763-128">Description</span></span>                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c763-129"><dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-129"><dt>-1</dt></span></span> </dl> | <span data-ttu-id="4c763-130">La función no se ha realizado correctamente. la tecla de acceso rápido no es válida.</span><span class="sxs-lookup"><span data-stu-id="4c763-130">The function is unsuccessful; the hot key is invalid.</span></span><br/>                        |
| <dl> <span data-ttu-id="4c763-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-131"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="4c763-132">La función no se ha realizado correctamente. la ventana no es válida.</span><span class="sxs-lookup"><span data-stu-id="4c763-132">The function is unsuccessful; the window is invalid.</span></span><br/>                         |
| <dl> <span data-ttu-id="4c763-133"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-133"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="4c763-134">La función se realiza correctamente y ninguna otra ventana tiene la misma tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="4c763-134">The function is successful, and no other window has the same hot key.</span></span><br/>        |
| <dl> <span data-ttu-id="4c763-135"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-135"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="4c763-136">La función es correcta, pero otra ventana ya tiene la misma tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="4c763-136">The function is successful, but another window already has the same hot key.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c763-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c763-137">Remarks</span></span>

<span data-ttu-id="4c763-138">No se puede asociar una tecla de acceso rápido a una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="4c763-138">A hot key cannot be associated with a child window.</span></span>

<span data-ttu-id="4c763-139">**VK \_** Las **\_ pestañas** escape, **\_ espacio VK** y VK son teclas de acceso rápido no válidas.</span><span class="sxs-lookup"><span data-stu-id="4c763-139">**VK\_ESCAPE**, **VK\_SPACE**, and **VK\_TAB** are invalid hot keys.</span></span>

<span data-ttu-id="4c763-140">Cuando el usuario presiona la tecla de acceso rápido, el sistema genera un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) con *wParam* igual a **SC \_ Hotkey** y *lParam* igual al identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="4c763-140">When the user presses the hot key, the system generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message with *wParam* equal to **SC\_HOTKEY** and *lParam* equal to the window's handle.</span></span> <span data-ttu-id="4c763-141">Si este mensaje se pasa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), el sistema llevará el último elemento emergente activo de la ventana (si existe) o la propia ventana (si no hay ninguna ventana emergente) al primer plano.</span><span class="sxs-lookup"><span data-stu-id="4c763-141">If this message is passed on to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the system will bring the window's last active popup (if it exists) or the window itself (if there is no popup window) to the foreground.</span></span>

<span data-ttu-id="4c763-142">Una ventana solo puede tener una tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="4c763-142">A window can only have one hot key.</span></span> <span data-ttu-id="4c763-143">Si la ventana ya tiene una tecla de acceso rápido asociada, la nueva tecla de acceso rápido reemplaza a la antigua.</span><span class="sxs-lookup"><span data-stu-id="4c763-143">If the window already has a hot key associated with it, the new hot key replaces the old one.</span></span> <span data-ttu-id="4c763-144">Si hay más de una ventana con la misma tecla de acceso rápido, la ventana que se activa mediante la tecla de acceso rápido es aleatoria.</span><span class="sxs-lookup"><span data-stu-id="4c763-144">If more than one window has the same hot key, the window that is activated by the hot key is random.</span></span>

<span data-ttu-id="4c763-145">Estas teclas de acceso directo no están relacionadas con las teclas de acceso rápido establecidas por [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span><span class="sxs-lookup"><span data-stu-id="4c763-145">These hot keys are unrelated to the hot keys set by [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c763-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c763-146">Requirements</span></span>



| <span data-ttu-id="4c763-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c763-147">Requirement</span></span> | <span data-ttu-id="4c763-148">Value</span><span class="sxs-lookup"><span data-stu-id="4c763-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c763-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c763-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4c763-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4c763-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4c763-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c763-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4c763-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c763-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4c763-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c763-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c763-154"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c763-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c763-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c763-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c763-156">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4c763-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4c763-157">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="4c763-157">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[<span data-ttu-id="4c763-158">**GETHOTKEY de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4c763-158">**WM\_GETHOTKEY**</span></span>](wm-gethotkey.md)
</dt> <dt>

[<span data-ttu-id="4c763-159">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4c763-159">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="4c763-160">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4c763-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4c763-161">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="4c763-161">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

