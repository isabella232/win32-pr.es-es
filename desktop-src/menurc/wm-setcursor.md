---
title: Mensaje de WM_SETCURSOR (Winuser. h)
description: Se envía a una ventana si el mouse hace que el cursor se mueva dentro de una ventana y no se captura la entrada del mouse.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079460"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="22ed7-104">Mensaje de SETCURSOR de WM \_</span><span class="sxs-lookup"><span data-stu-id="22ed7-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="22ed7-105">Se envía a una ventana si el mouse hace que el cursor se mueva dentro de una ventana y no se captura la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="22ed7-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="22ed7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22ed7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22ed7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22ed7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22ed7-108">Identificador de la ventana que contiene el cursor.</span><span class="sxs-lookup"><span data-stu-id="22ed7-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="22ed7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22ed7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22ed7-110">La palabra de orden inferior de *lParam* especifica el resultado de la prueba de posicionamiento para la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="22ed7-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="22ed7-111">Vea los valores devueltos de [WM_NCHITTEST](../inputdev/wm-nchittest.md) para ver los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="22ed7-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="22ed7-112">La palabra de orden superior de *lParam* especifica el mensaje de la ventana del mouse que desencadenó este evento, como [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span><span class="sxs-lookup"><span data-stu-id="22ed7-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="22ed7-113">Cuando la ventana entra en el modo de menú, este valor es cero.</span><span class="sxs-lookup"><span data-stu-id="22ed7-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22ed7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22ed7-114">Return value</span></span>

<span data-ttu-id="22ed7-115">Si una aplicación procesa este mensaje, debe devolver **true** para detener el procesamiento más o **false** para continuar.</span><span class="sxs-lookup"><span data-stu-id="22ed7-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="22ed7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22ed7-116">Remarks</span></span>

<span data-ttu-id="22ed7-117">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) pasa el mensaje de **\_ SETCURSOR de WM** a una ventana primaria antes del procesamiento.</span><span class="sxs-lookup"><span data-stu-id="22ed7-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="22ed7-118">Si la ventana primaria devuelve **true**, se detiene el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="22ed7-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="22ed7-119">Al pasar el mensaje a la ventana primaria de una ventana, se proporciona al control de ventana primaria sobre la configuración del cursor en una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="22ed7-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="22ed7-120">La función **DefWindowProc** también usa este mensaje para establecer el cursor en una flecha si no está en el área cliente, o en el cursor de clase registrado si está en el área cliente.</span><span class="sxs-lookup"><span data-stu-id="22ed7-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="22ed7-121">Si la palabra de orden inferior del parámetro *lParam* es **HTERROR** y la palabra de orden superior de *lParam* especifica que uno de los botones del mouse está presionado, **DefWindowProc** llama a la función [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .</span><span class="sxs-lookup"><span data-stu-id="22ed7-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="22ed7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22ed7-122">Requirements</span></span>



| <span data-ttu-id="22ed7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="22ed7-123">Requirement</span></span> | <span data-ttu-id="22ed7-124">Value</span><span class="sxs-lookup"><span data-stu-id="22ed7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ed7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ed7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="22ed7-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="22ed7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22ed7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22ed7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="22ed7-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="22ed7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22ed7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22ed7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="22ed7-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22ed7-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22ed7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="22ed7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="22ed7-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="22ed7-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22ed7-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="22ed7-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="22ed7-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22ed7-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="22ed7-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22ed7-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="22ed7-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="22ed7-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22ed7-137">Cursores</span><span class="sxs-lookup"><span data-stu-id="22ed7-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 

