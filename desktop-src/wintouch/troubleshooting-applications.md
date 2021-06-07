---
title: Solución de problemas de aplicaciones
description: En esta sección se ofrecen soluciones a problemas comunes.
ms.assetid: dfdc5a97-aa0a-4011-8f61-6e405e28b6f8
keywords:
- Windows Touch, solución de problemas de aplicaciones
- Windows Touch, rechazo de palm
- rechazo de la mano
- Windows Touch, compatibilidad heredada
- solución de problemas de Windows Touch
- inercia, solución de problemas de aplicaciones
- manipulaciones, solución de problemas de aplicaciones
- gestos, solución de problemas de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389d200cedc57b7f128a535355b12a9288c6e9eb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443156"
---
# <a name="troubleshooting-applications"></a><span data-ttu-id="ac774-111">Solución de problemas de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ac774-111">Troubleshooting Applications</span></span>

<span data-ttu-id="ac774-112">En esta sección se ofrecen soluciones a problemas comunes.</span><span class="sxs-lookup"><span data-stu-id="ac774-112">This section gives solutions to common problems.</span></span>

## <a name="general-troubleshooting"></a><span data-ttu-id="ac774-113">Solución general de problemas</span><span class="sxs-lookup"><span data-stu-id="ac774-113">General Troubleshooting</span></span>



| <span data-ttu-id="ac774-114">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-114">Category</span></span> | <span data-ttu-id="ac774-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-115">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-116">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-116">Issue</span></span>    | <span data-ttu-id="ac774-117">Estoy ejecutando Windows Server 2008 y las características de Windows Touch no funcionan.</span><span class="sxs-lookup"><span data-stu-id="ac774-117">I am running Windows Server 2008 and Windows Touch features are not working.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="ac774-118">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-118">Cause</span></span>    | <span data-ttu-id="ac774-119">No ha habilitado la experiencia de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ac774-119">You haven't enabled the Desktop Experience.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ac774-120">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-120">Solution</span></span> | <span data-ttu-id="ac774-121">Abra la herramienta Administrador del servidor administrativa: haga **clic** en Inicio , seleccione Herramientas **administrativas** y, a continuación, haga clic **Administrador del servidor**.</span><span class="sxs-lookup"><span data-stu-id="ac774-121">Open the Server Manager administrative tool: click **Start**, point to **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="ac774-122">Haga clic en **el elemento** Características de la columna izquierda.</span><span class="sxs-lookup"><span data-stu-id="ac774-122">Click the **Features** item in the left column.</span></span> <span data-ttu-id="ac774-123">Haga **clic en Agregar** características en la **sección** Características.</span><span class="sxs-lookup"><span data-stu-id="ac774-123">Click **Add Features** in the **Features** section.</span></span> <span data-ttu-id="ac774-124">Seleccione **Experiencia de escritorio,** haga clic **en Siguiente** y, a continuación, haga clic **en Instalar.**</span><span class="sxs-lookup"><span data-stu-id="ac774-124">Select **Desktop Experience**, click **Next**, and then click **Install**.</span></span> |



 



