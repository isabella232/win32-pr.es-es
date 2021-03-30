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
# <a name="customizing-a-folders-web-view"></a>Personalización de la vista Web de una carpeta

\[Esta característica solo se admite en Windows XP o versiones anteriores. \]

Una vista Web es una forma eficaz y flexible de usar el explorador de Windows para mostrar información sobre el contenido de una carpeta de Shell.

-   [Introducción](#introduction)
-   [Usar la plantilla Vista Web](#using-the-web-view-template)
    -   [El cuerpo de la plantilla](#the-template-body)
    -   [El encabezado de la plantilla](#the-template-head)
-   [Resumen](#summary)

## <a name="introduction"></a>Introducción

Windows ofrece a los usuarios dos maneras principales de ver y navegar por el espacio de nombres del shell. Lo más familiar, el estilo clásico, es similar al conocido administrador de archivos de Windows. En el panel derecho se muestra el contenido de la carpeta actualmente seleccionada en uno de los cinco formatos siguientes: iconos grandes, iconos pequeños, lista, detalles y miniatura. La diferencia principal del administrador de archivos de Windows es el panel izquierdo, que es muy similar a la barra del explorador de Windows Internet Explorer. Se puede cambiar de tamaño o quitar, y puede mostrar varios paneles además del árbol del sistema de archivos conocido, como un panel de búsqueda.

> [!Note]  
> La información de este documento no se aplica a Windows XP, las técnicas descritas solo se aplican a versiones anteriores de Windows.

 

En la ilustración siguiente se muestra la carpeta Impresoras en estilo clásico.

![estilo clásico de la carpeta de impresoras.](images/webview1.png)

El estilo clásico funciona razonablemente bien para carpetas y archivos normales del sistema de archivos. Sin embargo, con la introducción de Windows 95, el sistema de archivos ha evolucionado en el espacio de nombres. El espacio de nombres permite la creación de *carpetas virtuales*, como las impresoras o el entorno de red, que pueden representar tipos de información muy diferentes de los de una carpeta de sistema de archivos normal.

El estilo Web, también conocido como vista Web, ofrece una manera más flexible y eficaz de presentar información que el estilo clásico. En una vista Web, el usuario básicamente ve y navega por el espacio de nombres mediante Internet Explorer. El diseño básico de una vista Web es similar al estilo clásico. La barra del explorador no cambia. Sin embargo, la región ocupada por la lista de archivos se convierte en un área de visualización de uso general que es realmente una página web. Una vista Web todavía se usa para mostrar información sobre el contenido de una carpeta, pero hay pocas restricciones en cuanto a la información que se muestra o cómo. Cada carpeta puede tener su propia vista Web, personalizada para adaptarse a sus características concretas.

En la ilustración siguiente se muestra una vista Web de la carpeta Impresoras (mostrada anteriormente en estilo clásico).

![Vista Web predeterminada de la carpeta de impresoras.](images/webview2.png)

Al igual que las páginas web convencionales, las vistas Web se controlan mediante una plantilla basada en HTML. La creación de una plantilla de vista Web es prácticamente idéntica a la creación de una página web y proporciona el mismo grado de flexibilidad en el contenido y el diseño de la información. Las plantillas de vista Web pueden usar HTML dinámico (DHTML) y scripting para responder a eventos, como un usuario que hace clic en un elemento. También pueden hospedar objetos que les permiten obtener y Mostrar información de la carpeta o de su contenido.

El usuario puede elegir una vista Web iniciando el explorador de Windows, haciendo clic en **Opciones de carpeta** en el menú **Ver** y seleccionando esta opción: **Habilitar contenido web en carpetas**. Sin embargo, el usuario también puede iniciar Internet Explorer y señalar el explorador en el sistema de archivos; para ello, haga clic en el menú **Ver** , seleccione **barra del explorador** y haga clic en **carpetas**. En una vista Web, no hay prácticamente ninguna diferencia entre Internet Explorer y el explorador de Windows.

En el lado izquierdo del panel derecho, la vista Web impresoras muestra un banner con el nombre y el icono de la carpeta, seguido de un bloque de información sobre la carpeta. La lista de archivos habitual ocupa el lado derecho de la página.

Cuando un usuario hace clic en un elemento, en el bloque de información aparece información detallada sobre el elemento. La vista Web de impresoras muestra realmente la misma información que está disponible en el estilo clásico, pero lo hace en un formato más utilizable. Sin embargo, una vista Web no es simplemente una manera diferente de Mostrar información de estilo clásico. Por ejemplo, se puede mostrar un vínculo a un sitio web útil debajo del bloque de información, una característica que no está disponible en el estilo clásico. Si el usuario hace clic en el vínculo, se mostrará el sitio.

La vista Web de impresoras mostrada en la ilustración anterior es similar al estilo clásico, porque la plantilla de vista Web subyacente (un archivo. htt) se escribió de este modo. La lista de archivos, por ejemplo, no se genera directamente en la plantilla de vista Web. Se crea y muestra mediante un objeto [**WebViewFolderContents**](webviewfoldercontents.md) hospedado por la plantilla de vista Web. Los métodos y las propiedades del objeto permiten a la vista Web controlar su diseño y obtener información sobre elementos concretos. El contenido y el diseño del encabezado y el bloque de información se especifican en la plantilla de vista Web.

Dado que una vista Web es compatible con DHTML, la plantilla también se puede utilizar para controlar la interacción del usuario. Por ejemplo, cuando un usuario hace clic en uno de los iconos de la impresora, el objeto **WebViewFolderIcon** activa un evento [**SelectionChanged**](/windows/desktop/shell/application-support-bumper) . La plantilla usa un controlador de eventos DHTML escrito en el script para recuperar la información solicitada y mostrarla en el bloque de información.

Este sencillo ejemplo de la carpeta de impresoras no es, la única manera de usar una vista Web. Si escribe su propia plantilla y, si es necesario, los objetos, puede usar una vista Web para mostrar información e interactuar con el usuario de la forma que más le convenga. Tenga en cuenta que, en la actualidad, las plantillas de vista web solo muestran carpetas virtuales definidas por el sistema. Aunque los desarrolladores pueden crear una carpeta virtual mediante la implementación de una extensión de espacio de nombres, deben usar las técnicas descritas en [extensiones de espacio de nombres](/windows/desktop/shell/nse-works) para mostrarla.

## <a name="using-the-web-view-template"></a>Usar la plantilla Vista Web

La forma en que se muestran los datos en una vista Web puede personalizarse de una manera limitada modificando el archivo de Desktop.ini de una carpeta. Consulte [Personalización de carpetas con Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) para obtener más información. Una manera mucho más flexible y eficaz de personalizar una vista Web es crear una plantilla de vista web personalizada.

La plantilla Vista Web controla lo que se muestra en una vista Web y cómo. Utiliza las técnicas estándar de HTML, DHTML y scripting para obtener y Mostrar información e interactuar con el usuario. En esta sección se describe cómo crear una vista Web mediante el examen de una plantilla simple: Generic. htt.


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



Una manera sencilla de crear su propia plantilla de vista Web es usar Generic. htt y modificarla. Dado que es bastante limitado, también debe examinar otros ejemplos más complejos para ver ideas adicionales. Puede encontrarlos buscando en el sistema la extensión. htt usada por todas las plantillas de vista Web. Si desea crear una plantilla personalizada para una carpeta, debe comenzar con la plantilla default. htt, que normalmente se almacena en C: \\ WinNT \\ Web o c: \\ Windows \\ Web. Tenga en cuenta que estos archivos se definen como ocultos, por lo que es posible que tenga que modificar la configuración del explorador de Windows para verlos. Una vez creado un archivo. htt, debe marcarse como de solo lectura y estar oculto.

Las plantillas de vista web usan la extensión. htt porque difieren ligeramente de los documentos convencionales. htm. La diferencia principal son varias variables especiales en los archivos. htt que el sistema reemplaza con los valores de espacio de nombres actuales. Las variables% THISDIR% y% THISDIRPATH% representan el nombre y la ruta de acceso de la carpeta actualmente seleccionada. La variable% TEMPLATEDIR% representa la carpeta donde se almacenan las hojas de estilos de vista Web.

Al igual que la mayoría de las plantillas HTML, los archivos. htt tienen dos partes básicas: un cuerpo y un encabezado. El cuerpo de la plantilla controla el diseño básico de la vista Web y carga los objetos utilizados para comunicarse con el espacio de nombres y Mostrar información. El encabezado contiene scripts y funciones que realizan tareas como controlar el cambio de tamaño y obtener información de la carpeta. La mayoría de las plantillas, incluido Generic. htt, también incluyen una hoja de estilos. En general, es mejor incluir la información de la hoja de estilos en la plantilla. Es posible que las hojas de estilos independientes no funcionen correctamente cuando se utiliza una vista Web con espacios de nombres remotos.

### <a name="the-template-body"></a>El cuerpo de la plantilla

El cuerpo de la plantilla especifica lo que presentará una vista Web. También es donde se cargan los objetos que se usan para mostrar información y comunicarse con las carpetas de espacio de nombres. El diseño definido por Generic. htt es similar al que se muestra en la ilustración de la sección anterior. Hay tres regiones para mostrar: el titular y el bloque de información en el lado izquierdo de la vista, y la lista de archivos a la derecha.

Todas las regiones son identificadores asignados que van a usar la hoja de estilos y DHTML. Como se describe en la sección siguiente, hay dos banners posibles, con identificadores de "Banner" y "MiniBanner". El identificador de la región del bloque de información es "info". El identificador del objeto de la lista de archivos es "FileList". Los detalles del [diseño](#controlling-the-web-view-layout) de la región se controlan mediante la hoja de estilos y una función de Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), que se describe más adelante en el capítulo.

### <a name="the-banner-region"></a>La región del banner

El banner se encuentra en la parte superior de la pantalla, en la esquina superior izquierda de la vista Web. El banner normal muestra el nombre y el icono de la carpeta cuyo contenido se muestra en la lista de archivos de la derecha. Sin embargo, si la ventana es demasiado corta, puede que no haya espacio debajo del icono para mostrar la información. Por esta razón, Generic. htt también define un minibanner que solo muestra el nombre de la carpeta. Ambos banners se definen inicialmente como ocultos. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) elige cuál Mostrar y lo establece en "visible".

El banner normal de Generic. htt se define mediante:


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



La primera parte de la sección de pancarta muestra el título con una regla horizontal debajo. Las etiquetas de tabla se utilizan para controlar su posición. El atributo NoWrap está establecido para <TD> etiqueta para evitar el ajuste de palabras. El sistema reemplazará% THISDIRNAME% por el nombre de la carpeta actual. Un objeto **WebViewFolderIcon** , con un identificador de "Icon" para simplificar, se carga para extraer y mostrar el icono de la carpeta.

La sección minibanner es similar al banner normal. El formato del título se coloca ligeramente más alto y no tiene una regla. Dado que no hay ningún icono, el objeto **WebViewFolderIcon** no se carga.


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>La región de información

La parte de la vista Web situada debajo del banner se usa para presentar información detallada sobre el elemento seleccionado. Si no hay ningún elemento seleccionado, se muestra un mensaje predeterminado. Dado que Generic. htt solo muestra un solo bloque de texto, esta sección es bastante sencilla.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



La mayor parte del trabajo de recopilación de la información se controla mediante un [script de información de carpeta](#retrieving-and-displaying-folder-information) que se describe más adelante en el capítulo. Muestra la información asignando el texto a [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

Puede personalizar fácilmente la presentación de la información modificando estos elementos o incluyendo otros adicionales. Se puede usar todo lo que se puede colocar en una página web. Por ejemplo, para mostrar un vínculo a su sitio web, puede Agregar un elemento delimitador después del bloque de texto en Generic. htt.


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



### <a name="the-filelist-region"></a>La región FileList

Por último, Generic. htt carga un objeto [**WebViewFolderContents**](webviewfoldercontents.md) para la región FileList. Dado que su identificador se establece en "FileList", se hará referencia a él como el objeto FileList de Now.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



El objeto FileList se encuentra en la mayoría de las vistas web y sirve para varios propósitos. FileList muestra la lista de elementos contenidos en la carpeta seleccionada con las mismas opciones y apariencia que la lista de archivos en estilo clásico. Cuando se selecciona un elemento, FileList notifica a la vista Web desencadenando un evento [SelectionChanged](#retrieving-and-displaying-folder-information) . FileList también expone métodos y propiedades que se pueden utilizar para recuperar información sobre elementos individuales y controlar la posición y el tamaño de su área de presentación.

Aunque el objeto FileList es muy útil, solo devuelve información estándar del sistema de archivos, como el tamaño de archivo o los atributos. Para recuperar otros tipos de información de una carpeta de Shell, tendrá que cargar y controlar los objetos adicionales. Cualquier objeto que pueda hospedarse en una página web puede usarse con una vista Web.

### <a name="the-template-head"></a>El encabezado de la plantilla

El encabezado de la plantilla de vista Web contiene los scripts y las funciones que realizan la mayor parte del trabajo real. Hay dos tareas esenciales que deben administrarse. Uno es el diseño de la presentación de la vista Web, que debe ajustarse para adaptarse a distintas regiones de presentación. El otro está recuperando y mostrando información de la carpeta cuando se selecciona un elemento. Al igual que con las hojas de estilos, es mejor incluir todos los scripts y las funciones en la plantilla en lugar de hacer referencia a ellos como archivos independientes.

### <a name="controlling-the-web-view-layout"></a>Controlar el diseño de la vista Web

El área disponible para una vista Web depende del tamaño de la ventana de vista Web y de la parte de la barra del explorador de Windows. Esta área cambiará siempre que se cambie el tamaño de la ventana o de la barra del explorador de Windows. Por lo tanto, el diseño debe coincidir con el área disponible cuando se carga una vista Web y cambiar adecuadamente cuando se cambia el tamaño. Gran parte del diseño se especifica en la hoja de estilos. La región de información, por ejemplo, se define para ocupar el 30 por ciento más a la izquierda de la vista Web.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



A medida que se cambia el tamaño de una vista Web, el ancho de la región de información cambiará para mantener ese porcentaje. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) administra los problemas de diseño que no se pueden controlar mediante una hoja de estilos.

### <a name="loading-and-initializing-the-web-view"></a>Cargar e inicializar la vista Web

Cuando se carga una vista Web, el diseño debe ajustarse para ajustarse al área de presentación disponible. Dado que todavía no se ha seleccionado ningún elemento, las vistas Web suelen mostrar información predeterminada que se aplica a toda la carpeta. Para controlar la inicialización, el <BODY> la etiqueta de Generic. htt detecta el evento [OnLoad](/previous-versions//ms531409(v=vs.85)) y llama a la función **init** .


```
<body scroll=no onload="Init">
                    
```



**Init** es una sencilla función de JScript.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** enlaza [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) al evento [window. OnResize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) para que se llame a este método cada vez que cambie el área de visualización de la vista Web. A continuación, ejecuta FixSize para establecer el diseño inicial y asigna el \_ \_ texto de introducción L a la región de información. L \_ \_ el texto de introducción es un bloque de texto introductorio que se define en la sección hoja de estilos.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Ajustar el diseño mediante la función FixSize

La función [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) se usa para especificar varios aspectos del diseño que no se pueden controlar mediante la hoja de estilos.

Se pueden usar dos banners posibles, en función del alto de la vista Web.


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



Generic. htt usa un alto de 200 píxeles como la línea de división entre normal y minibanners. Establece el estilo del banner seleccionado en visible y el otro en oculto. También establece varias propiedades de diseño para las regiones info y FileList de modo que se ajusten correctamente a la pancarta seleccionada.

Si una vista Web es demasiado estrecha, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) usa el ancho completo del área de presentación de la pantalla de FileList.


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



Generic. htt usa 400 píxeles como línea divisoria entre las pantallas estrechas y anchas. Si la vista Web es demasiado estrecha, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) oculta la región de información y modifica la propiedad FileList [pixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) para que ocupe toda la región debajo del banner.

Las pocas líneas finales de [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) ajustan varias propiedades de diseño en función de los resultados del código anterior. El ancho de la región FileList se ajusta para que rellene exactamente la parte de la vista Web no ocupada por la región info. El alto de la región de información se ajusta para ajustarse al banner y a la parte inferior de la vista Web.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Recuperar y Mostrar información de carpetas

Cuando un usuario selecciona un elemento, el objeto FileList activa un evento [SelectionChanged](#retrieving-and-displaying-folder-information) . Este evento se controla mediante un script de JScript. Para simplificar, el script que se encuentra en Generic. htt supone que solo se puede seleccionar un elemento cada vez.


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



El script usa dos propiedades FileList, [**FileList. FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)y [**FileList. Folder**](/windows/desktop/shell/shellfolderview-folder) para obtener información sobre el elemento. **FileList. FocusedItem** identifica el elemento seleccionado, con el nombre del elemento dado por **FileList.FocusedItem.Name**. **FileList. Folder** es realmente un puntero a un objeto de [**carpeta**](../shell/folder.md) . El método [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) del objeto de carpeta se usa para recuperar la información restante sobre el elemento.

Toda la información se concatena en una sola cadena de texto, separadas por <BR> Etiquetas para mejorar la legibilidad. Después, se muestra el texto asignándole a [TextBlock. innerHTML](https://msdn.microsoft.com/library/ms533897(VS.85).aspx).

## <a name="summary"></a>Resumen

En este capítulo se describen algunas de las técnicas que puede usar para personalizar el modo en que el explorador de Windows muestra información acerca de las carpetas de Shell. La creación de un archivo de Desktop.ini permite realizar algunas personalizaciones sencillas, como mostrar un icono personalizado en lugar del icono de carpeta estándar. Cuando una carpeta aparece en una vista Web, el diseño y la presentación se controlan mediante una plantilla basada en HTML que determina qué información se muestra y cómo. Puede usar un alto grado de control sobre la vista Web de una carpeta mediante el uso de las técnicas estándar de HTML, DHTML y scripting para crear una plantilla personalizada.

 

 