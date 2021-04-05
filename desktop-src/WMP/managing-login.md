---
title: Administrar inicio de sesión
description: Administrar inicio de sesión
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player tiendas en línea, administrar inicios de sesión
- tiendas en línea, administrar inicios de sesión
- tipo 1 almacenes en línea, administrar inicios de sesión
- Windows Media Player tiendas en línea, inicios de sesión
- tiendas en línea, inicios de sesión
- tipo 1 tiendas en línea, inicios de sesión
- Windows Media Player tiendas en línea, proceso de inicio de sesión estándar
- tiendas en línea, proceso de inicio de sesión estándar
- tipo 1 almacenes en línea, proceso de inicio de sesión estándar
- Windows Media Player tiendas en línea, proceso de cierre de sesión
- tiendas en línea, proceso de cierre de sesión
- tipo 1 tiendas en línea, proceso de cierre de sesión
- proceso de inicio de sesión estándar
- proceso de cierre de sesión
- inicios de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633042692ab9193f46ab83415df13237d3a279e8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420279"
---
# <a name="managing-login"></a><span data-ttu-id="4432f-118">Administrar inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="4432f-118">Managing Login</span></span>

<span data-ttu-id="4432f-119">Windows Media Player admite una variedad de métodos para que el usuario inicie sesión en una tienda en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="4432f-119">Windows Media Player supports a variety of methods for the user to log in to a type 1 online store.</span></span> <span data-ttu-id="4432f-120">El reproductor proporciona un cuadro de diálogo de inicio de sesión estándar, pero la tienda en línea puede proporcionar una página web que actúa como alternativa al cuadro de diálogo estándar.</span><span class="sxs-lookup"><span data-stu-id="4432f-120">The Player provides a standard log-in dialog box, but the online store can provide a webpage that serves as an alternative to the standard dialog box.</span></span>

<span data-ttu-id="4432f-121">El usuario puede iniciar un intento de inicio de sesión mediante la interacción con la interfaz de usuario de Media Player de Windows o mediante la interacción con una página de detección proporcionada por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4432f-121">The user can initiate a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page provided by the online store.</span></span> <span data-ttu-id="4432f-122">Si el usuario inicia un intento de inicio de sesión mediante la interacción con una página de detección, el script de la página de detección llama al método [external. attemptLogin](external-attemptlogin.md) .</span><span class="sxs-lookup"><span data-stu-id="4432f-122">If the user initiates a log-in attempt by interacting with a discovery page, script on the discovery page calls the [External.attemptLogin](external-attemptlogin.md) method.</span></span>

<span data-ttu-id="4432f-123">La tienda en línea mantiene el estado de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-123">The user's log-in state is maintained by the online store.</span></span> <span data-ttu-id="4432f-124">Cuando cambia el estado de inicio de sesión del usuario, o si se produce un error en un intento de inicio de sesión, el complemento de la tienda en línea notifica a Windows Media Player llamando a [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), pasando wmpcnLoginStateChange en el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="4432f-124">When the user's log-in state changes, or if a log-in attempt fails, the online store's plug-in notifies Windows Media Player by calling [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="4432f-125">El reproductor pasa la notificación a la página de detección generando el evento [. OnLoginChange externo](external-onloginchange-event.md) .</span><span class="sxs-lookup"><span data-stu-id="4432f-125">The Player passes the notification along to the discovery page by raising the [External.OnLoginChange](external-onloginchange-event.md) event.</span></span>

<span data-ttu-id="4432f-126">Una llamada a **OnLoginChange** no significa necesariamente que haya cambiado el estado de inicio de sesión del usuario. podría significar que se produjo un error al intentar iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="4432f-126">A call to **OnLoginChange** does not necessarily mean that the user's log-in state changed; it could mean that an attempt to log in failed.</span></span> <span data-ttu-id="4432f-127">Para determinar el estado de inicio de sesión del usuario, el controlador de eventos **OnLoginChange** puede inspeccionar la propiedad [external. userLoggedIn](external-userloggedin.md) .</span><span class="sxs-lookup"><span data-stu-id="4432f-127">To determine the user's log-in state, the **OnLoginChange** event handler can inspect the [External.userLoggedIn](external-userloggedin.md) property.</span></span>

