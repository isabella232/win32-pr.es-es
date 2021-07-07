---
description: En este tema se describen los procedimientos recomendados para diseñar páginas web que usan el Agente de autenticación web para iniciar sesión.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Procedimientos recomendados para diseñar páginas web de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdd6ab5dc067c23cfb29d21d2ff4780cee0ef1c
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353678"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="bd386-103">Procedimientos recomendados para diseñar páginas web de autenticación</span><span class="sxs-lookup"><span data-stu-id="bd386-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="bd386-104">En este tema se describen los procedimientos recomendados para diseñar páginas web que usan el Agente de autenticación web para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="bd386-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="bd386-105">Uso de metatags</span><span class="sxs-lookup"><span data-stu-id="bd386-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="bd386-106">Uso del estilo Windows 8 CSS</span><span class="sxs-lookup"><span data-stu-id="bd386-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="bd386-107">Uso de colores y temas</span><span class="sxs-lookup"><span data-stu-id="bd386-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="bd386-108">Alineación</span><span class="sxs-lookup"><span data-stu-id="bd386-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="bd386-109">Diseño para ajustar</span><span class="sxs-lookup"><span data-stu-id="bd386-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="bd386-110">Diseño para una experiencia de inicio de sesión rápida y fluida</span><span class="sxs-lookup"><span data-stu-id="bd386-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="bd386-111">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="bd386-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="bd386-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd386-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="bd386-113">Uso de metatags</span><span class="sxs-lookup"><span data-stu-id="bd386-113">Use of metatags</span></span>

