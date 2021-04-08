---
title: Solucionar problemas de aplicaciones
description: En esta sección se proporcionan soluciones a problemas comunes.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch, solución de problemas de aplicaciones
- Windows Touch, rechazo de Palm
- rechazo de Palm
- Windows Touch, compatibilidad heredada
- solución de problemas de Windows Touch
- inercia, solución de problemas de aplicaciones
- manipulaciones, solución de problemas de aplicaciones
- gestos, solución de problemas de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1aeb37f139ea9063c07dd7d629ac5579229863
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003488"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="6b393-111">Solucionar problemas de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6b393-111">Troubleshooting Applications</span></span>

<span data-ttu-id="6b393-112">En esta sección se proporcionan soluciones a problemas comunes.</span><span class="sxs-lookup"><span data-stu-id="6b393-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="6b393-113">Solución general de problemas</span><span class="sxs-lookup"><span data-stu-id="6b393-113">General Troubleshooting</span></span>



|          |                                                                                                                                                                                                                                                                                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-114">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-114">Issue</span></span>    | <span data-ttu-id="6b393-115">Ejecuto Windows Server 2008 y las características de Windows Touch no funcionan.</span><span class="sxs-lookup"><span data-stu-id="6b393-115">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="6b393-116">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-116">Cause</span></span>    | <span data-ttu-id="6b393-117">No ha habilitado la experiencia de escritorio.</span><span class="sxs-lookup"><span data-stu-id="6b393-117">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6b393-118">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-118">Solution</span></span> | <span data-ttu-id="6b393-119">Abra la Administrador del servidor herramienta administrativa: haga clic en **Inicio**, seleccione **herramientas administrativas** y, a continuación, haga clic en **Administrador del servidor**.</span><span class="sxs-lookup"><span data-stu-id="6b393-119">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="6b393-120">Haga clic en el elemento **características** en la columna izquierda.</span><span class="sxs-lookup"><span data-stu-id="6b393-120">Click the **Features** item in the left column.</span></span> <span data-ttu-id="6b393-121">Haga clic en **Agregar características** en la sección **características** .</span><span class="sxs-lookup"><span data-stu-id="6b393-121">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="6b393-122">Seleccione **experiencia de escritorio**, haga clic en **siguiente** y, a continuación, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="6b393-122">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



|          |                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-123">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-123">Issue</span></span>    | <span data-ttu-id="6b393-124">Cada vez que mueva el dedo rápidamente por la aplicación, aparece una flecha y el gesto o la manipulación no se registra correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b393-124">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="6b393-125">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-125">Cause</span></span>    | <span data-ttu-id="6b393-126">Tener gestos habilitados cuando no los necesite.</span><span class="sxs-lookup"><span data-stu-id="6b393-126">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="6b393-127">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-127">Solution</span></span> | <span data-ttu-id="6b393-128">Tiene los gestos habilitados cuando desea que se deshabiliten.</span><span class="sxs-lookup"><span data-stu-id="6b393-128">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="6b393-129">Vea [compatibilidad heredada para la panorámica con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md) para obtener información sobre cómo deshabilitar los gestos del lápiz.</span><span class="sxs-lookup"><span data-stu-id="6b393-129">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b393-130">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-130">Issue</span></span></td>
<td><span data-ttu-id="6b393-131">No se puede distinguir entre la entrada del mouse y la entrada táctil de Windows.</span><span class="sxs-lookup"><span data-stu-id="6b393-131">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b393-132">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-132">Cause</span></span></td>
<td><span data-ttu-id="6b393-133">Windows genera mensajes de mouse para la compatibilidad heredada cuando un usuario hace clic en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6b393-133">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b393-134">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-134">Solution</span></span></td>
<td><span data-ttu-id="6b393-135">Puede llamar a <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> para los mensajes <strong>WM_LBUTTONDOWN</strong> y <strong>WM_LBUTTONUP</strong> para determinar el origen.</span><span class="sxs-lookup"><span data-stu-id="6b393-135">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="6b393-136">En el código siguiente se muestra cómo se puede hacer esto.</span><span class="sxs-lookup"><span data-stu-id="6b393-136">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b393-137">C++</span><span class="sxs-lookup"><span data-stu-id="6b393-137">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#define MOUSEEVENTF_FROMTOUCH 0xFF515700

