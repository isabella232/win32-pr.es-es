---
title: Personalización de la vista Web de una carpeta
description: Una vista Web es una forma eficaz y flexible de usar el explorador de Windows para mostrar información sobre el contenido de una carpeta de Shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Vistas Web
- Estilo clásico
- Estilo Web
- titulares
- Región FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e364551d461eff6ae17a780bafc0b69182a1f16f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789670"
---
# <a name="customizing-a-folders-web-view"></a><span data-ttu-id="dbf1d-108">Personalización de la vista Web de una carpeta</span><span class="sxs-lookup"><span data-stu-id="dbf1d-108">Customizing a Folder's Web View</span></span>

<span data-ttu-id="dbf1d-109">\[Esta característica solo se admite en Windows XP o versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-109">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="dbf1d-110">\]</span><span class="sxs-lookup"><span data-stu-id="dbf1d-110">\]</span></span>

<span data-ttu-id="dbf1d-111">Una vista Web es una forma eficaz y flexible de usar el explorador de Windows para mostrar información sobre el contenido de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-111">A Web view is a powerful and flexible way to use the Windows Explorer to display information about the contents of a Shell folder.</span></span>

-   [<span data-ttu-id="dbf1d-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="dbf1d-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="dbf1d-113">Usar la plantilla Vista Web</span><span class="sxs-lookup"><span data-stu-id="dbf1d-113">Using the Web View Template</span></span>](#using-the-web-view-template)
    -   [<span data-ttu-id="dbf1d-114">El cuerpo de la plantilla</span><span class="sxs-lookup"><span data-stu-id="dbf1d-114">The Template Body</span></span>](#the-template-body)
    -   [<span data-ttu-id="dbf1d-115">El encabezado de la plantilla</span><span class="sxs-lookup"><span data-stu-id="dbf1d-115">The Template Head</span></span>](#the-template-head)
-   [<span data-ttu-id="dbf1d-116">Resumen</span><span class="sxs-lookup"><span data-stu-id="dbf1d-116">Summary</span></span>](#summary)

## <a name="introduction"></a><span data-ttu-id="dbf1d-117">Introducción</span><span class="sxs-lookup"><span data-stu-id="dbf1d-117">Introduction</span></span>

<span data-ttu-id="dbf1d-118">Windows ofrece a los usuarios dos maneras principales de ver y navegar por el espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-118">Windows offers users two primary ways to view and navigate the Shell namespace.</span></span> <span data-ttu-id="dbf1d-119">Lo más familiar, el estilo clásico, es similar al conocido administrador de archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-119">The most familiar of these, the Classic style, is similar to the familiar Windows File Manager.</span></span> <span data-ttu-id="dbf1d-120">En el panel derecho se muestra el contenido de la carpeta actualmente seleccionada en uno de los cinco formatos siguientes: iconos grandes, iconos pequeños, lista, detalles y miniatura.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-120">The right pane lists the contents of the currently selected folder in one of five formats: Large Icon, Small Icon, List, Details, and Thumbnail.</span></span> <span data-ttu-id="dbf1d-121">La diferencia principal del administrador de archivos de Windows es el panel izquierdo, que es muy similar a la barra del explorador de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-121">The major difference from Windows File Manager is the left pane, which looks very similar to the Explorer bar of Windows Internet Explorer.</span></span> <span data-ttu-id="dbf1d-122">Se puede cambiar de tamaño o quitar, y puede mostrar varios paneles además del árbol del sistema de archivos conocido, como un panel de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-122">It can be resized or removed, and it can display several panes in addition to the familiar file system tree, such as a search pane.</span></span>

> [!Note]  
> <span data-ttu-id="dbf1d-123">La información de este documento no se aplica a Windows XP, las técnicas descritas solo se aplican a versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-123">The information in this document does not apply to Windows XP, the techniques discussed apply only to earlier versions of Windows.</span></span>

 

<span data-ttu-id="dbf1d-124">En la ilustración siguiente se muestra la carpeta Impresoras en estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-124">The following illustration shows the Printers folder in Classic style.</span></span>

![estilo clásico de la carpeta de impresoras.](images/webview1.png)

<span data-ttu-id="dbf1d-126">El estilo clásico funciona razonablemente bien para carpetas y archivos normales del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-126">The Classic style works reasonably well for normal file system folders and files.</span></span> <span data-ttu-id="dbf1d-127">Sin embargo, con la introducción de Windows 95, el sistema de archivos ha evolucionado en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-127">However, with the introduction of Windows 95, the file system has evolved into the namespace.</span></span> <span data-ttu-id="dbf1d-128">El espacio de nombres permite la creación de *carpetas virtuales*, como las impresoras o el entorno de red, que pueden representar tipos de información muy diferentes de los de una carpeta de sistema de archivos normal.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-128">The namespace allows the creation of *virtual folders*, such as Printers or Network Neighborhood, that can represent very different types of information than a normal file system folder.</span></span>

<span data-ttu-id="dbf1d-129">El estilo Web, también conocido como vista Web, ofrece una manera más flexible y eficaz de presentar información que el estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-129">The Web style, also known as a Web view, offers a more flexible and powerful way of presenting information than Classic style.</span></span> <span data-ttu-id="dbf1d-130">En una vista Web, el usuario básicamente ve y navega por el espacio de nombres mediante Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-130">In a Web view, the user basically views and navigates the namespace using Internet Explorer.</span></span> <span data-ttu-id="dbf1d-131">El diseño básico de una vista Web es similar al estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-131">The basic layout of a Web view is similar to Classic style.</span></span> <span data-ttu-id="dbf1d-132">La barra del explorador no cambia.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-132">The Explorer bar is unchanged.</span></span> <span data-ttu-id="dbf1d-133">Sin embargo, la región ocupada por la lista de archivos se convierte en un área de visualización de uso general que es realmente una página web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-133">However, the region that was occupied by the file list becomes a general-purpose display area that is effectively a webpage.</span></span> <span data-ttu-id="dbf1d-134">Una vista Web todavía se usa para mostrar información sobre el contenido de una carpeta, pero hay pocas restricciones en cuanto a la información que se muestra o cómo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-134">A Web view is still used to display information about the contents of a folder, but there are few constraints on what information is displayed, or how.</span></span> <span data-ttu-id="dbf1d-135">Cada carpeta puede tener su propia vista Web, personalizada para adaptarse a sus características concretas.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-135">Each folder can have its own Web view, customized to suit its particular features.</span></span>

<span data-ttu-id="dbf1d-136">En la ilustración siguiente se muestra una vista Web de la carpeta Impresoras (mostrada anteriormente en estilo clásico).</span><span class="sxs-lookup"><span data-stu-id="dbf1d-136">The following illustration shows a Web view of the Printers folder (shown previously in Classic style).</span></span>

![Vista Web predeterminada de la carpeta de impresoras.](images/webview2.png)

<span data-ttu-id="dbf1d-138">Al igual que las páginas web convencionales, las vistas Web se controlan mediante una plantilla basada en HTML.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-138">Much like conventional webpages, Web views are controlled by an HTML-based template.</span></span> <span data-ttu-id="dbf1d-139">La creación de una plantilla de vista Web es prácticamente idéntica a la creación de una página web y proporciona el mismo grado de flexibilidad en el contenido y el diseño de la información.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-139">Authoring a Web view template is nearly identical to authoring a webpage and provides the same degree of flexibility in content and layout of information.</span></span> <span data-ttu-id="dbf1d-140">Las plantillas de vista Web pueden usar HTML dinámico (DHTML) y scripting para responder a eventos, como un usuario que hace clic en un elemento.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-140">Web view templates can use Dynamic HTML (DHTML) and scripting to respond to events, such as a user clicking an item.</span></span> <span data-ttu-id="dbf1d-141">También pueden hospedar objetos que les permiten obtener y Mostrar información de la carpeta o de su contenido.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-141">They can also host objects that allow them to obtain and display information from the folder or its contents.</span></span>

<span data-ttu-id="dbf1d-142">El usuario puede elegir una vista Web iniciando el explorador de Windows, haciendo clic en **Opciones de carpeta** en el menú **Ver** y seleccionando esta opción: **Habilitar contenido web en carpetas**.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-142">The user can choose a Web view by starting Windows Explorer, clicking **Folder Options** on the **View** menu, and selecting this option: **Enable Web content in folders**.</span></span> <span data-ttu-id="dbf1d-143">Sin embargo, el usuario también puede iniciar Internet Explorer y señalar el explorador en el sistema de archivos; para ello, haga clic en el menú **Ver** , seleccione **barra del explorador** y haga clic en **carpetas**.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-143">However, the user can also start Internet Explorer and point the browser at the file system by clicking the **View** menu, pointing to **Explorer Bar**, and clicking **Folders**.</span></span> <span data-ttu-id="dbf1d-144">En una vista Web, no hay prácticamente ninguna diferencia entre Internet Explorer y el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-144">In a Web view, there is virtually no difference between Internet Explorer and Windows Explorer.</span></span>

<span data-ttu-id="dbf1d-145">En el lado izquierdo del panel derecho, la vista Web impresoras muestra un banner con el nombre y el icono de la carpeta, seguido de un bloque de información sobre la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-145">On the left side of the right pane, the Printers Web view displays a banner with the folder's name and icon, followed by a block of information about the folder.</span></span> <span data-ttu-id="dbf1d-146">La lista de archivos habitual ocupa el lado derecho de la página.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-146">The usual file list occupies the right side of the page.</span></span>

<span data-ttu-id="dbf1d-147">Cuando un usuario hace clic en un elemento, en el bloque de información aparece información detallada sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-147">When a user clicks an item, detailed information about the item appears in the information block.</span></span> <span data-ttu-id="dbf1d-148">La vista Web de impresoras muestra realmente la misma información que está disponible en el estilo clásico, pero lo hace en un formato más utilizable.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-148">The Printers Web view actually displays much the same information that is available in Classic style, but it does so in a more usable format.</span></span> <span data-ttu-id="dbf1d-149">Sin embargo, una vista Web no es simplemente una manera diferente de Mostrar información de estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-149">However, a Web view is not simply a different way to display Classic style information.</span></span> <span data-ttu-id="dbf1d-150">Por ejemplo, se puede mostrar un vínculo a un sitio web útil debajo del bloque de información, una característica que no está disponible en el estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-150">For example, a link to a useful website can be displayed below the information block, a feature that is not available in Classic style.</span></span> <span data-ttu-id="dbf1d-151">Si el usuario hace clic en el vínculo, se mostrará el sitio.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-151">If the user clicks the link, the site will be displayed.</span></span>

<span data-ttu-id="dbf1d-152">La vista Web de impresoras mostrada en la ilustración anterior es similar al estilo clásico, porque la plantilla de vista Web subyacente (un archivo. htt) se escribió de este modo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-152">The Printers Web view shown in the preceding illustration is similar to the Classic style, because the underlying Web view template (an .htt file) was written that way.</span></span> <span data-ttu-id="dbf1d-153">La lista de archivos, por ejemplo, no se genera directamente en la plantilla de vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-153">The list of files, for instance, is not generated by the Web view template directly.</span></span> <span data-ttu-id="dbf1d-154">Se crea y muestra mediante un objeto [**WebViewFolderContents**](webviewfoldercontents.md) hospedado por la plantilla de vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-154">It is created and displayed by a [**WebViewFolderContents**](webviewfoldercontents.md) object hosted by the Web view template.</span></span> <span data-ttu-id="dbf1d-155">Los métodos y las propiedades del objeto permiten a la vista Web controlar su diseño y obtener información sobre elementos concretos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-155">The object's methods and properties allow the Web view to control its layout and obtain information about particular items.</span></span> <span data-ttu-id="dbf1d-156">El contenido y el diseño del encabezado y el bloque de información se especifican en la plantilla de vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-156">The content and layout of the banner and information block is specified in the Web view template.</span></span>

<span data-ttu-id="dbf1d-157">Dado que una vista Web es compatible con DHTML, la plantilla también se puede utilizar para controlar la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-157">Because a Web view supports DHTML, the template can also be used to handle user interaction.</span></span> <span data-ttu-id="dbf1d-158">Por ejemplo, cuando un usuario hace clic en uno de los iconos de la impresora, el objeto **WebViewFolderIcon** activa un evento [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) .</span><span class="sxs-lookup"><span data-stu-id="dbf1d-158">For instance, when a user clicks one of the printer icons, the **WebViewFolderIcon** object fires a [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) event.</span></span> <span data-ttu-id="dbf1d-159">La plantilla usa un controlador de eventos DHTML escrito en el script para recuperar la información solicitada y mostrarla en el bloque de información.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-159">The template uses a DHTML event handler written in script to retrieve the requested information and display it in the information block.</span></span>

<span data-ttu-id="dbf1d-160">Este sencillo ejemplo de la carpeta de impresoras no es, la única manera de usar una vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-160">This simple example for the Printers folder is by no means the only way to use a Web view.</span></span> <span data-ttu-id="dbf1d-161">Si escribe su propia plantilla y, si es necesario, los objetos, puede usar una vista Web para mostrar información e interactuar con el usuario de la forma que más le convenga.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-161">By writing your own template and, if necessary, objects, you can use a Web view to display information and interact with the user in whatever way you find most effective.</span></span> <span data-ttu-id="dbf1d-162">Tenga en cuenta que, en la actualidad, las plantillas de vista web solo muestran carpetas virtuales definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-162">Note that, at present, Web view templates only display system-defined virtual folders.</span></span> <span data-ttu-id="dbf1d-163">Aunque los desarrolladores pueden crear una carpeta virtual mediante la implementación de una extensión de espacio de nombres, deben usar las técnicas descritas en [extensiones de espacio de nombres](/windows/desktop/shell/nse-works) para mostrarla.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-163">Although developers can create a virtual folder by implementing a namespace extension, they must use the techniques described in [Namespace Extensions](/windows/desktop/shell/nse-works) to display it.</span></span>

## <a name="using-the-web-view-template"></a><span data-ttu-id="dbf1d-164">Usar la plantilla Vista Web</span><span class="sxs-lookup"><span data-stu-id="dbf1d-164">Using the Web View Template</span></span>

<span data-ttu-id="dbf1d-165">La forma en que se muestran los datos en una vista Web puede personalizarse de una manera limitada modificando el archivo de Desktop.ini de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-165">The way data is displayed in a Web view can be customized in a limited way by modifying a folder's Desktop.ini file.</span></span> <span data-ttu-id="dbf1d-166">Consulte [Personalización de carpetas con Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-166">See [Customizing Folders with Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) for details.</span></span> <span data-ttu-id="dbf1d-167">Una manera mucho más flexible y eficaz de personalizar una vista Web es crear una plantilla de vista web personalizada.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-167">A much more flexible and powerful way to customize a Web view is to create a custom Web view template.</span></span>

<span data-ttu-id="dbf1d-168">La plantilla Vista Web controla lo que se muestra en una vista Web y cómo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-168">The Web view template controls what is displayed in a Web view and how.</span></span> <span data-ttu-id="dbf1d-169">Utiliza las técnicas estándar de HTML, DHTML y scripting para obtener y Mostrar información e interactuar con el usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-169">It uses standard HTML, DHTML, and scripting techniques to obtain and display information and interact with the user.</span></span> <span data-ttu-id="dbf1d-170">En esta sección se describe cómo crear una vista Web mediante el examen de una plantilla simple: Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-170">This section discusses how to create a Web view by examining a simple template—Generic.htt.</span></span>


```
<html>
    <style>
    <!-- This section defines a variety of styles that can be used
     when displaying the document -->
        body        {font: 8pt/10pt verdana; margin: 0}
        #Banner     {position: absolute; width: 100%; height: 88px; background: URL(res://webvw.dll/folder.gif) no-repeat top left}
        #MiniBanner {position: absolute; width: 100%; height: 32px; background: window}
        #Icon       {position: absolute; left: 11px; top: 12px; width: 64px; height: 64px}
        #FileList   {position: absolute; left: 30%; top: 88px; width: 1px; height: 1px}
        #Info       {position: absolute; top: 88px; width: 30%; background: window; overflow: auto}
        p       {margin-left: 20px; margin-right: 8px}
        p.Title     {font: 16pt/16pt verdana; font-weight: bold; color: #0099FF}
        a:link      {color: #FF6633}
        a:visited   {color: #0099FF}
        a:active    {color: black}
    </style>

    <head>
        <!-- allow references to any resources you might add to the
         folder -->
        <base href="%THISDIRPATH%\">

        <script language="JavaScript">
        
        <!-- This section defines a number of JavaScript utilities -->
            var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br><br>To get information about any of them, click the items icon.<br><br>";
            var L_Multiple_Text = " objects selected.";

            function FixSize() {
            // this function handles layout issues not covered by the style sheet

                var hideTop = 200;
                var hideLeft    = 400;
                var miniHeight  = 32;

                if (200 > document.body.clientHeight) {
                //A short window. Use the minibanner
                    document.all.Banner.style.visibility = "hidden";
                    document.all.MiniBanner.style.visibility = "visible";
                    document.all.FileList.style.top = 32;
                    document.all.Info.style.top = 32;
                }

                else {
                //A normal window. Use the normal banner
                    document.all.Banner.style.visibility = "visible";
                    document.all.MiniBanner.style.visibility = "hidden";
                    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
                    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
                    document.all.Rule.style.width = (document.body.clientWidth > 84 ? document.body.clientWidth - 84 : 0) + "px";     
                }
                if (400 > document.body.clientWidth) {
                //A narrow window. Hide the Info region and expand the file list region
                    document.all.Info.style.visibility = "hidden";
                    document.all.FileList.style.pixelLeft = 0;
                    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
                }

                else {
                //Normal width
                    document.all.Info.style.visibility = "visible";
                    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
                }
                document.all.FileList.style.pixelWidth = document.body.clientWidth - document.all.FileList.style.pixelLeft;
                document.all.FileList.style.pixelHeight = document.body.clientHeight - document.all.FileList.style.pixelTop;
                document.all.Info.style.pixelHeight = document.body.clientHeight - document.all.Info.style.pixelTop;
            }

            function Init() {
                /* Set the initial layout and have FixSize() called whenever the window is resized*/
                window.onresize = FixSize;
                FixSize();
                TextBlock.innerHTML = L_Intro_Text;
            }
        </script>

        <script language="JavaScript" for="FileList" event="SelectionChanged">
            // Updates the TextBlock region when an item is selected
            var data;
            var text;

            // name
            text = "<b>" + FileList.FocusedItem.Name + "</b>";

            // comment
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
            if (data)
                text += "<br>" + data;

            // documents
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
            if (data)
                text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

            // status
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
            if (data)
                text += "<br><br><b><font color=red>" + data + "</font></b>";

            // tip?
            data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
            if (data != "" && data != FileList.FocusedItem.Name)
                text += "<br><br>" + data;

            TextBlock.innerHTML = text;
        </script>
    </head>
<!-- The body of the document controls the actual data display.
 It uses several scripting objects to communicate with the
 namespace folder, and calls on the JavaScript objects defined
 in the header to handle much of the processing -->
    <body scroll=no onload="Init()">

        <!-- The normal banner. This banner displays the folder
         name and icon at the top of the WebView pane. This banner
         is used if the WebView pane is sufficiently large to
         display the icon and still have room for some information -->
        <div id="Banner" style="visibility: hidden">
            <!-- Display the folder name using a table with nowrap
             to prevent word wrapping. Explorer will replace
              %THISDIRNAME% with the current folder name -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 104px; margin-top: 16px">
                %THISDIRNAME% 
            </td></tr></table>
            <!-- this is more efficient than a long graphic, but it has to be adjusted in FixSize() -->
            <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
            <!-- Load the WebViewFolderIcon object, which extracts the folder's icon -->
            <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
                <param name="scale" value=200>
            </object>
        </div>

        <!-- The mini banner. This banner is used when the
         WebView pane is too short to display the icon. Instead,
          it displays only the folder name -->
        <div id="MiniBanner" style="visibility: hidden">
            <!-- use a table with nowrap to prevent word wrapping -->
            <table class="clsStd"><tr><td nowrap>
                <p class=Title style="margin-left: 16px; margin-top: 4px">
                %THISDIRNAME%
            </td></tr></table>
        </div>

        <!-- The Info region. This displays the information
         associated with a folder or file. Javascript in the header
         is used to generate the regions contents by by assigning
         a text block to TextBlock.innerHTML -->
        <div id="Info">
            <p style="margin-top: 16px");
            <span id="TextBlock">
            </span>
        </div>
        <!-- end left info panel -->

        <!-- Load the WebViewFolderContents object. This object
         returns information on the contents of the folder that
          can be used in the information display.  -->
        <object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>

    </body>
</html>
            
```



<span data-ttu-id="dbf1d-171">Una manera sencilla de crear su propia plantilla de vista Web es usar Generic. htt y modificarla.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-171">A simple way to create your own Web view template is to take Generic.htt and modify it.</span></span> <span data-ttu-id="dbf1d-172">Dado que es bastante limitado, también debe examinar otros ejemplos más complejos para ver ideas adicionales.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-172">Because it is rather limited, you should also look at other, more complex examples for additional ideas.</span></span> <span data-ttu-id="dbf1d-173">Puede encontrarlos buscando en el sistema la extensión. htt usada por todas las plantillas de vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-173">You can find them by searching your system for the .htt extension used by all Web view templates.</span></span> <span data-ttu-id="dbf1d-174">Si desea crear una plantilla personalizada para una carpeta, debe comenzar con la plantilla default. htt, que normalmente se almacena en C: \\ WinNT \\ Web o c: \\ Windows \\ Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-174">If you want to create a custom template for a folder, you should start with the default Folder.htt template, which is usually stored in either C:\\Winnt\\Web or C:\\Windows\\Web.</span></span> <span data-ttu-id="dbf1d-175">Tenga en cuenta que estos archivos se definen como ocultos, por lo que es posible que tenga que modificar la configuración del explorador de Windows para verlos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-175">Note that these files are defined as hidden, so you may need to modify your Windows Explorer settings to view them.</span></span> <span data-ttu-id="dbf1d-176">Una vez creado un archivo. htt, debe marcarse como de solo lectura y estar oculto.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-176">Once an .htt file is created, it should be marked as read-only and hidden.</span></span>

<span data-ttu-id="dbf1d-177">Las plantillas de vista web usan la extensión. htt porque difieren ligeramente de los documentos convencionales. htm.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-177">Web view templates use the .htt extension because they differ slightly from conventional .htm documents.</span></span> <span data-ttu-id="dbf1d-178">La diferencia principal son varias variables especiales en los archivos. htt que el sistema reemplaza con los valores de espacio de nombres actuales.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-178">The main difference is several special variables in .htt files that the system replaces with the current namespace values.</span></span> <span data-ttu-id="dbf1d-179">Las variables% THISDIR% y% THISDIRPATH% representan el nombre y la ruta de acceso de la carpeta actualmente seleccionada.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-179">The %THISDIR% and %THISDIRPATH% variables represent the name and path of the currently selected folder.</span></span> <span data-ttu-id="dbf1d-180">La variable% TEMPLATEDIR% representa la carpeta donde se almacenan las hojas de estilos de vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-180">The %TEMPLATEDIR% variable represents the folder where the Web view style sheets are stored.</span></span>

<span data-ttu-id="dbf1d-181">Al igual que la mayoría de las plantillas HTML, los archivos. htt tienen dos partes básicas: un cuerpo y un encabezado.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-181">Like most HTML templates, .htt files have two basic parts: a body and a head.</span></span> <span data-ttu-id="dbf1d-182">El cuerpo de la plantilla controla el diseño básico de la vista Web y carga los objetos utilizados para comunicarse con el espacio de nombres y Mostrar información.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-182">The template body controls the basic layout of the Web view and loads the objects used to communicate with the namespace and display information.</span></span> <span data-ttu-id="dbf1d-183">El encabezado contiene scripts y funciones que realizan tareas como controlar el cambio de tamaño y obtener información de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-183">The head contains scripts and functions that do tasks such as handling resizing and obtaining information from the folder.</span></span> <span data-ttu-id="dbf1d-184">La mayoría de las plantillas, incluido Generic. htt, también incluyen una hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-184">Most templates, including Generic.htt, also include a style sheet.</span></span> <span data-ttu-id="dbf1d-185">En general, es mejor incluir la información de la hoja de estilos en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-185">In general, it is better to include the style sheet information in your template.</span></span> <span data-ttu-id="dbf1d-186">Es posible que las hojas de estilos independientes no funcionen correctamente cuando se utiliza una vista Web con espacios de nombres remotos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-186">Separate style sheets may not work properly when a Web view is used with remote namespaces.</span></span>

### <a name="the-template-body"></a><span data-ttu-id="dbf1d-187">El cuerpo de la plantilla</span><span class="sxs-lookup"><span data-stu-id="dbf1d-187">The Template Body</span></span>

<span data-ttu-id="dbf1d-188">El cuerpo de la plantilla especifica lo que presentará una vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-188">The body of the template specifies what will be presented by a Web view.</span></span> <span data-ttu-id="dbf1d-189">También es donde se cargan los objetos que se usan para mostrar información y comunicarse con las carpetas de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-189">It is also where the objects used to display information and communicate with namespace folders are loaded.</span></span> <span data-ttu-id="dbf1d-190">El diseño definido por Generic. htt es similar al que se muestra en la ilustración de la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-190">The layout defined by Generic.htt is similar to that shown in the illustration in the previous section.</span></span> <span data-ttu-id="dbf1d-191">Hay tres regiones para mostrar: el titular y el bloque de información en el lado izquierdo de la vista, y la lista de archivos a la derecha.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-191">There are three display regions: the banner and information block on the left side of the view, and the file list on the right.</span></span>

<span data-ttu-id="dbf1d-192">Todas las regiones son identificadores asignados que van a usar la hoja de estilos y DHTML.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-192">The regions are all assigned identifiers to be used by the style sheet and DHTML.</span></span> <span data-ttu-id="dbf1d-193">Como se describe en la sección siguiente, hay dos banners posibles, con identificadores de "Banner" y "MiniBanner".</span><span class="sxs-lookup"><span data-stu-id="dbf1d-193">As discussed in the next section, there are two possible banners, with identifiers of "Banner" and "MiniBanner".</span></span> <span data-ttu-id="dbf1d-194">El identificador de la región del bloque de información es "info".</span><span class="sxs-lookup"><span data-stu-id="dbf1d-194">The identifier of the information block's region is "Info".</span></span> <span data-ttu-id="dbf1d-195">El identificador del objeto de la lista de archivos es "FileList".</span><span class="sxs-lookup"><span data-stu-id="dbf1d-195">The file list object's identifier is "FileList".</span></span> <span data-ttu-id="dbf1d-196">Los detalles del [diseño](#controlling-the-web-view-layout) de la región se controlan mediante la hoja de estilos y una función de Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), que se describe más adelante en el capítulo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-196">The details of the region's [layout](#controlling-the-web-view-layout) are handled by the style sheet and a Microsoft JScript function, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), which is discussed later in the chapter.</span></span>

### <a name="the-banner-region"></a><span data-ttu-id="dbf1d-197">La región del banner</span><span class="sxs-lookup"><span data-stu-id="dbf1d-197">The Banner Region</span></span>

<span data-ttu-id="dbf1d-198">El banner se encuentra en la parte superior de la pantalla, en la esquina superior izquierda de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-198">The banner is located at the top of the display, in the upper-left corner of the Web view.</span></span> <span data-ttu-id="dbf1d-199">El banner normal muestra el nombre y el icono de la carpeta cuyo contenido se muestra en la lista de archivos de la derecha.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-199">The normal banner displays the name and icon of the folder whose contents are displayed in the file list on the right.</span></span> <span data-ttu-id="dbf1d-200">Sin embargo, si la ventana es demasiado corta, puede que no haya espacio debajo del icono para mostrar la información.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-200">However, if the window becomes too short, there may be no room below the icon to display information.</span></span> <span data-ttu-id="dbf1d-201">Por esta razón, Generic. htt también define un minibanner que solo muestra el nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-201">For this reason, Generic.htt also defines a minibanner that only displays the folder name.</span></span> <span data-ttu-id="dbf1d-202">Ambos banners se definen inicialmente como ocultos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-202">Both banners are initially defined as hidden.</span></span> <span data-ttu-id="dbf1d-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) elige cuál Mostrar y lo establece en "visible".</span><span class="sxs-lookup"><span data-stu-id="dbf1d-203">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) chooses which one to display and sets it to "visible".</span></span>

<span data-ttu-id="dbf1d-204">El banner normal de Generic. htt se define mediante:</span><span class="sxs-lookup"><span data-stu-id="dbf1d-204">The normal banner for Generic.htt is defined by:</span></span>


```
<div id="Banner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
    <p class=Title style="margin-left: 104px; margin-top: 16px">
        %THISDIRNAME% 
    </td></tr></table>
    <hr id="Rule" size=1px color=black style="position: absolute; top: 44px; left: 84px">
    <object id=Icon classid="clsid:e5df9d10-3b52-11d1-83e8-00a0c90dc849">
        <param name="scale" value=200>
    </object>
</div>
                    
```



<span data-ttu-id="dbf1d-205">La primera parte de la sección de pancarta muestra el título con una regla horizontal debajo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-205">The first part of the banner section displays the title with a horizontal rule underneath it.</span></span> <span data-ttu-id="dbf1d-206">Las etiquetas de tabla se utilizan para controlar su posición.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-206">Table tags are used to control its position.</span></span> <span data-ttu-id="dbf1d-207">El atributo NoWrap está establecido para</span><span class="sxs-lookup"><span data-stu-id="dbf1d-207">The nowrap attribute is set for the</span></span> <TD> <span data-ttu-id="dbf1d-208">etiqueta para evitar el ajuste de palabras.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-208">tag to prevent word wrapping.</span></span> <span data-ttu-id="dbf1d-209">El sistema reemplazará% THISDIRNAME% por el nombre de la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-209">The system will replace %THISDIRNAME% with the name of the current folder.</span></span> <span data-ttu-id="dbf1d-210">Un objeto **WebViewFolderIcon** , con un identificador de "Icon" para simplificar, se carga para extraer y mostrar el icono de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-210">A **WebViewFolderIcon** object, with an identifier of "Icon" for simplicity, is then loaded to extract and display the folder's icon.</span></span>

<span data-ttu-id="dbf1d-211">La sección minibanner es similar al banner normal.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-211">The minibanner section is similar to the normal banner.</span></span> <span data-ttu-id="dbf1d-212">El formato del título se coloca ligeramente más alto y no tiene una regla.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-212">The format of the title is placed slightly higher and does not have a rule.</span></span> <span data-ttu-id="dbf1d-213">Dado que no hay ningún icono, el objeto **WebViewFolderIcon** no se carga.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-213">Because there is no icon, the **WebViewFolderIcon** object is not loaded.</span></span>


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a><span data-ttu-id="dbf1d-214">La región de información</span><span class="sxs-lookup"><span data-stu-id="dbf1d-214">The Info Region</span></span>

<span data-ttu-id="dbf1d-215">La parte de la vista Web situada debajo del banner se usa para presentar información detallada sobre el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-215">The portion of the Web view below the banner is used to present detailed information about the selected item.</span></span> <span data-ttu-id="dbf1d-216">Si no hay ningún elemento seleccionado, se muestra un mensaje predeterminado.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-216">If no item is selected, a default message is shown.</span></span> <span data-ttu-id="dbf1d-217">Dado que Generic. htt solo muestra un solo bloque de texto, esta sección es bastante sencilla.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-217">Because Generic.htt only displays a single block of text, this section is quite simple.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



<span data-ttu-id="dbf1d-218">La mayor parte del trabajo de recopilación de la información se controla mediante un [script de información de carpeta](#retrieving-and-displaying-folder-information) que se describe más adelante en el capítulo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-218">Most of the work of collecting the information is handled by a [folder information script](#retrieving-and-displaying-folder-information) that is discussed later in the chapter.</span></span> <span data-ttu-id="dbf1d-219">Muestra la información asignando el texto a [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="dbf1d-219">It displays the information by assigning the text to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

<span data-ttu-id="dbf1d-220">Puede personalizar fácilmente la presentación de la información modificando estos elementos o incluyendo otros adicionales.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-220">You can easily customize the information display by modifying these elements or including additional ones.</span></span> <span data-ttu-id="dbf1d-221">Se puede usar todo lo que se puede colocar en una página web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-221">Anything that you can put on a webpage can be used.</span></span> <span data-ttu-id="dbf1d-222">Por ejemplo, para mostrar un vínculo a su sitio web, puede Agregar un elemento delimitador después del bloque de texto en Generic. htt.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-222">For example, to display a link to your website, you can add an anchor element after the text block in Generic.htt.</span></span>


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
        <span>
        <p> Click on <a href="https://your.address"></a>
        </span>
</div>
                    
```



### <a name="the-filelist-region"></a><span data-ttu-id="dbf1d-223">La región FileList</span><span class="sxs-lookup"><span data-stu-id="dbf1d-223">The FileList Region</span></span>

<span data-ttu-id="dbf1d-224">Por último, Generic. htt carga un objeto [**WebViewFolderContents**](webviewfoldercontents.md) para la región FileList.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-224">Finally, Generic.htt loads a [**WebViewFolderContents**](webviewfoldercontents.md) object for the FileList region.</span></span> <span data-ttu-id="dbf1d-225">Dado que su identificador se establece en "FileList", se hará referencia a él como el objeto FileList de Now.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-225">Because its identifier is set to "FileList", it will be referred to as the FileList object from now on.</span></span>


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



<span data-ttu-id="dbf1d-226">El objeto FileList se encuentra en la mayoría de las vistas web y sirve para varios propósitos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-226">The FileList object is found in most Web views and serves several purposes.</span></span> <span data-ttu-id="dbf1d-227">FileList muestra la lista de elementos contenidos en la carpeta seleccionada con las mismas opciones y apariencia que la lista de archivos en estilo clásico.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-227">FileList displays the list of items contained by the selected folder with the same options and appearance as the file list in Classic style.</span></span> <span data-ttu-id="dbf1d-228">Cuando se selecciona un elemento, FileList notifica a la vista Web desencadenando un evento [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="dbf1d-228">When an item is selected, FileList notifies the Web view by firing a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="dbf1d-229">FileList también expone métodos y propiedades que se pueden utilizar para recuperar información sobre elementos individuales y controlar la posición y el tamaño de su área de presentación.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-229">FileList also exposes methods and properties that can be used to retrieve information about individual items and control the position and size of its display area.</span></span>

<span data-ttu-id="dbf1d-230">Aunque el objeto FileList es muy útil, solo devuelve información estándar del sistema de archivos, como el tamaño de archivo o los atributos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-230">Although the FileList object is very useful, it only returns standard file system information, such as file size or attributes.</span></span> <span data-ttu-id="dbf1d-231">Para recuperar otros tipos de información de una carpeta de Shell, tendrá que cargar y controlar los objetos adicionales.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-231">To retrieve other kinds of information from a Shell folder, you will have to load and handle additional objects.</span></span> <span data-ttu-id="dbf1d-232">Cualquier objeto que pueda hospedarse en una página web puede usarse con una vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-232">Any object that can be hosted by a webpage can be used with a Web view.</span></span>

### <a name="the-template-head"></a><span data-ttu-id="dbf1d-233">El encabezado de la plantilla</span><span class="sxs-lookup"><span data-stu-id="dbf1d-233">The Template Head</span></span>

<span data-ttu-id="dbf1d-234">El encabezado de la plantilla de vista Web contiene los scripts y las funciones que realizan la mayor parte del trabajo real.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-234">The head of the Web view template contains the scripts and functions that do most of the actual work.</span></span> <span data-ttu-id="dbf1d-235">Hay dos tareas esenciales que deben administrarse.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-235">There are two essential tasks that need to be handled.</span></span> <span data-ttu-id="dbf1d-236">Uno es el diseño de la presentación de la vista Web, que debe ajustarse para adaptarse a distintas regiones de presentación.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-236">One is the layout of the Web view display, which needs to be adjusted to accommodate different display regions.</span></span> <span data-ttu-id="dbf1d-237">El otro está recuperando y mostrando información de la carpeta cuando se selecciona un elemento.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-237">The other is retrieving and displaying information from the folder when an item is selected.</span></span> <span data-ttu-id="dbf1d-238">Al igual que con las hojas de estilos, es mejor incluir todos los scripts y las funciones en la plantilla en lugar de hacer referencia a ellos como archivos independientes.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-238">As with style sheets, it is better to include all scripts and functions in the template instead of referencing them as separate files.</span></span>

### <a name="controlling-the-web-view-layout"></a><span data-ttu-id="dbf1d-239">Controlar el diseño de la vista Web</span><span class="sxs-lookup"><span data-stu-id="dbf1d-239">Controlling the Web View Layout</span></span>

<span data-ttu-id="dbf1d-240">El área disponible para una vista Web depende del tamaño de la ventana de vista Web y de la parte de la barra del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-240">The area available for a Web view depends on the size of the Web view window and how much of it is taken up by the Windows Explorer bar.</span></span> <span data-ttu-id="dbf1d-241">Esta área cambiará siempre que se cambie el tamaño de la ventana o de la barra del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-241">This area will change anytime the window or Windows Explorer bar is resized.</span></span> <span data-ttu-id="dbf1d-242">Por lo tanto, el diseño debe coincidir con el área disponible cuando se carga una vista Web y cambiar adecuadamente cuando se cambia el tamaño.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-242">So the layout needs to be matched to the available area when a Web view is loaded and change appropriately when it is resized.</span></span> <span data-ttu-id="dbf1d-243">Gran parte del diseño se especifica en la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-243">Much of the layout is specified in the style sheet.</span></span> <span data-ttu-id="dbf1d-244">La región de información, por ejemplo, se define para ocupar el 30 por ciento más a la izquierda de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-244">The Info region, for example, is defined to occupy the leftmost 30 percent of the Web view.</span></span>


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



<span data-ttu-id="dbf1d-245">A medida que se cambia el tamaño de una vista Web, el ancho de la región de información cambiará para mantener ese porcentaje.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-245">As a Web view is resized, the width of the Info region will change to maintain that percentage.</span></span> <span data-ttu-id="dbf1d-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) administra los problemas de diseño que no se pueden controlar mediante una hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-246">[FixSize](#adjusting-the-layout-by-using-the-fixsize-function) manages the layout issues that can't be handled by a style sheet.</span></span>

### <a name="loading-and-initializing-the-web-view"></a><span data-ttu-id="dbf1d-247">Cargar e inicializar la vista Web</span><span class="sxs-lookup"><span data-stu-id="dbf1d-247">Loading and Initializing the Web View</span></span>

<span data-ttu-id="dbf1d-248">Cuando se carga una vista Web, el diseño debe ajustarse para ajustarse al área de presentación disponible.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-248">When a Web view is loaded, the layout needs to be adjusted to fit the available display area.</span></span> <span data-ttu-id="dbf1d-249">Dado que todavía no se ha seleccionado ningún elemento, las vistas Web suelen mostrar información predeterminada que se aplica a toda la carpeta.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-249">Because no item has been selected yet, Web views normally display some default information that applies to the whole folder.</span></span> <span data-ttu-id="dbf1d-250">Para controlar la inicialización, el</span><span class="sxs-lookup"><span data-stu-id="dbf1d-250">To handle initialization, the</span></span> <BODY> <span data-ttu-id="dbf1d-251">la etiqueta de Generic. htt detecta el evento [OnLoad](/previous-versions//ms531409(v=vs.85)) y llama a la función **init** .</span><span class="sxs-lookup"><span data-stu-id="dbf1d-251">tag for Generic.htt detects the [onload](/previous-versions//ms531409(v=vs.85)) event and calls the **Init** function.</span></span>


```
<body scroll=no onload="Init">
                    
```



<span data-ttu-id="dbf1d-252">**Init** es una sencilla función de JScript.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-252">**Init** is a simple JScript function.</span></span>


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



<span data-ttu-id="dbf1d-253">**Init** enlaza [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) al evento [window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) para que se llame a este método cada vez que cambie el área de visualización de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-253">**Init** binds [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) to the [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) event so that it will be called whenever the Web view display area changes.</span></span> <span data-ttu-id="dbf1d-254">A continuación, ejecuta FixSize para establecer el diseño inicial y asigna el \_ \_ texto de introducción L a la región de información.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-254">It then runs FixSize to set the initial layout and assigns L\_Intro\_Text to the Info region.</span></span> <span data-ttu-id="dbf1d-255">L \_ \_ el texto de introducción es un bloque de texto introductorio que se define en la sección hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-255">L\_Intro\_Text is a block of introductory text that is defined in the style sheet section.</span></span>


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a><span data-ttu-id="dbf1d-256">Ajustar el diseño mediante la función FixSize</span><span class="sxs-lookup"><span data-stu-id="dbf1d-256">Adjusting the Layout by using the FixSize function</span></span>

<span data-ttu-id="dbf1d-257">La función [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) se usa para especificar varios aspectos del diseño que no se pueden controlar mediante la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-257">The [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) function is used to specify several aspects of the layout that can't be handled by the style sheet.</span></span>

<span data-ttu-id="dbf1d-258">Se pueden usar dos banners posibles, en función del alto de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-258">There are two possible banners that can be used, depending on the height of the Web view.</span></span>


```
if (200 > document.body.clientHeight) {
    //A short window. Use the minibanner.
    document.all.Banner.style.visibility = "hidden";
    document.all.MiniBanner.style.visibility = "visible";
    document.all.FileList.style.top = 32;
    document.all.Info.style.top = 32;
}
else {
    //A normal window. Use the normal banner.
    document.all.Banner.style.visibility = "visible";
    document.all.MiniBanner.style.visibility = "hidden";
    document.all.FileList.style.top = (document.all.Banner.offsetHeight - 32) + "px";
    document.all.Info.style.top = (document.all.Banner.offsetHeight) + "px";
    document.all.Rule.style.width = (document.body.clientWidth > 84 ?                                    document.body.clientWidth - 84 : 0) + "px";      
}
                    
```



<span data-ttu-id="dbf1d-259">Generic. htt usa un alto de 200 píxeles como la línea de división entre normal y minibanners.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-259">Generic.htt uses a height of 200 pixels as the dividing line between normal and minibanners.</span></span> <span data-ttu-id="dbf1d-260">Establece el estilo del banner seleccionado en visible y el otro en oculto.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-260">It sets the style of the selected banner to visible and the other to hidden.</span></span> <span data-ttu-id="dbf1d-261">También establece varias propiedades de diseño para las regiones info y FileList de modo que se ajusten correctamente a la pancarta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-261">It also sets several layout properties for the Info and FileList regions so that they fit properly with the selected banner.</span></span>

<span data-ttu-id="dbf1d-262">Si una vista Web es demasiado estrecha, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) usa el ancho completo del área de presentación de la pantalla de FileList.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-262">If a Web view becomes too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) uses the full width of the display area for the FileList display.</span></span>


```
if (400 > document.body.clientWidth) {
    //A narrow window. Hide the Info region, and expand the file list region.
    document.all.Info.style.visibility = "hidden";
    document.all.FileList.style.pixelLeft = 0;
    document.all.FileList.style.pixelTop = document.all.Info.style.pixelTop;
}

else {
    //Normal width.
    document.all.Info.style.visibility = "visible";
    document.all.FileList.style.pixelLeft = document.all.Info.style.pixelWidth;
}
                    
```



<span data-ttu-id="dbf1d-263">Generic. htt usa 400 píxeles como línea divisoria entre las pantallas estrechas y anchas.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-263">Generic.htt uses 400 pixels as the dividing line between narrow and wide displays.</span></span> <span data-ttu-id="dbf1d-264">Si la vista Web es demasiado estrecha, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) oculta la región de información y modifica la propiedad FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) para que ocupe toda la región debajo del banner.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-264">If the Web view is too narrow, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) hides the Info region and modifies the FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) property so that it fills the entire region below the banner.</span></span>

<span data-ttu-id="dbf1d-265">Las pocas líneas finales de [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ajustan varias propiedades de diseño en función de los resultados del código anterior.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-265">The final few lines of [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) adjust several layout properties based on the results of the preceding code.</span></span> <span data-ttu-id="dbf1d-266">El ancho de la región FileList se ajusta para que rellene exactamente la parte de la vista Web no ocupada por la región info.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-266">The width of the FileList region is adjusted so that it exactly fills the portion of the Web view not occupied by the Info region.</span></span> <span data-ttu-id="dbf1d-267">El alto de la región de información se ajusta para ajustarse al banner y a la parte inferior de la vista Web.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-267">The height of the Info region is sized to fit between the banner and the bottom of the Web view.</span></span>


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a><span data-ttu-id="dbf1d-268">Recuperar y Mostrar información de carpetas</span><span class="sxs-lookup"><span data-stu-id="dbf1d-268">Retrieving and Displaying Folder Information</span></span>

<span data-ttu-id="dbf1d-269">Cuando un usuario selecciona un elemento, el objeto FileList activa un evento [SelectionChanged](#retrieving-and-displaying-folder-information) .</span><span class="sxs-lookup"><span data-stu-id="dbf1d-269">When a user selects an item, the FileList object fires a [SelectionChanged](#retrieving-and-displaying-folder-information) event.</span></span> <span data-ttu-id="dbf1d-270">Este evento se controla mediante un script de JScript.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-270">This event is handled by a JScript script.</span></span> <span data-ttu-id="dbf1d-271">Para simplificar, el script que se encuentra en Generic. htt supone que solo se puede seleccionar un elemento cada vez.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-271">For simplicity, the script found in Generic.htt assumes that only one item can be selected at a time.</span></span>


```
<script language="JavaScript" for="FileList" event="SelectionChanged">
    // Updates the TextBlock region when an item is selected.
    var data;
    var text;

    // Name
    text = "<b>" + FileList.FocusedItem.Name + "</b>";

    // Comment
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 3);
    if (data)
        text += "<br>" + data;

    // Documents
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 1);
    if (data)
        text += "<br><br>" + FileList.Folder.GetDetailsOf(null, 1) + ": " + data;

    // Status
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, 2);
    if (data)
        text += "<br><br><b><font color=red>" + data + "</font></b>";

    // Tip 
    data = FileList.Folder.GetDetailsOf(FileList.FocusedItem, -1);
    if (data != "" && data != FileList.FocusedItem.Name)
        text += "<br><br>" + data;

    TextBlock.innerHTML = text;
</script>
                    
```



<span data-ttu-id="dbf1d-272">El script usa dos propiedades FileList, [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)y [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) para obtener información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-272">The script uses two FileList properties, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)and [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) to obtain information about the item.</span></span> <span data-ttu-id="dbf1d-273">**FileList. FocusedItem** identifica el elemento seleccionado, con el nombre del elemento dado por **FileList.FocusedItem.Name**.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-273">**FileList.FocusedItem** identifies the selected item, with the item's name given by **FileList.FocusedItem.Name**.</span></span> <span data-ttu-id="dbf1d-274">**FileList. Folder** es realmente un puntero a un objeto de [**carpeta**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf1d-274">**FileList.Folder** is actually a pointer to a [**Folder**](../shell/folder.md) object.</span></span> <span data-ttu-id="dbf1d-275">El método [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) del objeto de carpeta se usa para recuperar la información restante sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-275">The Folder object's [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) method is used to retrieve the remaining information about the item.</span></span>

<span data-ttu-id="dbf1d-276">Toda la información se concatena en una sola cadena de texto, separadas por</span><span class="sxs-lookup"><span data-stu-id="dbf1d-276">All the information is concatenated into a single text string, separated by</span></span> <BR> <span data-ttu-id="dbf1d-277">Etiquetas para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-277">tags for readability.</span></span> <span data-ttu-id="dbf1d-278">Después, se muestra el texto asignándole a [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="dbf1d-278">The text is then displayed by assigning it to [TextBlock.innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="dbf1d-279">Resumen</span><span class="sxs-lookup"><span data-stu-id="dbf1d-279">Summary</span></span>

<span data-ttu-id="dbf1d-280">En este capítulo se describen algunas de las técnicas que puede usar para personalizar el modo en que el explorador de Windows muestra información acerca de las carpetas de Shell.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-280">This chapter outlines some of the techniques you can use to customize the way the Windows Explorer displays information about Shell folders.</span></span> <span data-ttu-id="dbf1d-281">La creación de un archivo de Desktop.ini permite realizar algunas personalizaciones sencillas, como mostrar un icono personalizado en lugar del icono de carpeta estándar.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-281">Creating a Desktop.ini file allows you to do some simple customization, such as displaying a custom icon in place of the standard folder icon.</span></span> <span data-ttu-id="dbf1d-282">Cuando una carpeta aparece en una vista Web, el diseño y la presentación se controlan mediante una plantilla basada en HTML que determina qué información se muestra y cómo.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-282">When a folder appears in a Web view, its layout and display are controlled by an HTML-based template that determines what information is displayed and how.</span></span> <span data-ttu-id="dbf1d-283">Puede usar un alto grado de control sobre la vista Web de una carpeta mediante el uso de las técnicas estándar de HTML, DHTML y scripting para crear una plantilla personalizada.</span><span class="sxs-lookup"><span data-stu-id="dbf1d-283">You can exercise a high degree of control over a folder's Web view by using standard HTML, DHTML, and scripting techniques to create a custom template.</span></span>

 

 