<span data-ttu-id="4432f-128">En las secciones siguientes se describe el proceso de inicio de sesión estándar, el proceso de inicio de sesión alternativo y el proceso de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="4432f-128">The following sections describe the standard log-in process, the alternative log-in process, and the log-out process.</span></span>

## <a name="standard-log-in"></a><span data-ttu-id="4432f-129">Inicio de sesión estándar</span><span class="sxs-lookup"><span data-stu-id="4432f-129">Standard Log-in</span></span>

<span data-ttu-id="4432f-130">El proceso de inicio de sesión estándar consta de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="4432f-130">The standard log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="4432f-131">El usuario inicia un intento de inicio de sesión mediante la interacción con la interfaz de usuario de Media Player de Windows o mediante la interacción con una página de detección.</span><span class="sxs-lookup"><span data-stu-id="4432f-131">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="4432f-132">Windows Media Player muestra un cuadro de diálogo que solicita al usuario un nombre de usuario y una contraseña.</span><span class="sxs-lookup"><span data-stu-id="4432f-132">Windows Media Player displays a dialog box that prompts the user for a user-name and password.</span></span>
3.  <span data-ttu-id="4432f-133">Cuando el usuario hace clic en el botón **iniciar sesión** del cuadro de diálogo, Windows Media Player llama a [IWMPContentPartner:: login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), que se implementa mediante el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4432f-133">When the user clicks the **Sign In** button in the dialog box, Windows Media Player calls [IWMPContentPartner::Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login), which is implemented by the online store's plug-in.</span></span>
4.  <span data-ttu-id="4432f-134">El complemento se comunica con la tienda en línea y se realiza correctamente o no puede iniciar sesión en el usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-134">The plug-in communicates with the online store and either succeeds or fails to log in the user.</span></span>
5.  <span data-ttu-id="4432f-135">Si el intento de inicio de sesión se realiza correctamente, el complemento notifica a Windows Media Player llamando a **IWMPContentPartnerCallback:: Notify**, pasando Variant \_ true en el miembro **boolVal** del parámetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="4432f-135">If the log-in attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="4432f-136">Si se produce un error en el intento de inicio de sesión, el complemento notifica a Windows Media Player llamando a **IWMPContentPartnerCallback:: Notify**, pasando un valor de 32 bits en el miembro **UlVal** del parámetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="4432f-136">If the log-in attempt fails, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing a 32-bit value in the **ulVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="4432f-137">A continuación, el reproductor pasa el valor de 32 bits a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) para obtener la dirección URL de una página web que puede controlar el error.</span><span class="sxs-lookup"><span data-stu-id="4432f-137">The Player then passes that 32-bit value to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to get the URL of a webpage that can handle the failure.</span></span>

## <a name="alternative-login"></a><span data-ttu-id="4432f-138">Inicio de sesión alternativo</span><span class="sxs-lookup"><span data-stu-id="4432f-138">Alternative Login</span></span>

<span data-ttu-id="4432f-139">Si la \_ marca ALTLOGIN de límite de suscripción \_ se establece en la entrada del registro **Capabilities** para el complemento de la tienda en línea, Windows Media Player no utiliza el cuadro de diálogo Inicio de sesión estándar.</span><span class="sxs-lookup"><span data-stu-id="4432f-139">If the SUBSCRIPTION\_CAP\_ALTLOGIN flag is set in the **Capabilities** registry entry for the online store's plug-in, Windows Media Player does not use the standard log-in dialog box.</span></span> <span data-ttu-id="4432f-140">En su lugar, Windows Media Player llama a **IWMPContentPartner:: GetItemInfo** para recuperar la dirección URL de una página web que realiza el proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="4432f-140">Instead, Windows Media Player calls **IWMPContentPartner::GetItemInfo** to retrieve the URL of a webpage that performs the log-in process.</span></span> <span data-ttu-id="4432f-141">Para obtener más información acerca de la entrada del registro **Capabilities** , consulte [claves del registro y entradas para una tienda en línea de tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="4432f-141">For more information about the **Capabilities** registry entry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="4432f-142">El reproductor llama a **GetItemInfo** dos veces: una vez pasado g \_ szItemInfo \_ ALTLoginURL para recuperar la dirección URL de la Página Web de inicio de sesión y después pasar g \_ szItemInfo \_ ALTLoginCaption para recuperar el título de la ventana que hospeda la Página Web.</span><span class="sxs-lookup"><span data-stu-id="4432f-142">The Player calls **GetItemInfo** twice: once passing g\_szItemInfo\_ALTLoginURL to retrieve the URL of the log-in webpage and once passing g\_szItemInfo\_ALTLoginCaption to retrieve the caption for the window that hosts the webpage.</span></span> <span data-ttu-id="4432f-143">Cuando **GetItemInfo** devuelve la dirección URL de la Página Web de inicio de sesión, puede especificar el tamaño de la ventana de inicio de sesión anexando la siguiente cadena de parámetro a la dirección URL:</span><span class="sxs-lookup"><span data-stu-id="4432f-143">When **GetItemInfo** returns the URL of the log-in webpage, it can specify the size of the log-in window by appending the following parameter string to the URL:</span></span>