if ((GetMessageExtraInfo() & MOUSEEVENTF_FROMTOUCH) == MOUSEEVENTF_FROMTOUCH) { 
    // Click was generated by wisptis / Windows Touch
}else{ 
    // Click was generated by the mouse.
}
</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



|          |                                                                                    |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-138">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-138">Issue</span></span>    | <span data-ttu-id="6b393-139">Cómo ejecutar aplicaciones de Microsoft PixelSense en Windows 7?</span><span class="sxs-lookup"><span data-stu-id="6b393-139">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="6b393-140">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-140">Cause</span></span>    | <span data-ttu-id="6b393-141">Windows Touch y Microsoft PixelSense son incompatibles.</span><span class="sxs-lookup"><span data-stu-id="6b393-141">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="6b393-142">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-142">Solution</span></span> | <span data-ttu-id="6b393-143">Debe tener como destino la plataforma Windows 7 o la plataforma PixelSense de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6b393-143">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="6b393-144">Solucionar problemas de manipulaciones e inercia</span><span class="sxs-lookup"><span data-stu-id="6b393-144">Troubleshooting Manipulations and Inertia</span></span>



|          |                                                                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-145">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-145">Issue</span></span>    | <span data-ttu-id="6b393-146">Mi aplicación está inmovilizada por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="6b393-146">My application is freezing for no reason.</span></span> <span data-ttu-id="6b393-147">Obtengo infracciones de acceso al inicializar mis interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="6b393-147">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="6b393-148">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-148">Cause</span></span>    | <span data-ttu-id="6b393-149">Falta una llamada a **CoInitialize** al usar las interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) o [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="6b393-149">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="6b393-150">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-150">Solution</span></span> | <span data-ttu-id="6b393-151">Esto puede deberse a la creación de instancias de los objetos del modelo de objetos componentes (COM) de Windows Touch sin llamar a CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="6b393-151">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="6b393-152">Esto sucede a veces cuando se convierten proyectos de mediante gestos al uso de las interfaces de manipulaciones o de inercia.</span><span class="sxs-lookup"><span data-stu-id="6b393-152">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-153">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-153">Issue</span></span>    | <span data-ttu-id="6b393-154">Mi objeto gira incorrectamente cuando se está traduciendo.</span><span class="sxs-lookup"><span data-stu-id="6b393-154">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="6b393-155">La rotación de un solo dedo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b393-155">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6b393-156">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-156">Cause</span></span>    | <span data-ttu-id="6b393-157">Valores dinámicos que se establecen incorrectamente en un objeto.</span><span class="sxs-lookup"><span data-stu-id="6b393-157">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6b393-158">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-158">Solution</span></span> | <span data-ttu-id="6b393-159">No se configuran correctamente los puntos dinámicos de manipulación.</span><span class="sxs-lookup"><span data-stu-id="6b393-159">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="6b393-160">Establezca las propiedades [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) y [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) en el centro del objeto o punto en el que desea girar y establezca la propiedad [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) en el radio del objeto.</span><span class="sxs-lookup"><span data-stu-id="6b393-160">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="6b393-161">Solución de problemas de entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="6b393-161">Troubleshooting Windows Touch Input</span></span>