| <span data-ttu-id="ac774-125">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-125">Category</span></span> | <span data-ttu-id="ac774-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-126">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-127">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-127">Issue</span></span>    | <span data-ttu-id="ac774-128">Cada vez que mudo el dedo rápidamente por la aplicación, aparece una flecha y mi gesto o manipulación no se registra correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac774-128">Whenever I move my finger quickly across my application, an arrow appears and my gesture or manipulation is not registering correctly.</span></span>                                                             |
| <span data-ttu-id="ac774-129">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-129">Cause</span></span>    | <span data-ttu-id="ac774-130">Tener habilitados los gestos cuando no lo necesite.</span><span class="sxs-lookup"><span data-stu-id="ac774-130">Having flicks enabled when you don't need it.</span></span>                                                                                                                                                      |
| <span data-ttu-id="ac774-131">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-131">Solution</span></span> | <span data-ttu-id="ac774-132">Tiene los gestos habilitados cuando desea que se deshabilite.</span><span class="sxs-lookup"><span data-stu-id="ac774-132">You have flicks enabled when you want it to be disabled.</span></span> <span data-ttu-id="ac774-133">Consulte [Compatibilidad heredada con desplazamiento](legacy-support-for-panning-with-scrollbars.md) panorámico con barras de desplazamiento para obtener información sobre cómo deshabilitar los gestos de lápiz.</span><span class="sxs-lookup"><span data-stu-id="ac774-133">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling pen flicks.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac774-134">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-134">Issue</span></span></td>
<td><span data-ttu-id="ac774-135">No puedo distinguir entre la entrada del mouse y la entrada de Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="ac774-135">I can't discern between mouse input and Windows Touch input.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac774-136">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-136">Cause</span></span></td>
<td><span data-ttu-id="ac774-137">Windows genera mensajes del mouse para la compatibilidad heredada cuando un usuario hace clic en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ac774-137">Windows generates mouse messages for legacy support when a user clicks on the screen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac774-138">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-138">Solution</span></span></td>
<td><span data-ttu-id="ac774-139">Puede llamar a <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo para</a> <strong>el</strong> WM_LBUTTONDOWN y <strong>WM_LBUTTONUP</strong> para determinar el origen.</span><span class="sxs-lookup"><span data-stu-id="ac774-139">You can call <a href="/windows/win32/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a> for the <strong>WM_LBUTTONDOWN</strong> and <strong>WM_LBUTTONUP</strong> messages to determine the source.</span></span> <span data-ttu-id="ac774-140">El código siguiente muestra cómo se podría hacer esto.</span><span class="sxs-lookup"><span data-stu-id="ac774-140">The following code shows how this could be done.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac774-141">C++</span><span class="sxs-lookup"><span data-stu-id="ac774-141">C++</span></span></th>
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



 



| <span data-ttu-id="ac774-142">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-142">Category</span></span> | <span data-ttu-id="ac774-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-143">Description</span></span> |
|----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-144">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-144">Issue</span></span>    | <span data-ttu-id="ac774-145">Cómo ejecutar aplicaciones de Microsoft PixelSense en Windows 7?</span><span class="sxs-lookup"><span data-stu-id="ac774-145">How do I run Microsoft PixelSense applications on Windows 7?</span></span>                       |
| <span data-ttu-id="ac774-146">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-146">Cause</span></span>    | <span data-ttu-id="ac774-147">Windows Touch y Microsoft PixelSense no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="ac774-147">Windows Touch and Microsoft PixelSense are incompatible.</span></span>                           |
| <span data-ttu-id="ac774-148">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-148">Solution</span></span> | <span data-ttu-id="ac774-149">Debe tener como destino la plataforma Windows 7 o la plataforma Microsoft PixelSense.</span><span class="sxs-lookup"><span data-stu-id="ac774-149">You either need to target the Windows 7 platform or Microsoft PixelSense platform.</span></span> |



 

## <a name="troubleshooting-manipulations-and-inertia"></a><span data-ttu-id="ac774-150">Solución de problemas de manipulaciones e inercia</span><span class="sxs-lookup"><span data-stu-id="ac774-150">Troubleshooting Manipulations and Inertia</span></span>



| <span data-ttu-id="ac774-151">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-151">Category</span></span> | <span data-ttu-id="ac774-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-152">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-153">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-153">Issue</span></span>    | <span data-ttu-id="ac774-154">Mi aplicación se está inmovilizando sin motivo alguno.</span><span class="sxs-lookup"><span data-stu-id="ac774-154">My application is freezing for no reason.</span></span> <span data-ttu-id="ac774-155">Obtendrá infracciones de acceso al inicializar las interfaces de objeto.</span><span class="sxs-lookup"><span data-stu-id="ac774-155">I'm getting access violations when I initialize my object interfaces.</span></span>                                                                                                                                          |
| <span data-ttu-id="ac774-156">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-156">Cause</span></span>    | <span data-ttu-id="ac774-157">Falta una llamada a **CoInitialize** cuando se usan las interfaces [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) [**o IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)</span><span class="sxs-lookup"><span data-stu-id="ac774-157">Missing a call to **CoInitialize** when using the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) or [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interfaces.</span></span>                                                                                 |
| <span data-ttu-id="ac774-158">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-158">Solution</span></span> | <span data-ttu-id="ac774-159">Esto podría deberse a la creación de instancias de los objetos del Modelo de objetos componentes (COM) de Windows Touch sin llamar a CoInitialize.</span><span class="sxs-lookup"><span data-stu-id="ac774-159">This could be caused by instantiating the Windows Touch Component Object Model (COM) objects without calling CoInitialize.</span></span> <span data-ttu-id="ac774-160">Esto sucede a veces cuando se convierten proyectos de usar gestos a usar las manipulaciones o interfaces de inercia.</span><span class="sxs-lookup"><span data-stu-id="ac774-160">This happens sometimes when you are converting projects from using gestures to using the manipulations or inertia interfaces.</span></span> |



 



