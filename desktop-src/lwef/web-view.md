---
title: Personalizar la vista web de una carpeta
description: Una vista web es una manera eficaz y flexible de usar Windows Explorer para mostrar información sobre el contenido de una carpeta de Shell.
ms.assetid: a894df21-bcc6-4760-b7d7-9bf95a0dba7f
keywords:
- Vistas web
- Estilo clásico
- Estilo web
- titulares
- Región FileList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85478bd42737f0a240b356bb6b3b73e838a8ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569469"
---
# <a name="customizing-a-folders-web-view"></a>Personalizar la vista web de una carpeta

\[Esta característica solo se admite en Windows XP o versiones anteriores. \]

Una vista web es una manera eficaz y flexible de usar Windows Explorer para mostrar información sobre el contenido de una carpeta de Shell.

-   [Introducción](#introduction)
-   [Uso de la plantilla de vista web](#using-the-web-view-template)
    -   [Cuerpo de la plantilla](#the-template-body)
    -   [El jefe de plantilla](#the-template-head)
-   [Resumen](#summary)

## <a name="introduction"></a>Introducción

Windows ofrece a los usuarios dos formas principales de ver y navegar por el espacio de nombres de Shell. El más conocido de ellos, el estilo clásico, es similar al conocido administrador de Windows archivos. En el panel derecho se muestra el contenido de la carpeta seleccionada actualmente en uno de los cinco formatos: Icono grande, Icono pequeño, Lista, Detalles y Miniatura. La principal diferencia con Windows administrador de archivos es el panel izquierdo, que es muy similar a la barra explorador de Windows Internet Explorer. Se puede cambiar de tamaño o quitarse, y puede mostrar varios paneles además del conocido árbol del sistema de archivos, como un panel de búsqueda.

> [!Note]  
> La información de este documento no se aplica a Windows XP, las técnicas analizadas solo se aplican a versiones anteriores de Windows.

 

En la ilustración siguiente se muestra la carpeta Impresoras en estilo clásico.

![estilo clásico de la carpeta de impresoras.](images/webview1.png)

El estilo clásico funciona razonablemente bien para archivos y carpetas normales del sistema de archivos. Sin embargo, con la introducción de Windows 95, el sistema de archivos ha evolucionado al espacio de nombres . El espacio de nombres permite la creación de carpetas *virtuales,* como Impresoras o Vecinos de red, que pueden representar tipos de información muy diferentes a una carpeta normal del sistema de archivos.

El estilo web, también conocido como vista web, ofrece una manera más flexible y eficaz de presentar información que el estilo clásico. En una vista web, el usuario básicamente ve y navega por el espacio de nombres mediante Internet Explorer. El diseño básico de una vista web es similar al estilo clásico. La barra explorador no ha cambiado. Sin embargo, la región ocupada por la lista de archivos se convierte en un área de presentación de uso general que es realmente una página web. Una vista web se sigue utilizando para mostrar información sobre el contenido de una carpeta, pero hay algunas restricciones sobre qué información se muestra o cómo. Cada carpeta puede tener su propia vista web, personalizada para adaptarse a sus características concretas.

En la ilustración siguiente se muestra una vista web de la carpeta Impresoras (mostrada anteriormente en el estilo clásico).

![vista web predeterminada de la carpeta de impresoras.](images/webview2.png)

Al igual que las páginas web convencionales, las vistas web se controlan mediante una plantilla basada en HTML. La creación de una plantilla de vista web es casi idéntica a la creación de una página web y proporciona el mismo grado de flexibilidad en el contenido y el diseño de la información. Las plantillas de vista web pueden usar HTML dinámico (DHTML) y scripting para responder a eventos, como un usuario que hace clic en un elemento. También pueden hospedar objetos que les permiten obtener y mostrar información de la carpeta o su contenido.

El usuario puede elegir una vista web iniciando  Windows Explorer, haciendo clic en Opciones de carpeta en el menú Ver y seleccionando esta opción: Habilitar contenido web en **carpetas**.  Sin embargo, el usuario también puede iniciar Internet Explorer apuntar el explorador  al sistema de archivos haciendo clic en el menú Ver, apuntando a barra del explorador y haciendo clic en **Carpetas.** En una vista web, prácticamente no hay ninguna diferencia entre Internet Explorer y Windows Explorer.

En el lado izquierdo del panel derecho, la vista Web impresoras muestra un banner con el nombre y el icono de la carpeta, seguido de un bloque de información sobre la carpeta. La lista de archivos habitual ocupa el lado derecho de la página.

Cuando un usuario hace clic en un elemento, aparece información detallada sobre el elemento en el bloque de información. La vista web impresoras muestra realmente la misma información que está disponible en el estilo clásico, pero lo hace en un formato más utilizable. Sin embargo, una vista web no es simplemente una manera diferente de mostrar información de estilo clásico. Por ejemplo, se puede mostrar un vínculo a un sitio web útil debajo del bloque de información, una característica que no está disponible en el estilo clásico. Si el usuario hace clic en el vínculo, se mostrará el sitio.

La vista Web impresoras que se muestra en la ilustración anterior es similar al estilo clásico, porque la plantilla de vista web subyacente (un archivo .htt) se escribió de esa manera. La lista de archivos, por ejemplo, no se genera directamente mediante la plantilla de vista web. Se crea y muestra mediante un [**objeto WebViewFolderContents**](webviewfoldercontents.md) hospedado por la plantilla de vista web. Los métodos y propiedades del objeto permiten a la vista web controlar su diseño y obtener información sobre elementos concretos. El contenido y el diseño del banner y el bloque de información se especifican en la plantilla de vista web.

Dado que una vista web admite DHTML, la plantilla también se puede usar para controlar la interacción del usuario. Por ejemplo, cuando un usuario hace clic en uno de los iconos de impresora, el objeto **WebViewFolderIcon** produce un [**evento SelectionChanged.**](/windows/desktop/shell/application-support-bumper) La plantilla usa un controlador de eventos DHTML escrito en script para recuperar la información solicitada y mostrarla en el bloque de información.

Este sencillo ejemplo de la carpeta Impresoras no es la única manera de usar una vista web. Al escribir su propia plantilla y, si es necesario, objetos, puede usar una vista web para mostrar información e interactuar con el usuario de la manera que le sea más eficaz. Tenga en cuenta que, en la actualidad, las plantillas de vista web solo muestran carpetas virtuales definidas por el sistema. Aunque los desarrolladores pueden crear una carpeta virtual implementando una extensión de espacio de nombres, deben usar las técnicas [descritas](/windows/desktop/shell/nse-works) en Extensiones de espacio de nombres para mostrarla.

## <a name="using-the-web-view-template"></a>Uso de la plantilla de vista web

La forma en que se muestran los datos en una vista web se puede personalizar de forma limitada modificando el archivo de Desktop.ini carpeta. Consulte [Personalización de carpetas con Desktop.ini](/windows/desktop/shell/how-to-customize-folders-with-desktop-ini) para obtener más información. Una manera mucho más flexible y eficaz de personalizar una vista web es crear una plantilla de vista web personalizada.

La plantilla vista web controla lo que se muestra en una vista web y cómo. Usa html estándar, DHTML y técnicas de scripting para obtener y mostrar información e interactuar con el usuario. En esta sección se describe cómo crear una vista web mediante el examen de una plantilla simple: Generic.htt.


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



Una manera sencilla de crear su propia plantilla de vista web es tomar Generic.htt y modificarla. Dado que es bastante limitado, también debe ver otros ejemplos más complejos para obtener ideas adicionales. Para encontrarlos, busque en el sistema la extensión .htt que usan todas las plantillas de vista web. Si desea crear una plantilla personalizada para una carpeta, debe empezar con la plantilla Folder.htt predeterminada, que normalmente se almacena en C: Winnt Web o \\ \\ C: \\ Windows \\ Web. Tenga en cuenta que estos archivos se definen como ocultos, por lo que es posible que tenga que modificar la configuración Windows Explorer para verlos. Una vez creado un archivo .htt, debe marcarse como de solo lectura y oculto.

Las plantillas de vista web usan la extensión .htt porque difieren ligeramente de los documentos .htm convencionales. La principal diferencia son varias variables especiales en los archivos .htt que el sistema reemplaza por los valores de espacio de nombres actuales. Las variables %THISDIR% y %THISDIRPATH% representan el nombre y la ruta de acceso de la carpeta seleccionada actualmente. La variable %TEMPLATEDIR% representa la carpeta donde se almacenan las hojas de estilos de vista web.

Al igual que la mayoría de las plantillas HTML, los archivos .htt tienen dos partes básicas: un cuerpo y una cabeza. El cuerpo de la plantilla controla el diseño básico de la vista web y carga los objetos usados para comunicarse con el espacio de nombres y mostrar información. El head contiene scripts y funciones que hacen tareas como controlar el tamaño y obtener información de la carpeta. La mayoría de las plantillas, incluido Generic.htt, también incluyen una hoja de estilos. En general, es mejor incluir la información de la hoja de estilos en la plantilla. Es posible que hojas de estilos independientes no funcionen correctamente cuando se usa una vista web con espacios de nombres remotos.

### <a name="the-template-body"></a>Cuerpo de la plantilla

El cuerpo de la plantilla especifica lo que presentará una vista web. También es donde se cargan los objetos usados para mostrar información y comunicarse con carpetas de espacio de nombres. El diseño definido por Generic.htt es similar al que se muestra en la ilustración de la sección anterior. Hay tres regiones para mostrar: el banner y el bloque de información en el lado izquierdo de la vista y la lista de archivos a la derecha.

Todas las regiones son identificadores asignados que la hoja de estilos y DHTML usarán. Como se describe en la sección siguiente, hay dos posibles banners, con identificadores de "Banner" y "MiniBanner". El identificador de la región del bloque de información es "Info". El identificador del objeto de lista de archivos es "FileList". Los detalles del diseño [](#controlling-the-web-view-layout) de la región se controlan mediante la hoja de estilos y una función de Microsoft JScript, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function), que se describe más adelante en el capítulo.

### <a name="the-banner-region"></a>Región del banner

El banner se encuentra en la parte superior de la pantalla, en la esquina superior izquierda de la vista web. El banner normal muestra el nombre y el icono de la carpeta cuyo contenido se muestra en la lista de archivos de la derecha. Sin embargo, si la ventana se vuelve demasiado corta, puede que no haya ninguna habitación debajo del icono para mostrar información. Por este motivo, Generic.htt también define un minibanner que solo muestra el nombre de la carpeta. Ambos banners se definen inicialmente como ocultos. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) elige cuál se va a mostrar y lo establece en "visible".

El banner normal de Generic.htt se define mediante:


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



La primera parte de la sección banner muestra el título con una regla horizontal debajo. Las etiquetas de tabla se usan para controlar su posición. El atributo nowrap se establece para <TD> etiqueta para evitar el ajuste de palabras. El sistema reemplazará %THISDIRNAME% por el nombre de la carpeta actual. A continuación, se carga un objeto **WebViewFolderIcon,** con un identificador de "Icono" para simplificar, para extraer y mostrar el icono de la carpeta.

La sección minibanner es similar al banner normal. El formato del título se coloca ligeramente más alto y no tiene una regla. Dado que no hay ningún icono, no se carga el objeto **WebViewFolderIcon.**


```
<div id="MiniBanner" style="visibility: hidden">
    <table class="clsStd"><tr><td nowrap>
        <p class=Title style="margin-left: 16px; margin-top: 4px">
        %THISDIRNAME%
    </td></tr></table>
</div>
                    
```



### <a name="the-info-region"></a>La región de información

La parte de la vista web debajo del banner se usa para presentar información detallada sobre el elemento seleccionado. Si no se selecciona ningún elemento, se muestra un mensaje predeterminado. Dado que Generic.htt solo muestra un único bloque de texto, esta sección es bastante sencilla.


```
<div id="Info">
    <p style="margin-top: 16px");
        <span id="TextBlock">
        </span>
</div>
                    
```



La mayor parte del trabajo de recopilación de la información se controla mediante un [script](#retrieving-and-displaying-folder-information) de información de carpetas que se describe más adelante en el capítulo. Muestra la información asignando el texto a [TextBlock.innerHTML.](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)

Puede personalizar fácilmente la presentación de información modificando estos elementos o incluyendo otros adicionales. Se puede usar todo lo que se puede colocar en una página web. Por ejemplo, para mostrar un vínculo a su sitio web, puede agregar un elemento delimitador después del bloque de texto en Generic.htt.


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

Por último, Generic.htt carga un [**objeto WebViewFolderContents**](webviewfoldercontents.md) para la región FileList. Dado que su identificador se establece en "FileList", a partir de ahora se hará referencia a él como el objeto FileList.


```
<object id="FileList" border=0 tabindex=1 classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2"
        </object>
                    
```



El objeto FileList se encuentra en la mayoría de las vistas web y tiene varios propósitos. FileList muestra la lista de elementos contenidos en la carpeta seleccionada con las mismas opciones y apariencia que la lista de archivos en el estilo clásico. Cuando se selecciona un elemento, FileList notifica a la vista web mediante la activación de [un evento SelectionChanged.](#retrieving-and-displaying-folder-information) FileList también expone métodos y propiedades que se pueden usar para recuperar información sobre elementos individuales y controlar la posición y el tamaño de su área de presentación.

Aunque el objeto FileList es muy útil, solo devuelve información estándar del sistema de archivos, como el tamaño de archivo o los atributos. Para recuperar otros tipos de información de una carpeta de Shell, tendrá que cargar y controlar objetos adicionales. Cualquier objeto que se pueda hospedar en una página web se puede usar con una vista web.

### <a name="the-template-head"></a>El jefe de plantilla

El responsable de la plantilla de vista web contiene los scripts y las funciones que hacen la mayor parte del trabajo real. Hay dos tareas esenciales que deben controlarse. Uno es el diseño de la presentación de la vista web, que debe ajustarse para adaptarse a diferentes regiones de visualización. La otra es recuperar y mostrar información de la carpeta cuando se selecciona un elemento. Al igual que con las hojas de estilos, es mejor incluir todos los scripts y funciones en la plantilla en lugar de hacer referencia a ellos como archivos independientes.

### <a name="controlling-the-web-view-layout"></a>Controlar el diseño de vista web

El área disponible para una vista web depende del tamaño de la ventana vista web y de la cantidad de ella que toma la barra Windows explorador. Esta área cambiará cada vez que se cambie el tamaño de Windows la barra del Explorador. Por lo tanto, el diseño debe coincidir con el área disponible cuando se carga una vista web y cambiar correctamente cuando se cambia de tamaño. Gran parte del diseño se especifica en la hoja de estilos. La región info, por ejemplo, se define para ocupar el 30 % más a la izquierda de la vista web.


```
#Info       {position: absolute; top: 88px; width: 30%; background: window;
    overflow: auto}
                    
```



A medida que se cambia el tamaño de una vista web, el ancho de la región De información cambiará para mantener ese porcentaje. [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) administra los problemas de diseño que no se pueden controlar mediante una hoja de estilos.

### <a name="loading-and-initializing-the-web-view"></a>Cargar e inicializar la vista web

Cuando se carga una vista web, el diseño debe ajustarse para ajustarse al área de presentación disponible. Dado que aún no se ha seleccionado ningún elemento, las vistas web normalmente muestran información predeterminada que se aplica a toda la carpeta. Para controlar la inicialización, la etiqueta BODY para Generic.htt detecta el evento &lt; &gt; [onload](/previous-versions//ms531409(v=vs.85)) y llama a la **función Init.**


```
<body scroll=no onload="Init">
                    
```



**Init** es una función JScript sencilla.


```
function Init() {
    window.onresize = FixSize;
    FixSize();
    TextBlock.innerHTML = L_Intro_Text;
}
                    
```



**Init** enlaza [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) al evento [window.onresize](https://msdn.microsoft.com/library/ms536959(VS.85).aspx) para que se llame cuando cambie el área de presentación de la vista web. A continuación, ejecuta FixSize para establecer el diseño inicial y asigna L \_ Intro Text a la región \_ Info. L \_ Intro Text es un bloque de texto \_ introductorio que se define en la sección de hoja de estilos.


```
var L_Intro_Text    = "This folder contains a variety of interesting stuff.<br>
<br>To get information about any of them, click the items icon.<br><br>";
                    
```



### <a name="adjusting-the-layout-by-using-the-fixsize-function"></a>Ajustar el diseño mediante la función FixSize

La [función FixSize](#adjusting-the-layout-by-using-the-fixsize-function) se usa para especificar varios aspectos del diseño que la hoja de estilos no puede controlar.

Hay dos banners posibles que se pueden usar, en función del alto de la vista web.


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



Generic.htt usa una altura de 200 píxeles como línea divisora entre normales y minibanners. Establece el estilo del banner seleccionado en visible y el otro en oculto. También establece varias propiedades de diseño para las regiones Info y FileList para que quepa correctamente con el banner seleccionado.

Si una vista web se vuelve demasiado estrecha, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) usa el ancho completo del área de presentación para la pantalla FileList.


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



Generic.htt usa 400 píxeles como línea divisora entre las pantallas estrechas y anchas. Si la vista web es demasiado estrecha, [FixSize](#adjusting-the-layout-by-using-the-fixsize-function) oculta la región Info y modifica la propiedad [PixelLeft](https://msdn.microsoft.com/library/ms534336(VS.85).aspx) de FileList para que rellene toda la región debajo del banner.

Las últimas líneas de [FixSize ajustan](#adjusting-the-layout-by-using-the-fixsize-function) varias propiedades de diseño en función de los resultados del código anterior. El ancho de la región FileList se ajusta para que rellene exactamente la parte de la vista web no ocupada por la región de información. El alto de la región de información tiene el tamaño que cabe entre el banner y la parte inferior de la vista web.


```
document.all.FileList.style.pixelWidth = document.body.clientWidth
    document.all.FileList.style.pixelLeft;
document.all.FileList.style.pixelHeight = document.body.clientHeight
    document.all.FileList.style.pixelTop;
document.all.Info.style.pixelHeight = document.body.clientHeight
    document.all.Info.style.pixelTop;
                    
```



### <a name="retrieving-and-displaying-folder-information"></a>Recuperar y mostrar información de carpeta

Cuando un usuario selecciona un elemento, el objeto FileList activará un [evento SelectionChanged.](#retrieving-and-displaying-folder-information) Este evento se controla mediante un JScript script. Para simplificar, el script que se encuentra en Generic.htt supone que solo se puede seleccionar un elemento a la vez.


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



El script usa dos propiedades FileList, [**FileList.FocusedItem**](/windows/desktop/shell/shellfolderview-focuseditem)y [**FileList.Folder**](/windows/desktop/shell/shellfolderview-folder) para obtener información sobre el elemento. **FileList.FocusedItem** identifica el elemento seleccionado, con el nombre del elemento especificado **por FileList.FocusedItem.Name**. **FileList.Folder es** realmente un puntero a un [**objeto Folder.**](../shell/folder.md) El método [**GetDetailsOf**](/windows/desktop/shell/folder-getdetailsof) del objeto Folder se usa para recuperar la información restante sobre el elemento.

Toda la información se concatena en una sola cadena de texto, separada por <BR> etiquetas para mejorar la legibilidad. A continuación, se muestra el texto asignándose a [TextBlock.innerHTML.](https://msdn.microsoft.com/library/ms533897(VS.85).aspx)

## <a name="summary"></a>Resumen

En este capítulo se describen algunas de las técnicas que puede usar para personalizar la forma en que el Explorador de Windows muestra información sobre las carpetas de Shell. La creación Desktop.ini archivo le permite realizar una personalización sencilla, como mostrar un icono personalizado en lugar del icono de carpeta estándar. Cuando una carpeta aparece en una vista web, su diseño y presentación se controlan mediante una plantilla basada en HTML que determina qué información se muestra y cómo. Puede ejercer un alto grado de control sobre la vista web de una carpeta mediante el uso de técnicas estándar de HTML, DHTML y scripting para crear una plantilla personalizada.

 

 