|          |                                                                                                                                                                                                                                                                                                                                        |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-162">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-162">Issue</span></span>    | <span data-ttu-id="6b393-163">Después de administrar el [**mensaje \_ Touch de WM**](wm-touchdown.md) , se deja de obtener comentarios de límite.</span><span class="sxs-lookup"><span data-stu-id="6b393-163">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="6b393-164">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-164">Cause</span></span>    | <span data-ttu-id="6b393-165">Consume el [**mensaje \_ Touch de WM**](wm-touchdown.md) sin controlarlo.</span><span class="sxs-lookup"><span data-stu-id="6b393-165">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6b393-166">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-166">Solution</span></span> | <span data-ttu-id="6b393-167">Probablemente esté consumiendo un mensaje de Windows Touch sin reenviarlo a **DefWindowProc**, lo que producirá un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="6b393-167">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="6b393-168">Consulte [Introducción con mensajes táctiles de Windows](getting-started-with-multi-touch-messages.md) para obtener más información sobre cómo administrar correctamente los mensajes [**\_ táctiles de WM**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="6b393-168">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b393-169">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-169">Issue</span></span></td>
<td><span data-ttu-id="6b393-170">Estoy incluyendo Windows. h, pero sigue indicando que no se ha definido <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6b393-170">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b393-171">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-171">Cause</span></span></td>
<td><span data-ttu-id="6b393-172">La versión de Windows en Targetver. h no es correcta.</span><span class="sxs-lookup"><span data-stu-id="6b393-172">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b393-173">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-173">Solution</span></span></td>
<td><span data-ttu-id="6b393-174">No ha establecido la versión correcta de Windows en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="6b393-174">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="6b393-175">En el código siguiente se muestran las versiones de Windows correctamente establecidas para Windows Touch en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b393-175">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b393-176">C++</span><span class="sxs-lookup"><span data-stu-id="6b393-176">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifndef WINVER                  // Specify that the minimum required platform is Windows 7.
#define WINVER 0x0601           
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b393-177">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-177">Issue</span></span></td>
<td><span data-ttu-id="6b393-178">Mis coordenadas x e y de entrada táctil parecen no válidos.</span><span class="sxs-lookup"><span data-stu-id="6b393-178">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="6b393-179">Son valores más grandes de lo que se esperan o son valores negativos.</span><span class="sxs-lookup"><span data-stu-id="6b393-179">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b393-180">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-180">Cause</span></span></td>
<td><span data-ttu-id="6b393-181">Es posible que tenga que convertir los puntos táctiles en píxeles, o puede que necesite convertir las coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6b393-181">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b393-182">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-182">Solution</span></span></td>
<td><span data-ttu-id="6b393-183">Asegúrese de que llama a <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> y <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6b393-183">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="6b393-184">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6b393-184">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b393-185">C++</span><span class="sxs-lookup"><span data-stu-id="6b393-185">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>      POINT ptInput;
      if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
        for (int i=0; i < static_cast<INT>(cInputs); i++){
          TOUCHINPUT ti = pInputs[i];                       
          if (ti.dwID != 0){                
            // Do something with your touch input handle.
            ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
            ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
            ScreenToClient(hWnd, &ptInput);
            points[ti.dwID][0] = ptInput.x;
            points[ti.dwID][1] = ptInput.y;
          }
        }
      }</code></pre></td>
</tr>
</tbody>
</table>

<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="6b393-186">Para poder usar la función <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> , debe tener compatibilidad con PPP alta en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b393-186">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="6b393-187">Para obtener más información acerca de la compatibilidad con altas PPP, visite la sección de <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">PPP alta</a> de MSDN.</span><span class="sxs-lookup"><span data-stu-id="6b393-187">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-188">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-188">Issue</span></span>    | <span data-ttu-id="6b393-189">No veo los mensajes [**\_ Touch de WM**](wm-touchdown.md) , pero sé que Windows Touch funciona porque veo mensajes de [**\_ gestos de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="6b393-189">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="6b393-190">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-190">Cause</span></span>    | <span data-ttu-id="6b393-191">Falta una llamada a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="6b393-191">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="6b393-192">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-192">Solution</span></span> | <span data-ttu-id="6b393-193">[**WM \_**](wm-touchdown.md) Los mensajes Touch y de [**\_ gestos de WM**](wm-gesture.md) son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="6b393-193">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="6b393-194">Si no llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), solo recibirá mensajes **de \_ gestos de WM** .</span><span class="sxs-lookup"><span data-stu-id="6b393-194">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



