---
title: Mensaje de WM_COMMAND (Winuser. h)
description: Se envía cuando el usuario selecciona un elemento de comando de un menú, cuando un control envía un mensaje de notificación a su ventana primaria o cuando se traduce una pulsación de tecla de aceleración.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709018"
---
# <a name="wm_command-message"></a><span data-ttu-id="8c42b-104">Mensaje de comando de WM \_</span><span class="sxs-lookup"><span data-stu-id="8c42b-104">WM\_COMMAND message</span></span>

<span data-ttu-id="8c42b-105">Se envía cuando el usuario selecciona un elemento de comando de un menú, cuando un control envía un mensaje de notificación a su ventana primaria o cuando se traduce una pulsación de tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="8c42b-105">Sent when the user selects a command item from a menu, when a control sends a notification message to its parent window, or when an accelerator keystroke is translated.</span></span>


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a><span data-ttu-id="8c42b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c42b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c42b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c42b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c42b-108">Para obtener una descripción de este parámetro, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8c42b-108">For a description of this parameter, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8c42b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c42b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c42b-110">Para obtener una descripción de este parámetro, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8c42b-110">For a description of this parameter, see Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c42b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c42b-111">Return value</span></span>

<span data-ttu-id="8c42b-112">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="8c42b-112">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="8c42b-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c42b-113">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="8c42b-114">Ejemplo tomado de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples) en github.</span><span class="sxs-lookup"><span data-stu-id="8c42b-114">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="8c42b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c42b-115">Remarks</span></span>

<span data-ttu-id="8c42b-116">El uso de los parámetros *wParam* e *lParam* se resume aquí.</span><span class="sxs-lookup"><span data-stu-id="8c42b-116">Use of the *wParam* and *lParam* parameters are summarized here.</span></span>



