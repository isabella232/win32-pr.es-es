---
Description: Se envía a una ventana después de cambiar su tamaño.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Mensaje de WM_SIZE (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650195"
---
# <a name="wm_size-message"></a><span data-ttu-id="d5c90-103">Mensaje de tamaño de WM \_</span><span class="sxs-lookup"><span data-stu-id="d5c90-103">WM\_SIZE message</span></span>

<span data-ttu-id="d5c90-104">Se envía a una ventana después de cambiar su tamaño.</span><span class="sxs-lookup"><span data-stu-id="d5c90-104">Sent to a window after its size has changed.</span></span>

<span data-ttu-id="d5c90-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="d5c90-105">A window receives this message through its [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a><span data-ttu-id="d5c90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5c90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c90-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5c90-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c90-108">Tipo de cambio de tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="d5c90-108">The type of resizing requested.</span></span> <span data-ttu-id="d5c90-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d5c90-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d5c90-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d5c90-110">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="d5c90-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d5c90-111">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <span data-ttu-id="d5c90-112"><dt>**Tamaño \_ de MAXHIDE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d5c90-112"><dt>**SIZE\_MAXHIDE**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="d5c90-113">El mensaje se envía a todas las ventanas emergentes cuando se maximiza otra ventana.</span><span class="sxs-lookup"><span data-stu-id="d5c90-113">Message is sent to all pop-up windows when some other window is maximized.</span></span><br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <span data-ttu-id="d5c90-114"><dt>**Tamaño \_ de MAXIMIZAdo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d5c90-114"><dt>**SIZE\_MAXIMIZED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="d5c90-115">La ventana se ha maximizado.</span><span class="sxs-lookup"><span data-stu-id="d5c90-115">The window has been maximized.</span></span><br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <span data-ttu-id="d5c90-116"><dt>**Tamaño \_ de MAXSHOW**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d5c90-116"><dt>**SIZE\_MAXSHOW**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="d5c90-117">El mensaje se envía a todas las ventanas emergentes cuando otra ventana se ha restaurado a su tamaño anterior.</span><span class="sxs-lookup"><span data-stu-id="d5c90-117">Message is sent to all pop-up windows when some other window has been restored to its former size.</span></span><br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <span data-ttu-id="d5c90-118"><dt>**Tamaño \_ de MINIMIZAda**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d5c90-118"><dt>**SIZE\_MINIMIZED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d5c90-119">La ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="d5c90-119">The window has been minimized.</span></span><br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <span data-ttu-id="d5c90-120"><dt>**Tamaño \_ de RESTAURAdo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5c90-120"><dt>**SIZE\_RESTORED**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="d5c90-121">Se ha cambiado el tamaño de la ventana, pero no se aplica el valor de **tamaño \_ minimizado** ni **tamaño \_ maximizado** .</span><span class="sxs-lookup"><span data-stu-id="d5c90-121">The window has been resized, but neither the **SIZE\_MINIMIZED** nor **SIZE\_MAXIMIZED** value applies.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d5c90-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5c90-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5c90-123">La palabra de orden inferior de *lParam* especifica el nuevo ancho del área cliente.</span><span class="sxs-lookup"><span data-stu-id="d5c90-123">The low-order word of *lParam* specifies the new width of the client area.</span></span>

<span data-ttu-id="d5c90-124">La palabra de orden superior de *lParam* especifica el nuevo alto del área cliente.</span><span class="sxs-lookup"><span data-stu-id="d5c90-124">The high-order word of *lParam* specifies the new height of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c90-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5c90-125">Return value</span></span>

<span data-ttu-id="d5c90-126">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="d5c90-126">Type: **LRESULT**</span></span>

<span data-ttu-id="d5c90-127">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="d5c90-127">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="d5c90-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d5c90-128">Example</span></span>

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

<span data-ttu-id="d5c90-129">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) en github.</span><span class="sxs-lookup"><span data-stu-id="d5c90-129">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5c90-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5c90-130">Remarks</span></span>

<span data-ttu-id="d5c90-131">Si se llama a la función [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) o [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para una ventana secundaria como resultado del mensaje **de \_ tamaño de WM** , el parámetro *bRedraw* o *bRepaint* debe ser distinto de cero para que la ventana se vuelva a dibujar.</span><span class="sxs-lookup"><span data-stu-id="d5c90-131">If the [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) or [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function is called for a child window as a result of the **WM\_SIZE** message, the *bRedraw* or *bRepaint* parameter should be nonzero to cause the window to be repainted.</span></span>

<span data-ttu-id="d5c90-132">Aunque el ancho y el alto de una ventana son valores de 32 bits, el parámetro *lParam* solo contiene los 16 bits de orden inferior de cada uno.</span><span class="sxs-lookup"><span data-stu-id="d5c90-132">Although the width and height of a window are 32-bit values, the *lParam* parameter contains only the low-order 16 bits of each.</span></span>

<span data-ttu-id="d5c90-133">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** cuando procesa el mensaje de [**\_ WINDOWPOSCHANGED de WM**](wm-windowposchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="d5c90-133">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the **WM\_SIZE** and **WM\_MOVE** messages when it processes the [**WM\_WINDOWPOSCHANGED**](wm-windowposchanged.md) message.</span></span>
<span data-ttu-id="d5c90-134">Los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** no se envían si una aplicación controla el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="d5c90-134">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c90-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c90-135">Requirements</span></span>



| <span data-ttu-id="d5c90-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c90-136">Requirement</span></span> | <span data-ttu-id="d5c90-137">Value</span><span class="sxs-lookup"><span data-stu-id="d5c90-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c90-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c90-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c90-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5c90-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d5c90-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c90-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c90-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5c90-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5c90-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5c90-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c90-143"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5c90-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c90-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c90-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5c90-145">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d5c90-145">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="d5c90-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5c90-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d5c90-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5c90-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5c90-148">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="d5c90-148">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="d5c90-149">**WINDOWPOSCHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d5c90-149">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="d5c90-150">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d5c90-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d5c90-151">Windows</span><span class="sxs-lookup"><span data-stu-id="d5c90-151">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="d5c90-152">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d5c90-152">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d5c90-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="d5c90-153">[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)</span></span>
</dt> </dl>

 

 