|          |                                                                                                                                                                                                                                                                                                                                                       |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-195">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-195">Issue</span></span>    | <span data-ttu-id="6b393-196">Veo pequeños retrasos desde el momento en que me toca el dedo hasta que obtengo la entrada en mi aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b393-196">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="6b393-197">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-197">Cause</span></span>    | <span data-ttu-id="6b393-198">El rechazo de Palm está causando retrasos en la entrada.</span><span class="sxs-lookup"><span data-stu-id="6b393-198">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="6b393-199">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-199">Solution</span></span> | <span data-ttu-id="6b393-200">Si **TWF \_ WANTPALM** se establece en llamadas a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), se habilita el rechazo de Palm.</span><span class="sxs-lookup"><span data-stu-id="6b393-200">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="6b393-201">Esto provoca un retraso pequeño (100 ms) mientras el software prueba si la entrada procede de un dedo, un lápiz o la palma del usuario.</span><span class="sxs-lookup"><span data-stu-id="6b393-201">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="6b393-202">Deshabilite el rechazo de Palm llamando a **RegisterTouchWindow** con la marca **\_ WANTPALM de TWF** desactivada.</span><span class="sxs-lookup"><span data-stu-id="6b393-202">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="6b393-203">Solución de problemas de gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="6b393-203">Troubleshooting Windows Touch Gestures</span></span>



|          |                                                                                                                                                                                                                                                                                                                                                                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-204">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-204">Issue</span></span>    | <span data-ttu-id="6b393-205">Después de controlar el mensaje de [**\_ gestos de WM**](wm-gesture.md) , se deja de obtener comentarios de límite.</span><span class="sxs-lookup"><span data-stu-id="6b393-205">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="6b393-206">O bien, un gesto que funcionó previamente no funciona ahora.</span><span class="sxs-lookup"><span data-stu-id="6b393-206">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="6b393-207">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-207">Cause</span></span>    | <span data-ttu-id="6b393-208">Consumo del mensaje [**de \_ gestos de WM**](wm-gesture.md) sin controlarlo.</span><span class="sxs-lookup"><span data-stu-id="6b393-208">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="6b393-209">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-209">Solution</span></span> | <span data-ttu-id="6b393-210">Probablemente esté consumiendo un mensaje de Windows Touch sin reenviarlo a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), lo que producirá un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="6b393-210">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="6b393-211">Consulte [Introducción con gestos de Windows](getting-started-with-multi-touch-gestures.md) para obtener más información sobre cómo administrar correctamente los mensajes de [**\_ gestos de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="6b393-211">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



|          |                                                                                                                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-212">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-212">Issue</span></span>    | <span data-ttu-id="6b393-213">No veo mensajes de [**\_ gestos de WM**](wm-gesture.md) , pero sé que el toque de Windows funciona porque veo mensajes [**\_ Touch de WM**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="6b393-213">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="6b393-214">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-214">Cause</span></span>    | <span data-ttu-id="6b393-215">Llamando a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="6b393-215">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="6b393-216">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-216">Solution</span></span> | <span data-ttu-id="6b393-217">[**WM \_**](wm-touchdown.md) Los mensajes Touch y de [**\_ gestos de WM**](wm-gesture.md) son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="6b393-217">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="6b393-218">Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), no recibirá mensajes **de \_ gestos de WM** .</span><span class="sxs-lookup"><span data-stu-id="6b393-218">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b393-219">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-219">Issue</span></span></td>
<td><span data-ttu-id="6b393-220">No veo todos los gestos que espero ver.</span><span class="sxs-lookup"><span data-stu-id="6b393-220">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="6b393-221">Por ejemplo, veo movimientos con el identificador <strong>GID_PAN</strong> pero no <strong>GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b393-221">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b393-222">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-222">Cause</span></span></td>
<td><span data-ttu-id="6b393-223">Algunos gestos, como el gesto girar, no están habilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6b393-223">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b393-224">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-224">Solution</span></span></td>
<td><span data-ttu-id="6b393-225">Debe llamar a <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> cuando reciba un mensaje de <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> como se describe en la referencia de <strong>WM_GESTURENOTIFY</strong> , o bien debe agregar un controlador para el mensaje de <strong>WM_GESTURENOTIFY</strong> .</span><span class="sxs-lookup"><span data-stu-id="6b393-225">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="6b393-226">En el código siguiente se muestra cómo se puede implementar un controlador para habilitar la compatibilidad con la rotación.</span><span class="sxs-lookup"><span data-stu-id="6b393-226">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b393-227">C++</span><span class="sxs-lookup"><span data-stu-id="6b393-227">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// The message map.
BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
     ... ... ...
    ON_MESSAGE(WM_GESTURENOTIFY, OnWindowsGestureNotify)
END_MESSAGE_MAP()  

LRESULT CTestWndApp::OnWindowsGestureNotify(
    UINT    uMsg,
    WPARAM  wParam,
    LPARAM  lParam,
    BOOL&   bHandled
    ){
    GESTURECONFIG gc;
    gc.dwID    = GID_ROTATE; // The gesture identifier.
    gc.dwWant  = GC_ROTATE;  // The gesture command you are enabling for GID_ROTATE.
    gc.dwBlock = 0;          // Don&#39;t block anything.
    UINT uiGcs = 1;          // The number of gestures being set.

  BOOL bResult = SetGestureConfig(g_hMainWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));
    if(!bResult) {
        // Something went wrong, report the error using your preferred logging.
    }

  return 0;
}  </code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b393-228">Para obtener más ejemplos de configuraciones de gestos típicas, vea <strong>SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b393-228">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



