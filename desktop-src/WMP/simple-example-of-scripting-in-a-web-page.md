---
title: Ejemplo sencillo de scripting en una página web
description: Ejemplo sencillo de scripting en una página web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Windows Media Player, incrustar el control ActiveX
- Modelo de objetos de Windows Media Player, incrustar el control ActiveX
- modelo de objetos, incrustar el control ActiveX
- Windows Media Player Mobile, incrustar el control ActiveX
- Control ActiveX de Windows Media Player, incrustación
- Control ActiveX móvil de Windows Media Player, incrustación
- Control ActiveX, incrustación
- Control ActiveX de Windows Media Player, páginas web
- Control ActiveX móvil de Windows Media Player, páginas web
- Control ActiveX, páginas web
- Control ActiveX de Windows Media Player, ejemplo de scripting
- Control ActiveX móvil de Windows Media Player, ejemplo de scripting
- Control ActiveX, ejemplo de scripting
- incrustación, páginas web
- Incrustación de páginas web, ejemplo de scripting
- ejemplo de scripting para la inserción de páginas web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2019
ms.locfileid: "105704825"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="5ce73-119">Ejemplo sencillo de scripting en una página web</span><span class="sxs-lookup"><span data-stu-id="5ce73-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="5ce73-120">Puede incrustar fácilmente el control Media Player de Windows en un archivo HTML mediante cualquier lenguaje de scripting que reconozca el explorador.</span><span class="sxs-lookup"><span data-stu-id="5ce73-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="5ce73-121">En el siguiente ejemplo simple se usa Microsoft JScript para crear una página que reproducirá un archivo al hacer clic en un botón y detener la reproducción del archivo al hacer clic en otro botón.</span><span class="sxs-lookup"><span data-stu-id="5ce73-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="5ce73-122">Puede incrustar el control ActiveX de Windows Media Player en una página web mediante los cuatro pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="5ce73-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="5ce73-123">Cree la Página Web.</span><span class="sxs-lookup"><span data-stu-id="5ce73-123">Create the webpage.</span></span>
2.  <span data-ttu-id="5ce73-124">Agregue la etiqueta de objeto.</span><span class="sxs-lookup"><span data-stu-id="5ce73-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="5ce73-125">Agregue una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5ce73-125">Add a user interface.</span></span> <span data-ttu-id="5ce73-126">En este caso, dos botones.</span><span class="sxs-lookup"><span data-stu-id="5ce73-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="5ce73-127">Agregue algunas líneas de código para responder cuando el usuario haga clic en uno de los botones que ha creado.</span><span class="sxs-lookup"><span data-stu-id="5ce73-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="5ce73-128">Creación de la página web</span><span class="sxs-lookup"><span data-stu-id="5ce73-128">Creating the Web Page</span></span>

<span data-ttu-id="5ce73-129">El primer paso es crear una página web HTML válida.</span><span class="sxs-lookup"><span data-stu-id="5ce73-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="5ce73-130">El código siguiente es el mínimo necesario para crear una página HTML en blanco pero válida:</span><span class="sxs-lookup"><span data-stu-id="5ce73-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="5ce73-131">Agregar la etiqueta de objeto</span><span class="sxs-lookup"><span data-stu-id="5ce73-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="5ce73-132">Una vez que haya creado una página web, debe agregar una etiqueta de objeto.</span><span class="sxs-lookup"><span data-stu-id="5ce73-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="5ce73-133">Esto identifica el control ActiveX en el explorador y configura las definiciones iniciales.</span><span class="sxs-lookup"><span data-stu-id="5ce73-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="5ce73-134">Debe colocar la etiqueta de objeto en el cuerpo del código.</span><span class="sxs-lookup"><span data-stu-id="5ce73-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="5ce73-135">Si lo coloca en el cuerpo, se mostrará la interfaz de usuario predeterminada de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5ce73-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="5ce73-136">Si desea crear su propia interfaz de usuario, establezca los atributos height y width en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="5ce73-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="5ce73-137">También puede establecer el *reproductor*. la propiedad **uiMode** en "invisible" cuando se desea ocultar el control, pero aún se reserva espacio para él en la página.</span><span class="sxs-lookup"><span data-stu-id="5ce73-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="5ce73-138">El código siguiente se recomienda cuando se proporciona una interfaz de usuario personalizada:</span><span class="sxs-lookup"><span data-stu-id="5ce73-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="5ce73-139">Se requieren los siguientes atributos de etiqueta de objeto:</span><span class="sxs-lookup"><span data-stu-id="5ce73-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="5ce73-140">id</span><span class="sxs-lookup"><span data-stu-id="5ce73-140">ID</span></span>

<span data-ttu-id="5ce73-141">Nombre que usarán otras partes del código para identificar y usar el control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="5ce73-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="5ce73-142">Puede elegir cualquier nombre que desee, siempre que sea un nombre que no esté siendo utilizado por HTML, extensiones HTML o el lenguaje de scripting que esté usando.</span><span class="sxs-lookup"><span data-stu-id="5ce73-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="5ce73-143">En este ejemplo, se usa el nombre "Player", pero también puede llamarlo "Replay" u otra cosa.</span><span class="sxs-lookup"><span data-stu-id="5ce73-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="5ce73-144">Simplemente seleccione un nombre que sea único para esa página web.</span><span class="sxs-lookup"><span data-stu-id="5ce73-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="5ce73-145">CLASSID</span><span class="sxs-lookup"><span data-stu-id="5ce73-145">CLASSID</span></span>