| <span data-ttu-id="ac774-161">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-161">Category</span></span> | <span data-ttu-id="ac774-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-162">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-163">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-163">Issue</span></span>    | <span data-ttu-id="ac774-164">Mi objeto se está girando incorrectamente cuando se está traduciendo.</span><span class="sxs-lookup"><span data-stu-id="ac774-164">My object is rotating improperly when it's being translated.</span></span> <span data-ttu-id="ac774-165">La rotación con un solo dedo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac774-165">Single-finger rotation is not working correctly.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ac774-166">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-166">Cause</span></span>    | <span data-ttu-id="ac774-167">Establecer incorrectamente pivotes en un objeto .</span><span class="sxs-lookup"><span data-stu-id="ac774-167">Improperly setting pivots on an object.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ac774-168">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-168">Solution</span></span> | <span data-ttu-id="ac774-169">No está configurando correctamente los puntos de pivote de manipulación.</span><span class="sxs-lookup"><span data-stu-id="ac774-169">You are not setting up the manipulation pivot points correctly.</span></span> <span data-ttu-id="ac774-170">Establezca las [**propiedades PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) y [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) en el centro del objeto o punto en el que desea girar y establezca la propiedad [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) en el radio del objeto.</span><span class="sxs-lookup"><span data-stu-id="ac774-170">Set the [**PivotPointX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx) and [**PivotPointY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy) properties to the center of the object or point you want to rotate around, and set the [**PivotRadius**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) property to the radius of your object.</span></span> |



 

## <a name="troubleshooting-windows-touch-input"></a><span data-ttu-id="ac774-171">Solución de problemas de entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="ac774-171">Troubleshooting Windows Touch Input</span></span>



