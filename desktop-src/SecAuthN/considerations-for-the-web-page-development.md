---
description: El agente de autenticación Web se basa en la parte superior de las mismas tecnologías que Power Internet Explorer en Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Consideraciones para el desarrollo de páginas web
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360800"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="594a3-103">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="594a3-103">Considerations for the web page development</span></span>

<span data-ttu-id="594a3-104">El agente de autenticación Web se basa en la parte superior de las mismas tecnologías que Power Internet Explorer en Windows.</span><span class="sxs-lookup"><span data-stu-id="594a3-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="594a3-105">Sin embargo, debido a una finalidad muy especial de este componente, algunas características de Internet Explorer se deshabilitaron o se bloqueaban para una configuración específica.</span><span class="sxs-lookup"><span data-stu-id="594a3-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="594a3-106">Además, el agente de autenticación Web proporciona un canal de registro de eventos dedicado para ayudar a solucionar problemas con las páginas que procesa.</span><span class="sxs-lookup"><span data-stu-id="594a3-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="594a3-107">Modo de documento estándar de Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="594a3-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="594a3-108">El agente de autenticación Web muestra todas las páginas en el "modo estándar de IE10".</span><span class="sxs-lookup"><span data-stu-id="594a3-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="594a3-109">Puede usar las herramientas de desarrollo de Internet Explorer para ver cómo funciona la página en diferentes modos de documento.</span><span class="sxs-lookup"><span data-stu-id="594a3-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="594a3-110">Para obtener más información sobre la compatibilidad de Internet Explorer 10, vea los temas de MSDN para [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="594a3-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="594a3-111">Características deshabilitadas y bloqueadas</span><span class="sxs-lookup"><span data-stu-id="594a3-111">Disabled and locked down features</span></span>

<span data-ttu-id="594a3-112">Varias características de Internet Explorer están completamente deshabilitadas o bloqueadas para valores específicos que no se pueden cambiar en las opciones de Internet del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="594a3-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="594a3-113">Característica</span><span class="sxs-lookup"><span data-stu-id="594a3-113">Feature</span></span>                            | <span data-ttu-id="594a3-114">Situación</span><span class="sxs-lookup"><span data-stu-id="594a3-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="594a3-115">API de caché de aplicaciones ("AppCache")</span><span class="sxs-lookup"><span data-stu-id="594a3-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="594a3-116">Disabled</span><span class="sxs-lookup"><span data-stu-id="594a3-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="594a3-117">Historial de vínculos</span><span class="sxs-lookup"><span data-stu-id="594a3-117">Link history</span></span>                       | <span data-ttu-id="594a3-118">Disabled</span><span class="sxs-lookup"><span data-stu-id="594a3-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="594a3-119">Archivos temporales</span><span class="sxs-lookup"><span data-stu-id="594a3-119">Temporary files</span></span>                    | <span data-ttu-id="594a3-120">habilitado</span><span class="sxs-lookup"><span data-stu-id="594a3-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="594a3-121">Cookies</span><span class="sxs-lookup"><span data-stu-id="594a3-121">Cookies</span></span>                            | <span data-ttu-id="594a3-122">Las cookies de sesión están habilitadas.</span><span class="sxs-lookup"><span data-stu-id="594a3-122">Session cookies are enabled.</span></span> <span data-ttu-id="594a3-123">Las cookies persistentes están permitidas, pero están sujetas a la limpieza automática a menos que el agente de autenticación Web esté en modo SSO.</span><span class="sxs-lookup"><span data-stu-id="594a3-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="594a3-124">Para obtener más información, consulte la sección Inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="594a3-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="594a3-125">BASE de índice</span><span class="sxs-lookup"><span data-stu-id="594a3-125">Index DB</span></span>                           | <span data-ttu-id="594a3-126">Disabled</span><span class="sxs-lookup"><span data-stu-id="594a3-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="594a3-127">Almacenamiento DOM</span><span class="sxs-lookup"><span data-stu-id="594a3-127">DOM storage</span></span>                        | <span data-ttu-id="594a3-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="594a3-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="594a3-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="594a3-129">ActiveX</span></span>                            | <span data-ttu-id="594a3-130">Disabled</span><span class="sxs-lookup"><span data-stu-id="594a3-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="594a3-131">Descargas de archivos</span><span class="sxs-lookup"><span data-stu-id="594a3-131">File downloads</span></span>                     | <span data-ttu-id="594a3-132">Disabled</span><span class="sxs-lookup"><span data-stu-id="594a3-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="594a3-133">Requisito de HTTPS</span><span class="sxs-lookup"><span data-stu-id="594a3-133">HTTPS requirement</span></span>

<span data-ttu-id="594a3-134">La primera dirección URL que utilizará una aplicación para comunicarse con el proveedor en línea debe ser HTTPS.</span><span class="sxs-lookup"><span data-stu-id="594a3-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="594a3-135">Dimensión para distintos tamaños de ventana</span><span class="sxs-lookup"><span data-stu-id="594a3-135">Dimension for different window sizes</span></span>

<span data-ttu-id="594a3-136">Una aplicación de Windows 8 puede aparecer en varios tamaños, como pantalla completa, una ventana cuyo tamaño se ha cambiado o en un acceso, como el acceso compartido.</span><span class="sxs-lookup"><span data-stu-id="594a3-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="594a3-137">En función del diseño de ventana que aparezca el agente de autenticación Web, el tamaño con el que tienen que trabajar las páginas web podría ser diferente.</span><span class="sxs-lookup"><span data-stu-id="594a3-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="594a3-138">Para obtener más información, vea el tema [instrucciones para cambiar el tamaño a diseños estrechos](/previous-versions/windows/hh465371(v=win.10)) y el tema [directrices para compartir contenido](/previous-versions/windows/hh465251(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="594a3-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="594a3-139">La página web debe usar las consultas multimedia de CSS para comprobar el tamaño con el que tiene que trabajar y colocarse en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="594a3-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="594a3-140">Sin embargo, la página no debe diseñarse en función de los píxeles exactos que se documentan aquí y deben poder escalarse a distintos tamaños.</span><span class="sxs-lookup"><span data-stu-id="594a3-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="594a3-141">Los tamaños especificados en este documento están sujetos a cambios en futuras versiones del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="594a3-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="594a3-142">Si una página no puede ajustarse a toda la información del espacio asignado (por ejemplo, una larga lista de permisos que una aplicación está solicitando), el agente de autenticación Web proporcionará barras de desplazamiento para permitir al usuario desplazarse por la página según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="594a3-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="594a3-143">El zoom también lo proporciona el zoom de pinch para dispositivos basados en táctil y Ctrl + rueda del mouse para equipos portátiles y de escritorio.</span><span class="sxs-lookup"><span data-stu-id="594a3-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="594a3-144">Para probar distintos factores de escala, use la [aplicación de ejemplo del SDK del agente de autenticación Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) cargada en Microsoft Visual Studio Professional 2012, que permite simular la pantalla completa y cambiar el tamaño de los Estados.</span><span class="sxs-lookup"><span data-stu-id="594a3-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="594a3-145">Además de los distintos diseños descritos anteriormente, asegúrese de probar la página en una orientación de pantalla diferente (por ejemplo, vertical y horizontal) y diferentes configuraciones regionales y idiomas, así como con características de accesibilidad, como la opción "hacer todo más grande" activada.</span><span class="sxs-lookup"><span data-stu-id="594a3-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="594a3-146">Los diseños disponibles son:</span><span class="sxs-lookup"><span data-stu-id="594a3-146">The available layouts are:</span></span>

-   [<span data-ttu-id="594a3-147">Pantalla completa</span><span class="sxs-lookup"><span data-stu-id="594a3-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="594a3-148">Ventana cuyo tamaño se ha cambiado</span><span class="sxs-lookup"><span data-stu-id="594a3-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="594a3-149">Vista de acceso</span><span class="sxs-lookup"><span data-stu-id="594a3-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="594a3-150">Vista del selector de archivos</span><span class="sxs-lookup"><span data-stu-id="594a3-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="594a3-151">Pantalla completa</span><span class="sxs-lookup"><span data-stu-id="594a3-151">Full screen</span></span>

<span data-ttu-id="594a3-152">En el diseño de pantalla completa, las dimensiones de la página web son:</span><span class="sxs-lookup"><span data-stu-id="594a3-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="594a3-153">Ancho: 566 píxeles</span><span class="sxs-lookup"><span data-stu-id="594a3-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="594a3-154">Alto: alto de la pantalla (depende de la resolución de la pantalla)</span><span class="sxs-lookup"><span data-stu-id="594a3-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="594a3-155">En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en el diseño de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="594a3-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![ejemplo de interfaz de usuario del agente de autenticación Web en el diseño de pantalla completa](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="594a3-157">Tamaño</span><span class="sxs-lookup"><span data-stu-id="594a3-157">Resized</span></span>

<span data-ttu-id="594a3-158">En el caso de una ventana cuyo tamaño se ha cambiado, las dimensiones de la página web pueden ser:</span><span class="sxs-lookup"><span data-stu-id="594a3-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="594a3-159">Ancho: 260 píxeles</span><span class="sxs-lookup"><span data-stu-id="594a3-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="594a3-160">Alto: alto de la pantalla (depende de la resolución de la pantalla)</span><span class="sxs-lookup"><span data-stu-id="594a3-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="594a3-161">En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en una ventana cuyo tamaño se ha cambiado en la Página Web de XBox.</span><span class="sxs-lookup"><span data-stu-id="594a3-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="594a3-162">Tenga en cuenta que la interfaz de usuario del agente de autenticación Web solo está en el lado derecho de la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="594a3-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![ejemplo de interfaz de usuario del agente de autenticación Web en una ventana cuyo tamaño se ha cambiado](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="594a3-164">Vista de acceso</span><span class="sxs-lookup"><span data-stu-id="594a3-164">Charm view</span></span>

<span data-ttu-id="594a3-165">En la vista de acceso, las dimensiones de la página web son:</span><span class="sxs-lookup"><span data-stu-id="594a3-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="594a3-166">Ancho: 566 píxeles</span><span class="sxs-lookup"><span data-stu-id="594a3-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="594a3-167">Alto: alto de la pantalla (depende de la resolución de la pantalla)</span><span class="sxs-lookup"><span data-stu-id="594a3-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="594a3-168">En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en la vista de acceso.</span><span class="sxs-lookup"><span data-stu-id="594a3-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![un ejemplo muestra la interfaz de usuario del agente de autenticación Web en la vista de acceso](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="594a3-170">Vista del selector de archivos</span><span class="sxs-lookup"><span data-stu-id="594a3-170">File picker view</span></span>

<span data-ttu-id="594a3-171">En la vista selector de archivos, las dimensiones de la página web son:</span><span class="sxs-lookup"><span data-stu-id="594a3-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="594a3-172">Ancho: 566 píxeles</span><span class="sxs-lookup"><span data-stu-id="594a3-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="594a3-173">Alto: alto de la pantalla (depende de la resolución de la pantalla)</span><span class="sxs-lookup"><span data-stu-id="594a3-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="594a3-174">En el ejemplo siguiente se muestra la interfaz de usuario del agente de autenticación Web en la vista del selector de archivos.</span><span class="sxs-lookup"><span data-stu-id="594a3-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![un ejemplo muestra la interfaz de usuario del agente de autenticación Web en la vista del selector de archivos](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="594a3-176">No hay ventanas nuevas de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="594a3-176">No new windows by default</span></span>

<span data-ttu-id="594a3-177">De forma predeterminada, ninguna dirección URL dará como resultado que se abra una nueva ventana, pero en su lugar se mostrará en la ventana agente de autenticación Web.</span><span class="sxs-lookup"><span data-stu-id="594a3-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="594a3-178">Esto incluye el método de JavaScript Window. Open, el atributo de destino de los hipervínculos o el uso del mecanismo Ctrl + clic para forzar que se abra una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="594a3-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="594a3-179">La excepción a esta regla es cuando una página Web declara que un vínculo es seguro para navegar en un explorador, tal como se describe en el destino de personalización de los hipervínculos.</span><span class="sxs-lookup"><span data-stu-id="594a3-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="594a3-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="594a3-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="594a3-181">Aplicación de ejemplo del SDK del agente de autenticación Web</span><span class="sxs-lookup"><span data-stu-id="594a3-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="594a3-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="594a3-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