|          |                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-229">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-229">Issue</span></span>    | <span data-ttu-id="6b393-230">Las barras de desplazamiento personalizadas en mi aplicación no se desplazan cuando se realiza el movimiento de la panorámica.</span><span class="sxs-lookup"><span data-stu-id="6b393-230">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="6b393-231">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-231">Cause</span></span>    | <span data-ttu-id="6b393-232">Faltan Controladores para los mensajes de desplazamiento de WM correctos \_ \* .</span><span class="sxs-lookup"><span data-stu-id="6b393-232">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="6b393-233">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-233">Solution</span></span> | <span data-ttu-id="6b393-234">No controla todos los mensajes de desplazamiento de WM \_ \* en las barras de desplazamiento personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6b393-234">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="6b393-235">Se recomienda que controle el mensaje [**de \_ gestos de WM**](wm-gesture.md) en lugar de conservar la funcionalidad de barra de desplazamiento personalizada mediante compatibilidad heredada.</span><span class="sxs-lookup"><span data-stu-id="6b393-235">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="6b393-236">Debe admitir los mensajes como se detalla en la sección [compatibilidad heredada para la panorámica con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="6b393-236">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



|          |                                                                                                                                                                                                                                                                 |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b393-237">Problema</span><span class="sxs-lookup"><span data-stu-id="6b393-237">Issue</span></span>    | <span data-ttu-id="6b393-238">Obtengo retrasos de los gestos.</span><span class="sxs-lookup"><span data-stu-id="6b393-238">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="6b393-239">Causa</span><span class="sxs-lookup"><span data-stu-id="6b393-239">Cause</span></span>    | <span data-ttu-id="6b393-240">Los gestos pueden causar retrasos en los movimientos.</span><span class="sxs-lookup"><span data-stu-id="6b393-240">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="6b393-241">Solución</span><span class="sxs-lookup"><span data-stu-id="6b393-241">Solution</span></span> | <span data-ttu-id="6b393-242">Los gestos pueden provocar retrasos durante el tiempo que tarda la aplicación en recibir mensajes de [**\_ gestos de WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="6b393-242">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="6b393-243">Vea [compatibilidad heredada para la panorámica con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md) para obtener información sobre cómo deshabilitar los gestos.</span><span class="sxs-lookup"><span data-stu-id="6b393-243">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6b393-244">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b393-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b393-245">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="6b393-245">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 