---
title: Mensaje de WM_DPICHANGED (WinUser. h)
description: Se envía cuando cambian los puntos por pulgada (PPP) efectivos de una ventana.
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED máximo de PPP del mensaje
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802527"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="9982e-104">Mensaje de DPICHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="9982e-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="9982e-105">Se envía cuando cambian los puntos por pulgada (PPP) efectivos de una ventana.</span><span class="sxs-lookup"><span data-stu-id="9982e-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="9982e-106">El PPP es el factor de escala de una ventana.</span><span class="sxs-lookup"><span data-stu-id="9982e-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="9982e-107">Hay varios eventos que pueden hacer que el PPP cambie.</span><span class="sxs-lookup"><span data-stu-id="9982e-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="9982e-108">En la lista siguiente se indican las posibles causas del cambio en PPP.</span><span class="sxs-lookup"><span data-stu-id="9982e-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="9982e-109">La ventana se mueve a un nuevo monitor que tiene un PPP diferente.</span><span class="sxs-lookup"><span data-stu-id="9982e-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="9982e-110">El PPP del monitor que hospeda la ventana cambia.</span><span class="sxs-lookup"><span data-stu-id="9982e-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="9982e-111">Los PPP actuales de una ventana siempre son iguales a los últimos PPP enviados por **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="9982e-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="9982e-112">Este es el factor de escala al que se debe ajustar la ventana para los subprocesos que tienen en cuenta los cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="9982e-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="9982e-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9982e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9982e-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9982e-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9982e-115">El [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del *wParam* contiene el valor del eje Y del nuevo PPP de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9982e-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="9982e-116">El [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del *wParam* contiene el valor del eje X del nuevo PPP de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9982e-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="9982e-117">Por ejemplo, 96, 120, 144 o 192.</span><span class="sxs-lookup"><span data-stu-id="9982e-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="9982e-118">Los valores de los ejes X y y son idénticos para las aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="9982e-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="9982e-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9982e-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9982e-120">Puntero a una estructura [**Rect**](/windows/desktop/api/windef/ns-windef-rect) que proporciona un tamaño sugerido y una posición de la ventana actual escalada para el nuevo ppp.</span><span class="sxs-lookup"><span data-stu-id="9982e-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="9982e-121">La expectativa es que las aplicaciones cambien la posición y el tamaño de las ventanas en función de las sugerencias proporcionadas por *lParam* al controlar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9982e-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9982e-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9982e-122">Return value</span></span>

<span data-ttu-id="9982e-123">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="9982e-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9982e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9982e-124">Remarks</span></span>

<span data-ttu-id="9982e-125">Este mensaje solo es relevante para el proceso por las aplicaciones con reconocimiento de **\_ \_ \_ PPP \_ de monitor** o el reconocimiento de PPP por subprocesos que **\_ \_ \_ \_ reconocen el monitor** .</span><span class="sxs-lookup"><span data-stu-id="9982e-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="9982e-126">Puede que se reciba en determinados cambios de PPP si el proceso o la ventana de nivel superior se ejecutan con reconocimiento de **PPP** o con **PPP del sistema**, pero en esas situaciones se puede pasar por alto sin ningún problema.</span><span class="sxs-lookup"><span data-stu-id="9982e-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="9982e-127">Para obtener más información acerca de los diferentes tipos de reconocimiento, vea reconocimiento de [**PPP de proceso \_ \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) y [**\_ reconocimiento de PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span><span class="sxs-lookup"><span data-stu-id="9982e-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="9982e-128">Las versiones anteriores de Windows requerían que el reconocimiento de PPP se asociara en el nivel de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9982e-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="9982e-129">Esas aplicaciones usan **el \_ \_ reconocimiento de PPP de proceso**.</span><span class="sxs-lookup"><span data-stu-id="9982e-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="9982e-130">Actualmente, el reconocimiento de PPP está asociado a los subprocesos y a las ventanas individuales en lugar de a toda la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9982e-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="9982e-131">Estas aplicaciones usan **\_ reconocimiento de PPP**.</span><span class="sxs-lookup"><span data-stu-id="9982e-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="9982e-132">Solo tiene que usar el eje X o el valor del eje Y al escalar la aplicación, ya que son iguales.</span><span class="sxs-lookup"><span data-stu-id="9982e-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="9982e-133">Para controlar este mensaje correctamente, tendrá que cambiar el tamaño y la posición de la ventana en función de las sugerencias proporcionadas por *lParam* y el uso de [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="9982e-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="9982e-134">Si no lo hace, la ventana aumentará o disminuirá con respecto a todo lo demás en el nuevo monitor.</span><span class="sxs-lookup"><span data-stu-id="9982e-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="9982e-135">Por ejemplo, si un usuario usa varios monitores y arrastra la ventana desde un monitor de 96 PPP a un monitor de 192 PPP, parecerá que la ventana es la mitad del tamaño con respecto a otros elementos del monitor de 192 ppp.</span><span class="sxs-lookup"><span data-stu-id="9982e-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="9982e-136">El valor base de DPI se define como **\_ PPP de \_ pantalla \_ predeterminada del usuario** , que se establece en 96.</span><span class="sxs-lookup"><span data-stu-id="9982e-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="9982e-137">Para determinar el factor de escala de un monitor, tome el valor de PPP y divida según los **\_ \_ \_ PPP de pantalla predeterminados del usuario**.</span><span class="sxs-lookup"><span data-stu-id="9982e-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="9982e-138">En la tabla siguiente se proporcionan algunos valores de PPP de ejemplo y los factores de escala asociados.</span><span class="sxs-lookup"><span data-stu-id="9982e-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="9982e-139">Valor de PPP</span><span class="sxs-lookup"><span data-stu-id="9982e-139">DPI value</span></span> | <span data-ttu-id="9982e-140">Porcentaje de escalado</span><span class="sxs-lookup"><span data-stu-id="9982e-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="9982e-141">96</span><span class="sxs-lookup"><span data-stu-id="9982e-141">96</span></span>        | <span data-ttu-id="9982e-142">100%</span><span class="sxs-lookup"><span data-stu-id="9982e-142">100%</span></span>               |
| <span data-ttu-id="9982e-143">120</span><span class="sxs-lookup"><span data-stu-id="9982e-143">120</span></span>       | <span data-ttu-id="9982e-144">125%</span><span class="sxs-lookup"><span data-stu-id="9982e-144">125%</span></span>               |
| <span data-ttu-id="9982e-145">144</span><span class="sxs-lookup"><span data-stu-id="9982e-145">144</span></span>       | <span data-ttu-id="9982e-146">150%</span><span class="sxs-lookup"><span data-stu-id="9982e-146">150%</span></span>               |
| <span data-ttu-id="9982e-147">192</span><span class="sxs-lookup"><span data-stu-id="9982e-147">192</span></span>       | <span data-ttu-id="9982e-148">200%</span><span class="sxs-lookup"><span data-stu-id="9982e-148">200%</span></span>               |



 

<span data-ttu-id="9982e-149">En el ejemplo siguiente se proporciona un controlador de cambio de PPP de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9982e-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="9982e-150">El código siguiente escala linealmente un valor del 100% (96 PPP) a un DPI arbitrario definido por *g \_ DPI*.</span><span class="sxs-lookup"><span data-stu-id="9982e-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="9982e-151">Una manera alternativa de escalar un valor es convertir el valor de PPP en un factor de escala y usarlo.</span><span class="sxs-lookup"><span data-stu-id="9982e-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="9982e-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9982e-152">Requirements</span></span>



| <span data-ttu-id="9982e-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="9982e-153">Requirement</span></span> | <span data-ttu-id="9982e-154">Value</span><span class="sxs-lookup"><span data-stu-id="9982e-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9982e-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9982e-155">Minimum supported client</span></span><br/> | <span data-ttu-id="9982e-156">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9982e-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9982e-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9982e-157">Minimum supported server</span></span><br/> | <span data-ttu-id="9982e-158">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9982e-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9982e-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9982e-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="9982e-160"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9982e-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9982e-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="9982e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9982e-162">**reconocimiento de PPP \_**</span><span class="sxs-lookup"><span data-stu-id="9982e-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="9982e-163">**\_reconocimiento de PPP de proceso \_**</span><span class="sxs-lookup"><span data-stu-id="9982e-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