<span data-ttu-id="4432f-144">? DlgX =*ancho*&DlgY =*alto*</span><span class="sxs-lookup"><span data-stu-id="4432f-144">?DlgX=*width*&DlgY=*height*</span></span>

<span data-ttu-id="4432f-145">En la cadena de parámetro, *ancho* y *alto* son el ancho y el alto de la ventana en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4432f-145">In the parameter string, *width* and *height* are the width and height of the window in pixels.</span></span> <span data-ttu-id="4432f-146">Por ejemplo, **GetItemInfo** podría devolver la siguiente cadena para especificar que AltLogin.htm debe mostrarse en una ventana con un ancho de 800 píxeles y un alto de 400 píxeles.</span><span class="sxs-lookup"><span data-stu-id="4432f-146">For example **GetItemInfo** could return the following string to specify that AltLogin.htm should be displayed in a window that has a width of 800 pixels and a height of 400 pixels</span></span>


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



<span data-ttu-id="4432f-147">El proceso de inicio de sesión alternativo implica los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="4432f-147">The alternative log-in process involves the following steps:</span></span>

1.  <span data-ttu-id="4432f-148">El usuario inicia un intento de inicio de sesión mediante la interacción con la interfaz de usuario de Media Player de Windows o mediante la interacción con una página de detección.</span><span class="sxs-lookup"><span data-stu-id="4432f-148">The user initiates a log-in attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="4432f-149">Windows Media Player abre una ventana modal que muestra la Página Web de inicio de sesión proporcionada por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4432f-149">Windows Media Player opens a modal window that displays the log-in webpage provided by the online store.</span></span>
3.  <span data-ttu-id="4432f-150">La página web se comunica con la tienda en línea y se realiza correctamente o no puede iniciar sesión en el usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-150">The webpage communicates with the online store and either succeeds or fails to log in the user.</span></span>
4.  <span data-ttu-id="4432f-151">Si el intento de inicio de sesión se realiza correctamente, la página web notifica al complemento de la tienda en línea llamando a [external. SendMessage](external-sendmessage.md), lo que da como resultado una llamada a [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="4432f-151">If the log-in attempt succeeds, the webpage notifies the online store's plug-in by calling [External.sendMessage](external-sendmessage.md), which results in a call to [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage).</span></span> <span data-ttu-id="4432f-152">El complemento de la tienda en línea determina que el intento de inicio de sesión se realizó correctamente mediante la inspección de los parámetros pasados a **IWMPContentPartner:: SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="4432f-152">The online store's plug-in determines that the log-in attempt succeeded by inspecting the parameters passed to **IWMPContentPartner::SendMessage**.</span></span> <span data-ttu-id="4432f-153">Los parámetros no son interpretados por Media Player de Windows; solo tienen significado en la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4432f-153">Those parameters are not interpreted by Windows Media Player; they have meaning only to the online store.</span></span> <span data-ttu-id="4432f-154">El complemento llama a **IWMPContentPartnerCallback:: Notify**, pasando Variant \_ true en el miembro **boolVal** del parámetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="4432f-154">The plug-in calls **IWMPContentPartnerCallback::Notify**, passing VARIANT\_TRUE in the **boolVal** member of the *pContext* parameter.</span></span> <span data-ttu-id="4432f-155">Si se produce un error en el inicio de sesión, la tienda en línea debe determinar cómo ayudar al usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-155">If the log-in fails, the online store must determine how to assist the user.</span></span> <span data-ttu-id="4432f-156">Una posibilidad es mostrar una nueva página web en la ventana modal que hospeda la Página Web de inicio de sesión alternativa.</span><span class="sxs-lookup"><span data-stu-id="4432f-156">One possibility is to display a new webpage in the modal window that hosts the alternative log-in webpage.</span></span>

## <a name="log-out"></a><span data-ttu-id="4432f-157">Cierre sesión.</span><span class="sxs-lookup"><span data-stu-id="4432f-157">Log-out</span></span>

<span data-ttu-id="4432f-158">El proceso de cierre de sesión implica los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4432f-158">The log-out process involves the following steps.</span></span>

1.  <span data-ttu-id="4432f-159">El usuario inicia un intento de cierre de sesión interactuando con la interfaz de usuario de Media Player de Windows o interactuando con una página de detección.</span><span class="sxs-lookup"><span data-stu-id="4432f-159">The user initiates a log-out attempt by interacting with the Windows Media Player user interface or by interacting with a discovery page.</span></span>
2.  <span data-ttu-id="4432f-160">Windows Media Player llama a [IWMPContentPartner:: Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), que se implementa mediante el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4432f-160">Windows Media Player calls [IWMPContentPartner::Logout](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout), which is implemented by the online store's plug-in.</span></span>
3.  <span data-ttu-id="4432f-161">El complemento se comunica con la tienda en línea y se realiza correctamente o no puede cerrar la sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-161">The plug-in communicates with the online store and either succeeds or fails to log out the user.</span></span>
4.  <span data-ttu-id="4432f-162">Si el intento de cierre de sesión se realiza correctamente, el complemento notifica a Windows Media Player llamando a **IWMPContentPartnerCallback:: Notify**, pasando Variant \_ false en el miembro **boolVal** del parámetro *pContext* .</span><span class="sxs-lookup"><span data-stu-id="4432f-162">If the log-out attempt succeeds, the plug-in notifies Windows Media Player by calling **IWMPContentPartnerCallback::Notify**, passing VARIANT\_FALSE in the **boolVal** member of the *pContext* parameter.</span></span>

<span data-ttu-id="4432f-163">Cuando un intento de iniciar o cerrar sesión se realiza correctamente, el complemento de la tienda en línea llama a **IWMPContentPartnerCallback:: Notify**, pasando wmpcnLoginStateChange en el parámetro de *tipo* .</span><span class="sxs-lookup"><span data-stu-id="4432f-163">When an attempt to log in or out is successful, the online store's plug-in calls **IWMPContentPartnerCallback::Notify**, passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="4432f-164">El complemento usa el parámetro *pContext* para especificar el estado de inicio de sesión actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-164">The plug-in uses the *pContext* parameter to specify the user's current log-in state.</span></span> <span data-ttu-id="4432f-165">Si el complemento establece *pContext* -> **boolVal** en Variant \_ true, el usuario ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4432f-165">If the plug-in sets *pContext*->**boolVal** to VARIANT\_TRUE, the user is logged in.</span></span> <span data-ttu-id="4432f-166">Si el complemento establece *pContext* -> **boolVal** en Variant \_ false, se cerrará la sesión del usuario. Tenga en cuenta que *pContext* no indica si el intento se realizó correctamente o no. en su lugar, indica el estado de inicio de sesión actual del usuario.</span><span class="sxs-lookup"><span data-stu-id="4432f-166">If the plug-in sets *pContext*->**boolVal** to VARIANT\_FALSE, the user is logged out. Note that *pContext* does not indicate the success or failure of the attempt; rather, it indicates user's current log-in state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4432f-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4432f-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4432f-168">**External. attemptLogin**</span><span class="sxs-lookup"><span data-stu-id="4432f-168">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="4432f-169">**Evento external. OnLoginChange**</span><span class="sxs-lookup"><span data-stu-id="4432f-169">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="4432f-170">**External. userLoggedIn**</span><span class="sxs-lookup"><span data-stu-id="4432f-170">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="4432f-171">**IWMPContentPartner:: login**</span><span class="sxs-lookup"><span data-stu-id="4432f-171">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="4432f-172">**IWMPContentPartner:: logout**</span><span class="sxs-lookup"><span data-stu-id="4432f-172">**IWMPContentPartner::Logout**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[<span data-ttu-id="4432f-173">**Guía de programación para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="4432f-173">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




