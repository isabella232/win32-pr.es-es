---
title: Problemas de páginas web
description: Problemas de páginas web
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Listas de reproducción de metarchivos de Windows Media, páginas web
- listas de reproducción, páginas web
- listas de reproducción de metarchivos, páginas web
- Listas de reproducción de metarchivos de Windows Media, personalizar HTMLView
- listas de reproducción, personalizar HTMLView
- listas de reproducción de metarchivos, personalizar HTMLView
- Listas de reproducción de metarchivos de Windows Media, personalización de HTMLView
- listas de reproducción, personalización de HTMLView
- listas de reproducción de metarchivos, personalización de HTMLView
- Personalización de HTMLView
- Windows Media Player, páginas web
- Windows Media Player, personalizar HTMLView
- Windows Media Player, personalización de HTMLView
- HTMLView, personalizar
- HTMLView, páginas web
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778937"
---
# <a name="web-page-issues"></a><span data-ttu-id="cbffc-118">Problemas de páginas web</span><span class="sxs-lookup"><span data-stu-id="cbffc-118">Web Page Issues</span></span>

<span data-ttu-id="cbffc-119">Hay algunos aspectos que se deben tener en cuenta al crear una página web que se mostrará en la característica Windows Media Player **Now jugando** .</span><span class="sxs-lookup"><span data-stu-id="cbffc-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="cbffc-120">En esta sección se tratan algunos de los problemas que pueden surgir al crear el contenido basado en Web.</span><span class="sxs-lookup"><span data-stu-id="cbffc-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="cbffc-121">Personalización de HTMLView</span><span class="sxs-lookup"><span data-stu-id="cbffc-121">Customizing HTMLView</span></span>

<span data-ttu-id="cbffc-122">La Página Web de HTMLView puede ser tan simple o compleja como desee.</span><span class="sxs-lookup"><span data-stu-id="cbffc-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="cbffc-123">Puede incluir cualquiera de los elementos que utiliza normalmente en el contenido basado en Web.</span><span class="sxs-lookup"><span data-stu-id="cbffc-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="cbffc-124">Si incrusta el control Media Player de Windows, puede mostrar una de las interfaces de usuario proporcionadas por el control, crear su propia interfaz de usuario mediante código HTML y código de script, o no proporcionar ninguna interfaz de usuario (lo que significa que el usuario puede usar los controles de transporte del reproductor en modo completo).</span><span class="sxs-lookup"><span data-stu-id="cbffc-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="cbffc-125">El tamaño recomendado para las páginas web que se muestran mediante la característica HTMLView es 575 x 345 píxeles.</span><span class="sxs-lookup"><span data-stu-id="cbffc-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="cbffc-126">Sin embargo, el usuario tiene la capacidad de cambiar el tamaño de Windows Media Player y elegir la resolución de pantalla.</span><span class="sxs-lookup"><span data-stu-id="cbffc-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="cbffc-127">Si la Página Web de HTMLView es mayor que el tamaño que admite la característica de **reproducción en curso** , el reproductor muestra barras de desplazamiento horizontal y vertical que permiten al usuario ver toda la página.</span><span class="sxs-lookup"><span data-stu-id="cbffc-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="cbffc-128">Debe probar el contenido de HTMLView con una variedad de resoluciones de pantalla y tamaños de reproductor para determinar el mejor tamaño de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="cbffc-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="cbffc-129">Windows Media Player no proporciona un método que le permita especificar un tamaño para el reproductor en modo completo.</span><span class="sxs-lookup"><span data-stu-id="cbffc-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="cbffc-130">Navegación de páginas web</span><span class="sxs-lookup"><span data-stu-id="cbffc-130">Web page navigation</span></span>

<span data-ttu-id="cbffc-131">Windows Media Player no proporciona una barra de herramientas de navegación para las páginas web que se muestran en la característica **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="cbffc-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="cbffc-132">Esto significa que tiene un control total sobre si los usuarios pueden salir de la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="cbffc-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="cbffc-133">Si desea permitir que los usuarios naveguen a otras páginas web, debe incluir elementos en el código HTML para proporcionar esa funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="cbffc-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="cbffc-134">Recuperar la ventana primaria</span><span class="sxs-lookup"><span data-stu-id="cbffc-134">Retrieving the parent window</span></span>

<span data-ttu-id="cbffc-135">Si el código de script existente utiliza **window. Parent** para recuperar el objeto de ventana principal, este código no funcionará en la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="cbffc-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="cbffc-136">Cuando se usa HTMLView, no hay ningún objeto de ventana principal; por lo tanto, esta característica de scripting no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cbffc-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="cbffc-137">Acerca del explorador incrustado</span><span class="sxs-lookup"><span data-stu-id="cbffc-137">About the embedded browser</span></span>