| <span data-ttu-id="8c42b-117">Origen del mensaje</span><span class="sxs-lookup"><span data-stu-id="8c42b-117">Message Source</span></span> | <span data-ttu-id="8c42b-118">wParam (palabra alta)</span><span class="sxs-lookup"><span data-stu-id="8c42b-118">wParam (high word)</span></span>                | <span data-ttu-id="8c42b-119">wParam (palabra baja)</span><span class="sxs-lookup"><span data-stu-id="8c42b-119">wParam (low word)</span></span>                | <span data-ttu-id="8c42b-120">lParam</span><span class="sxs-lookup"><span data-stu-id="8c42b-120">lParam</span></span>                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| <span data-ttu-id="8c42b-121">Menú</span><span class="sxs-lookup"><span data-stu-id="8c42b-121">Menu</span></span>           | <span data-ttu-id="8c42b-122">0</span><span class="sxs-lookup"><span data-stu-id="8c42b-122">0</span></span>                                 | <span data-ttu-id="8c42b-123">Identificador de menú (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="8c42b-123">Menu identifier (IDM\_\*)</span></span>        | <span data-ttu-id="8c42b-124">0</span><span class="sxs-lookup"><span data-stu-id="8c42b-124">0</span></span>                            |
| <span data-ttu-id="8c42b-125">Acelerador</span><span class="sxs-lookup"><span data-stu-id="8c42b-125">Accelerator</span></span>    | <span data-ttu-id="8c42b-126">1</span><span class="sxs-lookup"><span data-stu-id="8c42b-126">1</span></span>                                 | <span data-ttu-id="8c42b-127">Identificador de acelerador (IDM \_ \* )</span><span class="sxs-lookup"><span data-stu-id="8c42b-127">Accelerator identifier (IDM\_\*)</span></span> | <span data-ttu-id="8c42b-128">0</span><span class="sxs-lookup"><span data-stu-id="8c42b-128">0</span></span>                            |
| <span data-ttu-id="8c42b-129">Control</span><span class="sxs-lookup"><span data-stu-id="8c42b-129">Control</span></span>        | <span data-ttu-id="8c42b-130">Código de notificación definido por el control</span><span class="sxs-lookup"><span data-stu-id="8c42b-130">Control-defined notification code</span></span> | <span data-ttu-id="8c42b-131">Identificador de control</span><span class="sxs-lookup"><span data-stu-id="8c42b-131">Control identifier</span></span>               | <span data-ttu-id="8c42b-132">Identificador de la ventana de control</span><span class="sxs-lookup"><span data-stu-id="8c42b-132">Handle to the control window</span></span> |



 

### <a name="menus"></a><span data-ttu-id="8c42b-133">Menús</span><span class="sxs-lookup"><span data-stu-id="8c42b-133">Menus</span></span>

<span data-ttu-id="8c42b-134">Si una aplicación habilita un separador de menús, el sistema envía un mensaje de **\_ comando de WM** con la palabra baja del parámetro *wParam* establecida en cero cuando el usuario selecciona el separador.</span><span class="sxs-lookup"><span data-stu-id="8c42b-134">If an application enables a menu separator, the system sends a **WM\_COMMAND** message with the low-word of the *wParam* parameter set to zero when the user selects the separator.</span></span>

<span data-ttu-id="8c42b-135">Si se define un menú con un valor [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) de **mns \_ NOTIFYBYPOS**, se envía [**WM \_ MENUCOMMAND**](wm-menucommand.md) en lugar del **\_ comando WM**.</span><span class="sxs-lookup"><span data-stu-id="8c42b-135">If a menu is defined with a [**MENUINFO.dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) value of **MNS\_NOTIFYBYPOS**, [**WM\_MENUCOMMAND**](wm-menucommand.md) is sent instead of **WM\_COMMAND**.</span></span>

### <a name="accelerators"></a><span data-ttu-id="8c42b-136">Aceleradores</span><span class="sxs-lookup"><span data-stu-id="8c42b-136">Accelerators</span></span>

<span data-ttu-id="8c42b-137">Las pulsaciones de teclas de aceleración que seleccionan elementos en el menú ventana se traducen en mensajes [**\_ SYSCOMMAND de WM**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="8c42b-137">Accelerator keystrokes that select items from the window menu are translated into [**WM\_SYSCOMMAND**](wm-syscommand.md) messages.</span></span>

<span data-ttu-id="8c42b-138">Si se produce una pulsación de tecla de aceleración que corresponde a un elemento de menú cuando se minimiza la ventana que posee el menú, no se envía ningún mensaje de **\_ comando de WM** .</span><span class="sxs-lookup"><span data-stu-id="8c42b-138">If an accelerator keystroke occurs that corresponds to a menu item when the window that owns the menu is minimized, no **WM\_COMMAND** message is sent.</span></span> <span data-ttu-id="8c42b-139">Sin embargo, si se produce una pulsación de tecla de aceleración que no coincide con ninguno de los elementos del menú de la ventana o en el menú ventana, se envía un mensaje de **\_ comando de WM** , incluso si la ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="8c42b-139">However, if an accelerator keystroke occurs that does not match any of the items in the window's menu or in the window menu, a **WM\_COMMAND** message is sent, even if the window is minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c42b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c42b-140">Requirements</span></span>



| <span data-ttu-id="8c42b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c42b-141">Requirement</span></span> | <span data-ttu-id="8c42b-142">Value</span><span class="sxs-lookup"><span data-stu-id="8c42b-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c42b-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c42b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8c42b-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c42b-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8c42b-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c42b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8c42b-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c42b-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c42b-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c42b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c42b-148"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c42b-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c42b-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c42b-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c42b-150">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8c42b-150">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="8c42b-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c42b-151">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8c42b-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c42b-152">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8c42b-153">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8c42b-153">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c42b-154">Menús</span><span class="sxs-lookup"><span data-stu-id="8c42b-154">Menus</span></span>](menus.md)
</dt> </dl>

 