<span data-ttu-id="bd386-114">Mediante metatags, el proveedor "Contoso Social" puede especificar el título, el icono y el color del encabezado.</span><span class="sxs-lookup"><span data-stu-id="bd386-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="bd386-115">En el archivo HTML de ejemplo (WebAuthLogin.html), esto se realiza mediante el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="bd386-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="bd386-116">Esto permite Windows la presencia del proveedor de forma destacada en el encabezado de la interfaz de usuario, como se resalta en el cuadro rojo de la captura de pantalla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bd386-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![página de inicio de sesión que muestra el encabezado contoso en la interfaz de usuario](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="bd386-118">Uso del estilo Windows 8 CSS</span><span class="sxs-lookup"><span data-stu-id="bd386-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="bd386-119">La hoja de estilos ui-light.css proporcionada es Windows 8 hoja de estilos que usan las Windows Store.</span><span class="sxs-lookup"><span data-stu-id="bd386-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="bd386-120">Define el estilo Windows store para la tipografía y los controles estándar, como botones, cuadros de texto, hipervínculos y casillas para asegurarse de que son táctiles.</span><span class="sxs-lookup"><span data-stu-id="bd386-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="bd386-121">Al diseñar y personalizar páginas de autorización web para Windows 8, le recomendamos que use esta hoja de estilos tal y como está y la actualice según sea necesario siempre que la página web siga los procedimientos recomendados a su manera.</span><span class="sxs-lookup"><span data-stu-id="bd386-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="bd386-122">Por ejemplo, si tiene una hoja de estilos especial para saber qué aspecto deben tener los hipervínculos en la página web, es bueno tener cuidado para asegurarse de que el estilo que proporcione sea descriptivo al toque de la misma manera que los hipervínculos estándar Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bd386-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="bd386-123">Esto es esencial para la base de consumidores mediante Windows 8 en sus dispositivos táctiles.</span><span class="sxs-lookup"><span data-stu-id="bd386-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="bd386-124">Uso de colores y temas</span><span class="sxs-lookup"><span data-stu-id="bd386-124">Use of color and themes</span></span>

<span data-ttu-id="bd386-125">En este ejemplo se muestra un uso cuidadoso del color de varias maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="bd386-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="bd386-126">Fondo blanco de la página web.</span><span class="sxs-lookup"><span data-stu-id="bd386-126">White background for the web page.</span></span> <span data-ttu-id="bd386-127">Como puede ver en la captura de pantalla anterior, la página web se hospeda dentro de una superficie blanca que abarca el ancho de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="bd386-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="bd386-128">Para asegurarse de que la página web se integra con la superficie, se recomienda que la página web tenga un fondo blanco.</span><span class="sxs-lookup"><span data-stu-id="bd386-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="bd386-129">Colores de los controles en función del color de la marca.</span><span class="sxs-lookup"><span data-stu-id="bd386-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="bd386-130">El archivo CSS theme-colors.css proporciona estilo para invalidar los colores estándar de los controles de la hoja de estilos de la interfaz de usuario ligera para que coincidan con el tema de los controles con el color del encabezado.</span><span class="sxs-lookup"><span data-stu-id="bd386-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="bd386-131">Por ejemplo, en la siguiente captura de pantalla, los botones y los hipervínculos toman colores derivados del color del encabezado.</span><span class="sxs-lookup"><span data-stu-id="bd386-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![captura de pantalla de los botones y el texto con el mismo color que el encabezado](images/wab-figure11.png)
-   <span data-ttu-id="bd386-133">Color del encabezado.</span><span class="sxs-lookup"><span data-stu-id="bd386-133">Header color.</span></span> <span data-ttu-id="bd386-134">El uso del color de marca de Contoso en el encabezado crea una personalidad unificada para la marca del proveedor dentro de la interfaz de usuario del sistema.</span><span class="sxs-lookup"><span data-stu-id="bd386-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="bd386-135">Alignment</span><span class="sxs-lookup"><span data-stu-id="bd386-135">Alignment</span></span>

<span data-ttu-id="bd386-136">La propia página web no tiene relleno a la izquierda ni a la derecha para permitir la alineación tipográfica con el título del encabezado de la izquierda y el icono en el encabezado de la derecha.</span><span class="sxs-lookup"><span data-stu-id="bd386-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="bd386-137">También observará que los botones siempre están alineados de abajo a la derecha en la página web (y alineados a la derecha con el icono del encabezado).</span><span class="sxs-lookup"><span data-stu-id="bd386-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="bd386-138">Este es el procedimiento recomendado, ya Windows 8 usuarios estarán acostumbrados a flujos de diálogo similares con botones en la parte inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="bd386-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="bd386-139">Diseño para ajustar</span><span class="sxs-lookup"><span data-stu-id="bd386-139">Designing for snap</span></span>

<span data-ttu-id="bd386-140">En la imagen siguiente, puede ver las páginas de inicio de sesión y permisos en estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="bd386-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="bd386-141">vista snap de la pantalla de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="bd386-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="bd386-142">.</span><span class="sxs-lookup"><span data-stu-id="bd386-142">.</span></span> ![<span data-ttu-id="bd386-143">vista de instantánea de la página de permisos</span><span class="sxs-lookup"><span data-stu-id="bd386-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="bd386-144">En el archivo de ejemplo ui-webauth.css, puede ver el uso de consultas multimedia que optimizan el diseño de la página para ajustar el estado en función del ancho disponible para la página web.</span><span class="sxs-lookup"><span data-stu-id="bd386-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="bd386-145">El fragmento de código incluido en el ámbito siguiente implementa CSS adaptado para el estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="bd386-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="bd386-146">En Windows 8, el ancho del estado de ajuste es de 320 píxeles.</span><span class="sxs-lookup"><span data-stu-id="bd386-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="bd386-147">La página de autenticación web ocupa 260 píxeles en la interfaz de usuario anterior.</span><span class="sxs-lookup"><span data-stu-id="bd386-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="bd386-148">Estamos usando un valor de ancho máximo con margen suficiente, por lo que el código de consulta multimedia del proveedor no está enlazado al ancho exacto del estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="bd386-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="bd386-149">Al personalizar la aplicación para la vista de ajuste, es importante que el usuario no pierda ningún contexto que tenga en las demás vistas de la experiencia de autenticación web (vistas completa, de relleno o de acceso), pero es útil volver a estructurar el diseño y la jerarquía de los elementos de la página para que la información necesaria para conservar el contexto sea visible e interactiva.</span><span class="sxs-lookup"><span data-stu-id="bd386-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="bd386-150">Hemos llamado a algunos ejemplos de cómo el ejemplo adapta la página web para el estado de ajuste.</span><span class="sxs-lookup"><span data-stu-id="bd386-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="bd386-151">Por ejemplo, para la página de inicio de sesión en estado de ajuste, la propiedad width del campo de texto de entrada (como se especifica en ui-light.css) se ha invalidado y se ha establecido como un valor numérico más pequeño, de modo que el campo de texto no se recorta horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="bd386-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="bd386-152">Como otro ejemplo, en estado de ajuste, el tamaño de fuente de los encabezados h1 y h2 se reduce a 20 pt y 11 pt de 42 pt y 20 pt respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bd386-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="bd386-153">Esto se realiza de acuerdo con la rampa Windows 8 tipo y optimiza el texto para que sea más compacto en la ventanilla modificada.</span><span class="sxs-lookup"><span data-stu-id="bd386-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="bd386-154">Como otro ejemplo, observe que los tamaños de los iconos de la página de permisos son más pequeños (compare con la página de vista completa anterior).</span><span class="sxs-lookup"><span data-stu-id="bd386-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="bd386-155">De nuevo, esto se hace para conservar el contexto, al mismo tiempo que se intercambian los recursos de diseño para los más óptimos para la ventanilla modificada.</span><span class="sxs-lookup"><span data-stu-id="bd386-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="bd386-156">Diseño para una experiencia de inicio de sesión rápida y fluida</span><span class="sxs-lookup"><span data-stu-id="bd386-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="bd386-157">Al principio del diseño de esta página web, nos hemos puesto en peligro en el hecho de que una de las cosas en las que esta página es mejor es una experiencia de inicio de sesión rápida y fluida.</span><span class="sxs-lookup"><span data-stu-id="bd386-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="bd386-158">Por lo tanto, la interfaz de usuario más destacada en el flujo es el campo nombre de usuario y contraseña de la página de inicio de sesión para una experiencia rápida de entrada de credenciales.</span><span class="sxs-lookup"><span data-stu-id="bd386-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="bd386-159">Aunque hemos identificado que hay otros escenarios comunes, como la recuperación de contraseñas y la referencia a declaraciones de privacidad, la experiencia enriquecencia de la web es un mejor lugar para esas experiencias.</span><span class="sxs-lookup"><span data-stu-id="bd386-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="bd386-160">Para todos los flujos no relacionados con la experiencia de autenticación web segura, se recomienda navegar al usuario al explorador.</span><span class="sxs-lookup"><span data-stu-id="bd386-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="bd386-161">Esto se muestra en el archivo HTML de ejemplo (WebAuthLogin.html) como se indica a continuación: se abren todas las páginas web vinculadas a desde la página de inicio de sesión o permisos en el explorador predeterminado del usuario, donde el usuario puede completar estos flujos y, a continuación, volver a la aplicación para iniciar `<meta name="mswebdialog-newwindowurl" content="*" />` sesión.</span><span class="sxs-lookup"><span data-stu-id="bd386-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="bd386-162">Consideraciones sobre la seguridad</span><span class="sxs-lookup"><span data-stu-id="bd386-162">Security Considerations</span></span>

<span data-ttu-id="bd386-163">En los artículos siguientes se proporcionan instrucciones para escribir código C++ seguro.</span><span class="sxs-lookup"><span data-stu-id="bd386-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="bd386-164">Procedimientos recomendados de seguridad para C++</span><span class="sxs-lookup"><span data-stu-id="bd386-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="bd386-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="bd386-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd386-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd386-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd386-167">Consideraciones para el desarrollo de páginas web</span><span class="sxs-lookup"><span data-stu-id="bd386-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="bd386-168">Preguntas más frecuentes sobre el Agente de autenticación web</span><span class="sxs-lookup"><span data-stu-id="bd386-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)
</dt> <dt>

[<span data-ttu-id="bd386-169">Aplicación de ejemplo del SDK del Agente de autenticación web</span><span class="sxs-lookup"><span data-stu-id="bd386-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="bd386-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="bd386-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
