---
title: Mensaje de WM_GETDLGCODE (Winuser. h)
description: Se envía al procedimiento de ventana asociado a un control.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695974"
---
# <a name="wm_getdlgcode-message"></a><span data-ttu-id="c6722-104">Mensaje de GETDLGCODE de WM \_</span><span class="sxs-lookup"><span data-stu-id="c6722-104">WM\_GETDLGCODE message</span></span>

<span data-ttu-id="c6722-105">Se envía al procedimiento de ventana asociado a un control.</span><span class="sxs-lookup"><span data-stu-id="c6722-105">Sent to the window procedure associated with a control.</span></span> <span data-ttu-id="c6722-106">De forma predeterminada, el sistema controla todas las entradas de teclado del control; el sistema interpreta determinados tipos de entradas de teclado como teclas de navegación de cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c6722-106">By default, the system handles all keyboard input to the control; the system interprets certain types of keyboard input as dialog box navigation keys.</span></span> <span data-ttu-id="c6722-107">Para invalidar este comportamiento predeterminado, el control puede responder al mensaje de **\_ GETDLGCODE de WM** para indicar los tipos de entrada que desea procesar.</span><span class="sxs-lookup"><span data-stu-id="c6722-107">To override this default behavior, the control can respond to the **WM\_GETDLGCODE** message to indicate the types of input it wants to process itself.</span></span>


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a><span data-ttu-id="c6722-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6722-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6722-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6722-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6722-110">La clave virtual, presionada por el usuario, que solicitó que Windows emita esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c6722-110">The virtual key, pressed by the user, that prompted Windows to issue this notification.</span></span> <span data-ttu-id="c6722-111">El controlador debe administrar estas claves de forma selectiva.</span><span class="sxs-lookup"><span data-stu-id="c6722-111">The handler must selectively handle these keys.</span></span> <span data-ttu-id="c6722-112">Por ejemplo, el controlador podría aceptar y procesar **VK \_ devolver** , pero delegar **VK \_ Tab** en la ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="c6722-112">For instance, the handler might accept and process **VK\_RETURN** but delegate **VK\_TAB** to the owner window.</span></span> <span data-ttu-id="c6722-113">Para obtener una lista de valores, vea [**códigos de tecla virtual**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="c6722-113">For a list of values, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="c6722-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6722-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6722-115">Puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) (o **null** si el sistema está realizando una consulta).</span><span class="sxs-lookup"><span data-stu-id="c6722-115">A pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure (or **NULL** if the system is performing a query).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6722-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6722-116">Return value</span></span>

<span data-ttu-id="c6722-117">El valor devuelto es uno o varios de los siguientes valores, que indica qué tipo de entrada procesa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c6722-117">The return value is one or more of the following values, indicating which type of input the application processes.</span></span>