<span data-ttu-id="cbffc-138">Dado que Windows Media Player usa una instancia incrustada de Internet Explorer para mostrar el contenido de HTMLView, la configuración de usuario y las directivas de Internet Explorer se aplican a las páginas web que se muestran en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="cbffc-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="cbffc-139">Por ejemplo, si el usuario ha configurado Internet Explorer para evitar que las páginas web descarguen cookies en el equipo, la Página Web de HTMLView también se impide hacerlo.</span><span class="sxs-lookup"><span data-stu-id="cbffc-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="cbffc-140">Las páginas web que se abren mediante la característica HTMLView siempre se ejecutan en la zona de seguridad de **Internet** de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cbffc-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="cbffc-141">El control de explorador Web incrustado utiliza las mismas reglas para almacenar en caché las páginas web como la versión independiente de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cbffc-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="cbffc-142">Se recomienda usar páginas de Active Server (ASP) al crear el contenido para asegurarse de que el contenido se entregue desde el servidor web cada vez que Windows Media Player acceda a la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="cbffc-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="cbffc-143">El uso de páginas ASP puede ser tan sencillo como cambiar el nombre de la página web para usar una extensión de nombre de archivo. asp.</span><span class="sxs-lookup"><span data-stu-id="cbffc-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="cbffc-144">Acerca del contenido Web local</span><span class="sxs-lookup"><span data-stu-id="cbffc-144">About local Web content</span></span>

<span data-ttu-id="cbffc-145">La característica HTMLView no permite abrir páginas web almacenadas en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="cbffc-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="cbffc-146">Preguntar al usuario</span><span class="sxs-lookup"><span data-stu-id="cbffc-146">Prompting the user</span></span>

<span data-ttu-id="cbffc-147">Puede usar **window. prompt** para solicitar información al usuario.</span><span class="sxs-lookup"><span data-stu-id="cbffc-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="cbffc-148">Sin embargo, **window. Alert** y **window. CONFIRM** no están disponibles cuando se usa HTMLView.</span><span class="sxs-lookup"><span data-stu-id="cbffc-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="cbffc-149">Problemas de temporización</span><span class="sxs-lookup"><span data-stu-id="cbffc-149">Timing issues</span></span>

<span data-ttu-id="cbffc-150">Puede encontrar problemas de temporización al utilizar un control de Media Player de Windows incrustado en la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="cbffc-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="cbffc-151">En HTMLView, un control de reproductor incrustado comparte su motor de reproducción con la Media Player de Windows independiente.</span><span class="sxs-lookup"><span data-stu-id="cbffc-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="cbffc-152">Es posible que el reproductor independiente pueda abrir y comenzar a reproducir la primera entrada de la lista de reproducción antes de que la página web (y, por lo tanto, el control del reproductor) termine de cargarse.</span><span class="sxs-lookup"><span data-stu-id="cbffc-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="cbffc-153">Esto significa que, si controla los eventos **OpenStateChange** o **PlayStateChange** , el código de script no recibirá notificaciones de eventos para estos eventos hasta que se carguen el control de reproducción y sus objetos asociados.</span><span class="sxs-lookup"><span data-stu-id="cbffc-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="cbffc-154">Puede realizar los pasos del código para retrasar la reproducción hasta que se cree una instancia del control de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbffc-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="cbffc-155">Una manera de hacerlo es hacer que la primera entrada de la lista de reproducción del metarchivo apunte a un archivo de imagen y establecer la duración del archivo en un período de tiempo que permita que se cargue el control del reproductor.</span><span class="sxs-lookup"><span data-stu-id="cbffc-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="cbffc-156">En el código de ejemplo siguiente se muestra esta opción:</span><span class="sxs-lookup"><span data-stu-id="cbffc-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="cbffc-157">Cuando se abre la lista de reproducción anterior, Windows Media Player espera en la primera entrada de la lista de reproducción hasta un minuto mientras el reproductor carga la Página Web de HTMLView.</span><span class="sxs-lookup"><span data-stu-id="cbffc-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="cbffc-158">Después, en la Página Web de HTMLView, escriba el código de script para controlar el evento **OnLoad** del elemento **Body** .</span><span class="sxs-lookup"><span data-stu-id="cbffc-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="cbffc-159">En la función de controlador de eventos, llame al método Player **Controls. Next** para comenzar la reproducción de la segunda entrada en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cbffc-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="cbffc-160">Cuando finaliza la carga de la página web en el ejemplo anterior, Windows Media Player avanza inmediatamente a la segunda entrada de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cbffc-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="cbffc-161">Esto invalida la duración especificada para el primer elemento de la lista de reproducción, lo que significa que el usuario no tiene que esperar todo un minuto antes de ver el contenido deseado. solo tiene que esperar a que la página web termine de cargarse.</span><span class="sxs-lookup"><span data-stu-id="cbffc-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="cbffc-162">Dado que en este punto se crean instancias completas del control Player, los eventos **OpenStateChange** y **PlayStateChange** se pueden controlar de la manera habitual.</span><span class="sxs-lookup"><span data-stu-id="cbffc-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbffc-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbffc-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbffc-164">**Mostrar páginas web en Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="cbffc-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="cbffc-165">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="cbffc-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="cbffc-166">**Evento Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="cbffc-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




