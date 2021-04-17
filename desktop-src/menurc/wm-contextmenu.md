---
title: Mensaje de WM_CONTEXTMENU (Winuser. h)
description: Notifica a una ventana que el usuario hizo clic con el botón secundario del mouse en la ventana.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714573"
---
# <a name="wm_contextmenu-message"></a><span data-ttu-id="68418-104">Mensaje de CONTEXTMENU de WM \_</span><span class="sxs-lookup"><span data-stu-id="68418-104">WM\_CONTEXTMENU message</span></span>

<span data-ttu-id="68418-105">Notifica a una ventana que el usuario desea que aparezca un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="68418-105">Notifies a window that the user desires a context menu to appear.</span></span>  <span data-ttu-id="68418-106">Es posible que el usuario haya hecho clic con el botón secundario del mouse en la ventana, presionó Mayús + F10 o presionó la tecla aplicaciones (tecla del menú contextual) disponible en algunos teclados.</span><span class="sxs-lookup"><span data-stu-id="68418-106">The user may have clicked the right mouse button (right-clicked) in the window, pressed Shift+F10 or pressed the applications key (context menu key) available on some keyboards.</span></span>


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a><span data-ttu-id="68418-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68418-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68418-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68418-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68418-109">Identificador de la ventana en la que el usuario hizo clic con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="68418-109">A handle to the window in which the user right-clicked the mouse.</span></span> <span data-ttu-id="68418-110">Puede tratarse de una ventana secundaria de la ventana que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="68418-110">This can be a child window of the window receiving the message.</span></span> <span data-ttu-id="68418-111">Para obtener más información sobre el procesamiento de este mensaje, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="68418-111">For more information about processing this message, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="68418-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68418-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68418-113">La palabra de orden inferior especifica la posición horizontal del cursor, en coordenadas de la pantalla, en el momento del clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="68418-113">The low-order word specifies the horizontal position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

<span data-ttu-id="68418-114">La palabra de orden superior especifica la posición vertical del cursor, en coordenadas de pantalla, en el momento del clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="68418-114">The high-order word specifies the vertical position of the cursor, in screen coordinates, at the time of the mouse click.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68418-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68418-115">Return value</span></span>

<span data-ttu-id="68418-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="68418-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68418-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68418-117">Remarks</span></span>

<span data-ttu-id="68418-118">Una ventana puede procesar este mensaje mostrando un menú contextual mediante las funciones [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) o [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .</span><span class="sxs-lookup"><span data-stu-id="68418-118">A window can process this message by displaying a shortcut menu using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) or [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) functions.</span></span> <span data-ttu-id="68418-119">Para obtener las posiciones horizontal y vertical, use el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="68418-119">To obtain the horizontal and vertical positions, use the following code.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="68418-120">Si una ventana no muestra un menú contextual, debe pasar este mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="68418-120">If a window does not display a shortcut menu it should pass this message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="68418-121">Si una ventana es una ventana secundaria, **DefWindowProc** envía el mensaje al elemento primario.</span><span class="sxs-lookup"><span data-stu-id="68418-121">If a window is a child window, **DefWindowProc** sends the message to the parent.</span></span> <span data-ttu-id="68418-122">De lo contrario, **DefWindowProc** muestra un menú contextual predeterminado si la posición especificada está en el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="68418-122">Otherwise, **DefWindowProc** displays a default shortcut menu if the specified position is in the window's caption.</span></span>

<span data-ttu-id="68418-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera el mensaje de **\_ CONTEXTMENU de WM** cuando procesa el mensaje de [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) o cuando el usuario escribe Mayús + F10.</span><span class="sxs-lookup"><span data-stu-id="68418-123">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generates the **WM\_CONTEXTMENU** message when it processes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message or when the user types SHIFT+F10.</span></span> <span data-ttu-id="68418-124">El mensaje de **\_ CONTEXTMENU de WM** también se genera cuando el usuario presiona y libera la clave de [**\_ aplicaciones VK**](/windows/desktop/inputdev/virtual-key-codes) .</span><span class="sxs-lookup"><span data-stu-id="68418-124">The **WM\_CONTEXTMENU** message is also generated when the user presses and releases the [**VK\_APPS**](/windows/desktop/inputdev/virtual-key-codes) key.</span></span>

<span data-ttu-id="68418-125">Si el menú contextual se genera desde el teclado, por ejemplo, si el usuario escribe Mayús + F10, las coordenadas x e y son-1 y la aplicación debe mostrar el menú contextual en la ubicación de la selección actual en lugar de en (xPos, yPos).</span><span class="sxs-lookup"><span data-stu-id="68418-125">If the context menu is generated from the keyboard for example, if the user types SHIFT+F10 then the x- and y-coordinates are -1 and the application should display the context menu at the location of the current selection rather than at (xPos, yPos).</span></span>

## <a name="requirements"></a><span data-ttu-id="68418-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68418-126">Requirements</span></span>



| <span data-ttu-id="68418-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="68418-127">Requirement</span></span> | <span data-ttu-id="68418-128">Value</span><span class="sxs-lookup"><span data-stu-id="68418-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68418-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68418-129">Minimum supported client</span></span><br/> | <span data-ttu-id="68418-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68418-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="68418-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68418-131">Minimum supported server</span></span><br/> | <span data-ttu-id="68418-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68418-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="68418-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68418-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="68418-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68418-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68418-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="68418-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="68418-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="68418-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68418-137">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="68418-137">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="68418-138">**OBTENER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="68418-138">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="68418-139">**OBTENER \_ \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="68418-139">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="68418-140">**TrackPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="68418-140">**TrackPopupMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[<span data-ttu-id="68418-141">**TrackPopupMenuEx**</span><span class="sxs-lookup"><span data-stu-id="68418-141">**TrackPopupMenuEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[<span data-ttu-id="68418-142">**NCRBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="68418-142">**WM\_NCRBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[<span data-ttu-id="68418-143">**RBUTTONUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="68418-143">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

<span data-ttu-id="68418-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="68418-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68418-145">Menús</span><span class="sxs-lookup"><span data-stu-id="68418-145">Menus</span></span>](menus.md)
</dt> </dl>

 