| <span data-ttu-id="c6722-118">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6722-118">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="c6722-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6722-119">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6722-120"><dt>**DLGC \_ BOTÓN**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-120"><dt>**DLGC\_BUTTON**</dt> <dt>0x2000</dt></span></span> </dl>          | <span data-ttu-id="c6722-121">Botón.</span><span class="sxs-lookup"><span data-stu-id="c6722-121">Button.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="c6722-122"><dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-122"><dt>**DLGC\_DEFPUSHBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>   | <span data-ttu-id="c6722-123">Botón de opción predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c6722-123">Default push button.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="c6722-124"><dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-124"><dt>**DLGC\_HASSETSEL**</dt> <dt>0x0008</dt></span></span> </dl>       | <span data-ttu-id="c6722-125">[**Em \_ Mensajes SETSEL**](/windows/desktop/Controls/em-setsel) .</span><span class="sxs-lookup"><span data-stu-id="c6722-125">[**EM\_SETSEL**](/windows/desktop/Controls/em-setsel) messages.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="c6722-126"><dt>**DLGC \_ RADIOBUTTON**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-126"><dt>**DLGC\_RADIOBUTTON**</dt> <dt>0x0040</dt></span></span> </dl>     | <span data-ttu-id="c6722-127">Botón de radio.</span><span class="sxs-lookup"><span data-stu-id="c6722-127">Radio button.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="c6722-128"><dt>**DLGC \_**</dt> <dt>0x0100</dt> estática</span><span class="sxs-lookup"><span data-stu-id="c6722-128"><dt>**DLGC\_STATIC**</dt> <dt>0x0100</dt></span></span> </dl>          | <span data-ttu-id="c6722-129">Control estático.</span><span class="sxs-lookup"><span data-stu-id="c6722-129">Static control.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="c6722-130"><dt>**DLGC \_ UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-130"><dt>**DLGC\_UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="c6722-131">Botón de extracción no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c6722-131">Non-default push button.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="c6722-132"><dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-132"><dt>**DLGC\_WANTALLKEYS**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="c6722-133">Todas las entradas de teclado.</span><span class="sxs-lookup"><span data-stu-id="c6722-133">All keyboard input.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="c6722-134"><dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-134"><dt>**DLGC\_WANTARROWS**</dt> <dt>0x0001</dt></span></span> </dl>      | <span data-ttu-id="c6722-135">Teclas de dirección.</span><span class="sxs-lookup"><span data-stu-id="c6722-135">Direction keys.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="c6722-136"><dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-136"><dt>**DLGC\_WANTCHARS**</dt> <dt>0x0080</dt></span></span> </dl>       | <span data-ttu-id="c6722-137">[**WM \_ Mensajes CHAR**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="c6722-137">[**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="c6722-138"><dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-138"><dt>**DLGC\_WANTMESSAGE**</dt> <dt>0x0004</dt></span></span> </dl>     | <span data-ttu-id="c6722-139">Toda la entrada del teclado (la aplicación pasa este mensaje en la estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) al control).</span><span class="sxs-lookup"><span data-stu-id="c6722-139">All keyboard input (the application passes this message in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure to the control).</span></span><br/> |
| <dl> <span data-ttu-id="c6722-140"><dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-140"><dt>**DLGC\_WANTTAB**</dt> <dt>0x0002</dt></span></span> </dl>         | <span data-ttu-id="c6722-141">Tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="c6722-141">TAB key.</span></span><br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c6722-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6722-142">Remarks</span></span>

<span data-ttu-id="c6722-143">Aunque la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) siempre devuelve cero en respuesta al mensaje **de \_ GETDLGCODE de WM** , el procedimiento de ventana para las clases de control predefinidas devuelve un código adecuado para cada clase.</span><span class="sxs-lookup"><span data-stu-id="c6722-143">Although the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function always returns zero in response to the **WM\_GETDLGCODE** message, the window procedure for the predefined control classes return a code appropriate for each class.</span></span>

<span data-ttu-id="c6722-144">El **mensaje \_ GETDLGCODE de WM** y los valores devueltos solo son útiles en los controles de cuadro de diálogo definidos por el usuario o en los controles estándar modificados por subclase.</span><span class="sxs-lookup"><span data-stu-id="c6722-144">The **WM\_GETDLGCODE** message and the returned values are useful only with user-defined dialog box controls or standard controls modified by subclassing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6722-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6722-145">Requirements</span></span>



| <span data-ttu-id="c6722-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6722-146">Requirement</span></span> | <span data-ttu-id="c6722-147">Value</span><span class="sxs-lookup"><span data-stu-id="c6722-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6722-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6722-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c6722-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c6722-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c6722-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6722-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c6722-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6722-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6722-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6722-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6722-153"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6722-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6722-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6722-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6722-155">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c6722-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6722-156">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c6722-156">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c6722-157">**\_SETSEL em**</span><span class="sxs-lookup"><span data-stu-id="c6722-157">**EM\_SETSEL**</span></span>](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[<span data-ttu-id="c6722-158">**MENSAJE**</span><span class="sxs-lookup"><span data-stu-id="c6722-158">**MSG**</span></span>](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[<span data-ttu-id="c6722-159">**carácter de WM \_**</span><span class="sxs-lookup"><span data-stu-id="c6722-159">**WM\_CHAR**</span></span>](/windows/desktop/inputdev/wm-char)
</dt> <dt>

<span data-ttu-id="c6722-160">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c6722-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c6722-161">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="c6722-161">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