<span data-ttu-id="5ce73-146">Un número hexadecimal muy grande que es único para el control.</span><span class="sxs-lookup"><span data-stu-id="5ce73-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="5ce73-147">Solo un control tiene este número y es el control ActiveX de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5ce73-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="5ce73-148">Para evitar errores tipográficos, puede copiar y pegar este número de la documentación.</span><span class="sxs-lookup"><span data-stu-id="5ce73-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="5ce73-149">Las versiones del control de Windows Media Player anteriores a la versión 7,0 tenían un CLASSID diferente.</span><span class="sxs-lookup"><span data-stu-id="5ce73-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="5ce73-150">Agregar una interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="5ce73-150">Adding a User Interface</span></span>

<span data-ttu-id="5ce73-151">HTML permite una gran cantidad de elementos de la interfaz de usuario, lo que permite al usuario interactuar con la página web haciendo clic, presionando las teclas y otras acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ce73-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="5ce73-152">Agregar algunos botones de entrada es la forma más fácil de proporcionar una interfaz de usuario rápida.</span><span class="sxs-lookup"><span data-stu-id="5ce73-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="5ce73-153">En el código siguiente se crean dos botones que pueden responder al usuario.</span><span class="sxs-lookup"><span data-stu-id="5ce73-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="5ce73-154">Al hacer clic en un botón, se inicia la reproducción del flujo multimedia y el otro botón lo detiene:</span><span class="sxs-lookup"><span data-stu-id="5ce73-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="5ce73-155">El nombre del botón se usa para identificar el botón en el código; el valor es la etiqueta que aparecerá en el botón y el atributo OnClick identifica a qué parte del código de script se llamará cuando se haga clic en el botón.</span><span class="sxs-lookup"><span data-stu-id="5ce73-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="5ce73-156">Agregar código de scripting</span><span class="sxs-lookup"><span data-stu-id="5ce73-156">Adding Scripting Code</span></span>

<span data-ttu-id="5ce73-157">El código de script agrega interactividad a la página.</span><span class="sxs-lookup"><span data-stu-id="5ce73-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="5ce73-158">El código de scripting puede responder a eventos, llamar a métodos y cambiar las propiedades de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5ce73-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="5ce73-159">Los scripts extendidos se incluyen en un conjunto de etiquetas de SCRIPT.</span><span class="sxs-lookup"><span data-stu-id="5ce73-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="5ce73-160">La etiqueta de SCRIPT indica al explorador que el código de scripting es e identifica el lenguaje de scripting.</span><span class="sxs-lookup"><span data-stu-id="5ce73-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="5ce73-161">Si no identifica un idioma, el idioma predeterminado será Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="5ce73-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="5ce73-162">Es aconsejable escribir el script en etiquetas de Comentario HTML para que los exploradores que no admiten el scripting no representen el código como texto.</span><span class="sxs-lookup"><span data-stu-id="5ce73-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="5ce73-163">Coloque la etiqueta de SCRIPT en cualquier parte del cuerpo del archivo HTML e inserte el código rodeado de comentarios dentro de las etiquetas de SCRIPT de apertura y cierre.</span><span class="sxs-lookup"><span data-stu-id="5ce73-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="5ce73-164">El siguiente ejemplo de código de Microsoft JScript llama al control Media Player de Windows y realiza una acción adecuada en respuesta al clic de botón correspondiente.</span><span class="sxs-lookup"><span data-stu-id="5ce73-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="5ce73-165">Se llama a la función de ejemplo, StartMeUp, cuando se hace clic en el botón de reproducción marcado de reproducción y se llama a la función ShutMeDown cuando se hace clic en el botón detener.</span><span class="sxs-lookup"><span data-stu-id="5ce73-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="5ce73-166">El código dentro de StartMeUp usa la propiedad URL para definir una ruta de acceso a los elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="5ce73-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="5ce73-167">Los elementos multimedia comenzarán a reproducirse inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5ce73-167">The media will start playing immediately.</span></span>

<span data-ttu-id="5ce73-168">El código ShutMeDown llama al método **Stop** del objeto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="5ce73-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="5ce73-169">Tenga en cuenta que se llama al objeto **Controls** mediante la propiedad **Controls** del objeto **Player** , que tiene el valor de ID de "Player".</span><span class="sxs-lookup"><span data-stu-id="5ce73-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="5ce73-170">En el código siguiente se muestra un ejemplo completo.</span><span class="sxs-lookup"><span data-stu-id="5ce73-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="5ce73-171">Tenga en cuenta que debe proporcionar una dirección URL válida a un nombre de archivo válido en la propiedad URL.</span><span class="sxs-lookup"><span data-stu-id="5ce73-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="5ce73-172">En este caso, se supone que el archivo Laure. WMA está en el mismo directorio que el archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="5ce73-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ce73-173">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ce73-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce73-174">**Usar el control Media Player de Windows en una página web**</span><span class="sxs-lookup"><span data-stu-id="5ce73-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