| <span data-ttu-id="ac774-172">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-172">Category</span></span> | <span data-ttu-id="ac774-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-173">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-174">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-174">Issue</span></span>    | <span data-ttu-id="ac774-175">Después de controlar el mensaje [**WM \_ TOUCH,**](wm-touchdown.md) deté de recibir comentarios de límites.</span><span class="sxs-lookup"><span data-stu-id="ac774-175">After I handle the [**WM\_TOUCH**](wm-touchdown.md) message, I stop getting boundary feedback.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="ac774-176">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-176">Cause</span></span>    | <span data-ttu-id="ac774-177">Consumir el [**mensaje WM \_ TOUCH**](wm-touchdown.md) sin controlarlo.</span><span class="sxs-lookup"><span data-stu-id="ac774-177">Consuming the [**WM\_TOUCH**](wm-touchdown.md) message without handling it.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ac774-178">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-178">Solution</span></span> | <span data-ttu-id="ac774-179">Es probable que esté consumiendo un mensaje de Windows Touch sin reenviarlo a **DefWindowProc,** lo que dará lugar a un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="ac774-179">You are probably consuming a Windows Touch message without forwarding it to **DefWindowProc**, which will result in unexpected behavior.</span></span> <span data-ttu-id="ac774-180">Consulte [Tareas iniciales mensajes de Windows Touch](getting-started-with-multi-touch-messages.md) para obtener más información sobre cómo controlar correctamente los mensajes WM [**\_ TOUCH.**](wm-touchdown.md)</span><span class="sxs-lookup"><span data-stu-id="ac774-180">Check [Getting Started with Windows Touch Messages](getting-started-with-multi-touch-messages.md) for more information on how to properly handle [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac774-181">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-181">Issue</span></span></td>
<td><span data-ttu-id="ac774-182">Estoy incluyendo windows.h, pero sigue indicando que WM_TOUCH <a href="wm-touchdown.md"><strong>no</strong></a> está definido.</span><span class="sxs-lookup"><span data-stu-id="ac774-182">I am including windows.h, but it still says that <a href="wm-touchdown.md"><strong>WM_TOUCH</strong></a> is not defined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac774-183">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-183">Cause</span></span></td>
<td><span data-ttu-id="ac774-184">La versión de Windows en Targetver.h es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="ac774-184">The Windows version in Targetver.h is incorrect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac774-185">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-185">Solution</span></span></td>
<td><span data-ttu-id="ac774-186">No ha establecido la versión correcta de Windows en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ac774-186">You haven't set the correct Windows version in your project.</span></span> <span data-ttu-id="ac774-187">El código siguiente muestra las versiones de Windows establecidas correctamente para Windows Touch en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ac774-187">The following code illustrates the properly set Windows versions for Windows Touch in Windows 7.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac774-188">C++</span><span class="sxs-lookup"><span data-stu-id="ac774-188">C++</span></span></th>
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
<td><span data-ttu-id="ac774-189">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-189">Issue</span></span></td>
<td><span data-ttu-id="ac774-190">Mis coordenadas x de entrada táctil y las coordenadas Y parecen no válidas.</span><span class="sxs-lookup"><span data-stu-id="ac774-190">My touch input x-coordinates and y-coordinates seem invalid.</span></span> <span data-ttu-id="ac774-191">Son valores mayores de los esperados o son valores negativos.</span><span class="sxs-lookup"><span data-stu-id="ac774-191">They are either larger values than I expect or they are negative values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac774-192">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-192">Cause</span></span></td>
<td><span data-ttu-id="ac774-193">Es posible que tenga que convertir los puntos táctiles en píxeles o que necesite convertir las coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ac774-193">You may need to convert your touch points to pixels, or you may need to convert the screen coordinates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac774-194">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-194">Solution</span></span></td>
<td><span data-ttu-id="ac774-195">Asegúrese de llamar a <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> y <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ac774-195">Make sure that you are calling <a href="/windows/desktop/api/winuser/nf-winuser-touch_coord_to_pixel"><strong>TOUCH_COORD_TO_PIXEL</strong></a> and <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a>.</span></span> <span data-ttu-id="ac774-196">El código siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="ac774-196">The following code shows how to do this.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac774-197">C++</span><span class="sxs-lookup"><span data-stu-id="ac774-197">C++</span></span></th>
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
<span data-ttu-id="ac774-198">Para usar la función <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient,</strong></a> debe tener compatibilidad con valores altos de PPP en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac774-198">In order to use the <a href="/windows/desktop/api/winuser/nf-winuser-screentoclient"><strong>ScreenToClient</strong></a> function, you must have high DPI support in your application.</span></span> <span data-ttu-id="ac774-199">Para obtener más información sobre la compatibilidad con valores altos de PPP, visite la <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">sección Valores altos</a> de PPP de MSDN.</span><span class="sxs-lookup"><span data-stu-id="ac774-199">For more information on supporting high DPI, visit the <a href=" /windows/win32/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a> section of MSDN.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="ac774-200">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-200">Category</span></span> | <span data-ttu-id="ac774-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-201">Description</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-202">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-202">Issue</span></span>    | <span data-ttu-id="ac774-203">No veo mensajes [**WM \_ TOUCH,**](wm-touchdown.md) pero sé que Windows Touch funciona porque veo mensajes [**WM \_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="ac774-203">I'm not seeing [**WM\_TOUCH**](wm-touchdown.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>                                                             |
| <span data-ttu-id="ac774-204">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-204">Cause</span></span>    | <span data-ttu-id="ac774-205">Falta una llamada a [**RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)</span><span class="sxs-lookup"><span data-stu-id="ac774-205">Missing a call to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                          |
| <span data-ttu-id="ac774-206">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-206">Solution</span></span> | <span data-ttu-id="ac774-207">[**WM \_ Los mensajes TOUCH**](wm-touchdown.md) [**y WM \_ GESTURE**](wm-gesture.md) son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="ac774-207">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="ac774-208">Si no llama a [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)solo recibirá mensajes **WM \_ GESTURE.**</span><span class="sxs-lookup"><span data-stu-id="ac774-208">If you don't call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will receive only **WM\_GESTURE** messages.</span></span> |



 



| <span data-ttu-id="ac774-209">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-209">Category</span></span> | <span data-ttu-id="ac774-210">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-210">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-211">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-211">Issue</span></span>    | <span data-ttu-id="ac774-212">Estoy apercibiendo pequeños retrasos desde el momento en que toco el dedo hacia abajo hasta que obtendí entradas en mi aplicación.</span><span class="sxs-lookup"><span data-stu-id="ac774-212">I am noticing small delays from the time I touch my finger down to when I am getting input in my application.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="ac774-213">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-213">Cause</span></span>    | <span data-ttu-id="ac774-214">El rechazo de la mano está causando retrasos en la entrada.</span><span class="sxs-lookup"><span data-stu-id="ac774-214">Palm rejection is causing delays in input.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ac774-215">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-215">Solution</span></span> | <span data-ttu-id="ac774-216">Si **TWF \_ WANTPALM se establece** en llamadas a [**RegisterTouchWindow,**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)el rechazo de la mano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ac774-216">If **TWF\_WANTPALM** is set in calls to [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), palm rejection is enabled.</span></span> <span data-ttu-id="ac774-217">Esto provoca un retraso pequeño (100 ms) mientras el software comprueba si la entrada viene de un dedo, un lápiz o la mano del usuario.</span><span class="sxs-lookup"><span data-stu-id="ac774-217">This causes a small (100 ms) delay while the software tests whether input is coming from a finger, pen, or the user's palm.</span></span> <span data-ttu-id="ac774-218">Deshabilite el rechazo de hojas llamando **a RegisterTouchWindow** con la **marca \_ TWF WANTPALM** desactivada.</span><span class="sxs-lookup"><span data-stu-id="ac774-218">Disable palm rejection by calling **RegisterTouchWindow** with the **TWF\_WANTPALM** flag cleared.</span></span> |



 

## <a name="troubleshooting-windows-touch-gestures"></a><span data-ttu-id="ac774-219">Solución de problemas de gestos táctiles de Windows</span><span class="sxs-lookup"><span data-stu-id="ac774-219">Troubleshooting Windows Touch Gestures</span></span>



| <span data-ttu-id="ac774-220">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-220">Category</span></span> | <span data-ttu-id="ac774-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-221">Description</span></span> |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-222">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-222">Issue</span></span>    | <span data-ttu-id="ac774-223">Después de controlar el [**mensaje \_ WM GESTURE,**](wm-gesture.md) deté de recibir comentarios de límites.</span><span class="sxs-lookup"><span data-stu-id="ac774-223">After handling the [**WM\_GESTURE**](wm-gesture.md) message, I stop getting boundary feedback.</span></span> <span data-ttu-id="ac774-224">O bien, un gesto que funcionaba anteriormente no funciona ahora.</span><span class="sxs-lookup"><span data-stu-id="ac774-224">Or, a gesture that worked previously does not work now.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="ac774-225">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-225">Cause</span></span>    | <span data-ttu-id="ac774-226">Consumir el mensaje [**WM \_ GESTURE**](wm-gesture.md) sin controlarlo.</span><span class="sxs-lookup"><span data-stu-id="ac774-226">Consuming the [**WM\_GESTURE**](wm-gesture.md) message without handling it.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ac774-227">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-227">Solution</span></span> | <span data-ttu-id="ac774-228">Es probable que esté consumiendo un mensaje de Windows Touch sin reenviarlo a [DefWindowProc,](/windows/win32/api/winuser/nf-winuser-defwindowproca)lo que provocará un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="ac774-228">You are probably consuming a Windows Touch message without forwarding it to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca), which will result in unexpected behavior.</span></span> <span data-ttu-id="ac774-229">Compruebe [Tareas iniciales con gestos de Windows](getting-started-with-multi-touch-gestures.md) para obtener más información sobre cómo controlar correctamente los mensajes DE WM [**\_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="ac774-229">Check [Getting Started with Windows Gestures](getting-started-with-multi-touch-gestures.md) for more information on how to properly handle [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> |



 



| <span data-ttu-id="ac774-230">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-230">Category</span></span> | <span data-ttu-id="ac774-231">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-231">Description</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-232">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-232">Issue</span></span>    | <span data-ttu-id="ac774-233">No veo mensajes [**WM \_ GESTURE,**](wm-gesture.md) pero sé que Windows Touch funciona porque veo mensajes [**WM \_ TOUCH.**](wm-touchdown.md)</span><span class="sxs-lookup"><span data-stu-id="ac774-233">I'm not seeing [**WM\_GESTURE**](wm-gesture.md) messages, but I know that Windows Touch is working because I'm seeing [**WM\_TOUCH**](wm-touchdown.md) messages.</span></span>                                                      |
| <span data-ttu-id="ac774-234">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-234">Cause</span></span>    | <span data-ttu-id="ac774-235">Llamar [**a RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span><span class="sxs-lookup"><span data-stu-id="ac774-235">Calling [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow).</span></span>                                                                                                                                                             |
| <span data-ttu-id="ac774-236">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-236">Solution</span></span> | <span data-ttu-id="ac774-237">[**WM \_ Los mensajes TOUCH**](wm-touchdown.md) [**y WM \_ GESTURE**](wm-gesture.md) son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="ac774-237">[**WM\_TOUCH**](wm-touchdown.md) and [**WM\_GESTURE**](wm-gesture.md) messages are mutually exclusive.</span></span> <span data-ttu-id="ac774-238">Si llama a [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), no recibirá mensajes **WM \_ GESTURE.**</span><span class="sxs-lookup"><span data-stu-id="ac774-238">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will not receive **WM\_GESTURE** messages.</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ac774-239">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-239">Issue</span></span></td>
<td><span data-ttu-id="ac774-240">No veo todos los gestos que esperaba ver.</span><span class="sxs-lookup"><span data-stu-id="ac774-240">I'm not seeing all of the gestures that I expect to see.</span></span> <span data-ttu-id="ac774-241">Por ejemplo, veo gestos con el identificador GID_PAN <strong>pero</strong> <strong>no GID_ROTATE</strong>.</span><span class="sxs-lookup"><span data-stu-id="ac774-241">For example, I'm seeing gestures with the identifier <strong>GID_PAN</strong> but not <strong>GID_ROTATE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ac774-242">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-242">Cause</span></span></td>
<td><span data-ttu-id="ac774-243">Algunos gestos, como el gesto de rotación, no están habilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ac774-243">Some gestures, such as the rotate gesture, are not enabled by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ac774-244">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-244">Solution</span></span></td>
<td><span data-ttu-id="ac774-245">Debe llamar a <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> cuando reciba un mensaje <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> como se describe en la referencia <strong>de WM_GESTURENOTIFY,</strong> o bien debe agregar un controlador para el <strong>mensaje WM_GESTURENOTIFY.</strong></span><span class="sxs-lookup"><span data-stu-id="ac774-245">You need to call <a href="/windows/desktop/api/winuser/nf-winuser-setgestureconfig"><strong>SetGestureConfig</strong></a> when you receive a <a href="wm-gesturenotify.md"><strong>WM_GESTURENOTIFY</strong></a> message as described in the <strong>WM_GESTURENOTIFY</strong> reference, or you need to add a handler for the <strong>WM_GESTURENOTIFY</strong> message.</span></span> <span data-ttu-id="ac774-246">El código siguiente muestra cómo se podría implementar un controlador para habilitar la compatibilidad con la rotación.</span><span class="sxs-lookup"><span data-stu-id="ac774-246">The following code shows how a handler could be implemented to enable support for rotation.</span></span> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ac774-247">C++</span><span class="sxs-lookup"><span data-stu-id="ac774-247">C++</span></span></th>
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

<span data-ttu-id="ac774-248">Para obtener más ejemplos de configuraciones de gestos típicas, <strong>vea SetGestureConfig</strong>.</span><span class="sxs-lookup"><span data-stu-id="ac774-248">For more examples of typical gesture configurations, see <strong>SetGestureConfig</strong>.</span></span></td>
</tr>
</tbody>
</table>



 



| <span data-ttu-id="ac774-249">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-249">Category</span></span> | <span data-ttu-id="ac774-250">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-250">Description</span></span> |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-251">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-251">Issue</span></span>    | <span data-ttu-id="ac774-252">Las barras de desplazamiento personalizadas de mi aplicación no se desplazan cuando se realiza el gesto de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ac774-252">The custom scroll bars in my application are not scrolling when I perform the pan gesture.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ac774-253">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-253">Cause</span></span>    | <span data-ttu-id="ac774-254">Faltan controladores para los mensajes WM \_ \* SCROLL correctos.</span><span class="sxs-lookup"><span data-stu-id="ac774-254">Missing handlers for the correct WM\_\*SCROLL messages.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ac774-255">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-255">Solution</span></span> | <span data-ttu-id="ac774-256">No está controlando todos los mensajes WM \_ \* SCROLL en las barras de desplazamiento personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ac774-256">You are not handling all of the WM\_\*SCROLL messages in your custom scroll bars.</span></span> <span data-ttu-id="ac774-257">Se recomienda controlar el mensaje [**WM \_ GESTURE**](wm-gesture.md) en lugar de conservar la funcionalidad de barra de desplazamiento personalizada mediante compatibilidad heredada.</span><span class="sxs-lookup"><span data-stu-id="ac774-257">It is recommended that you handle the [**WM\_GESTURE**](wm-gesture.md) message rather than retain custom scrollbar functionality through legacy support.</span></span> <span data-ttu-id="ac774-258">Debe admitir mensajes como se detalla en la sección Compatibilidad heredada para el movimiento [panorámico con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md).</span><span class="sxs-lookup"><span data-stu-id="ac774-258">You need to support messages as detailed in the section [Legacy Support for Panning with Scroll bars](legacy-support-for-panning-with-scrollbars.md).</span></span> |



 



| <span data-ttu-id="ac774-259">Categoría</span><span class="sxs-lookup"><span data-stu-id="ac774-259">Category</span></span> | <span data-ttu-id="ac774-260">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac774-260">Description</span></span> |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac774-261">Incidencia</span><span class="sxs-lookup"><span data-stu-id="ac774-261">Issue</span></span>    | <span data-ttu-id="ac774-262">Estoy obteniendo retrasos para los gestos.</span><span class="sxs-lookup"><span data-stu-id="ac774-262">I am getting delays for gestures.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="ac774-263">Causa</span><span class="sxs-lookup"><span data-stu-id="ac774-263">Cause</span></span>    | <span data-ttu-id="ac774-264">Los gestos pueden estar causando retrasos.</span><span class="sxs-lookup"><span data-stu-id="ac774-264">Flicks may be causing delays for gestures.</span></span>                                                                                                                                                                                                                      |
| <span data-ttu-id="ac774-265">Solución</span><span class="sxs-lookup"><span data-stu-id="ac774-265">Solution</span></span> | <span data-ttu-id="ac774-266">Los gestos pueden provocar retrasos durante el tiempo que tarda la aplicación en recibir [**mensajes WM \_ GESTURE.**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="ac774-266">Flicks can cause delays for how long it takes for your application to receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="ac774-267">Consulte [Compatibilidad heredada para el movimiento panorámico](legacy-support-for-panning-with-scrollbars.md) con barras de desplazamiento para obtener información sobre cómo deshabilitar los gestos.</span><span class="sxs-lookup"><span data-stu-id="ac774-267">See [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) for information on disabling flicks.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ac774-268">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac774-268">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac774-269">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="ac774-269">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 