---
title: Formato de archivo de tema
description: En este documento se describe el formato de los archivos de tema (. theme). Un archivo. Theme es un archivo de texto. ini que se divide en secciones que especifican elementos visuales que aparecen en un escritorio de Windows. Los nombres de sección se incluyen entre corchetes (\ \) en el archivo. ini.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "103904884"
---
# <a name="theme-file-format"></a>Formato de archivo de tema

En este documento se describe el formato de los archivos de tema (. theme). Un archivo. Theme es un archivo de texto. ini que se divide en secciones que especifican elementos visuales que aparecen en un escritorio de Windows. Los nombres de sección se incluyen entre corchetes ( \[ \] ) en el archivo. ini.

Se incorporó un nuevo formato de archivo,. themepack, con Windows 7 para ayudar a los usuarios a compartir temas. Los temas se pueden seleccionar en el panel de control personalización solo en Windows 7 Home Premium o superior, o solo en Windows Server 2008 R2 cuando se instala el componente de escritorio.

Los temas siguientes se describen en este artículo.

-   [Crear un archivo de tema](#creating-a-theme-file)
-   [Descripción de un archivo de tema](#description-of-a-theme-file)
    -   [\[\]Sección tema](#theme-section)
    -   [\[Sección de colores del panel de control \\ \]](#control-panelcolors-section)
    -   [\[Sección de \\ cursores del panel de control \]](#control-panelcursors-section)
    -   [\[Sección escritorio del panel de control \\ \]](#control-paneldesktop-section)
    -   [\[Sección de presentación \]](#slideshow-section)
    -   [\[Sección de métricas \]](#metrics-section)
    -   [\[Sección de estilos visuales \]](#visual-styles-section)
    -   [\[\]Secciones sonidos y \[ AppEvents \] (sonidos)](#sounds-and-appevents-sections-sounds)
    -   [\[Sección de arranque \]](#boot-section)
    -   [\[\]Sección MasterThemeSelector](#masterthemeselector-section)
-   [Ejemplo de un archivo de tema](#example-of-a-theme-file)
-   [Instalación de archivos de tema](#installing-theme-files)
-   [Paquetes de temas](#theme-packs)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-theme-file"></a>Crear un archivo de tema

Un archivo. theme permite cambiar la apariencia de determinados elementos del escritorio. Puede crear o modificar un archivo. theme de dos maneras:

-   Modifique la configuración de personalización o de pantalla en el panel de control y guarde la configuración como un archivo. theme. Consulte la ayuda de Windows para obtener instrucciones.
-   Cree un archivo. theme manualmente para obtener un mayor nivel de control sobre los detalles de su tema.

Para que el tema esté disponible para otros usuarios, debe proporcionar el archivo. theme, así como los archivos de imagen de fondo, protector de pantalla e iconos. Puede hacerlo con un paquete de [temas](#theme-packs).

## <a name="description-of-a-theme-file"></a>Descripción de un archivo de tema

Los archivos de tema tienen una serie de secciones obligatorias y opcionales. A continuación se describen las secciones de los archivos. theme y se proporcionan ejemplos de cómo especificar los cambios para los distintos elementos.

### <a name="theme-section"></a>\[\]Sección tema

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración predeterminada.

 

La \[ sección del tema \] identifica el nombre del tema personalizado y especifica el logotipo de la marca del tema y los iconos del escritorio.

La primera parte de la \[ sección del tema \] contiene los dos elementos siguientes:



| Elemento                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName = Nombre<br/> or<br/> DisplayName = @module ,-stringId<br/> ejemplo: DisplayName = @themeui.dll ,-2013 | DisplayName es el nombre del tema que se mostrará en el panel de control de personalización. Puede ser una cadena o una referencia a un nombre traducido.<br/> Este campo es opcional. Si falta, se utiliza el nombre de archivo de tema como nombre del tema.<br/>                                                                                                                                                                                                                                         |
| BrandImage = ruta de acceso de la imagen<br/> ejemplo: BrandImage = c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 y versiones posteriores** BrandImage especifica la ruta de acceso a un archivo gráfico de marca que se incorpora en la vista previa del tema en el panel de control de personalización.<br/> El gráfico del icono debe ser un archivo PNG. El gráfico se escala a 80x240 píxeles, por lo que se recomienda proporcionar una imagen de ese tamaño. La galería de temas respeta las regiones transparentes del icono de la marca.<br/> Este campo es opcional. Si falta, no se muestra ningún logotipo como icono de tema.<br/> |



 

En el resto de la \[ sección del tema se \] especifican iconos personalizados para características de escritorio como el equipo, mis documentos, la red y la papelera de reciclaje. Si no especifica iconos de escritorio personalizados, el escritorio muestra los iconos de escritorio predeterminados del sistema.

A continuación se muestran dos ejemplos de cómo un archivo. theme establece el icono del **equipo** .


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



A continuación se muestran los valores de los iconos de escritorio predeterminados de Windows 7.


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a>\[Sección de colores del panel de control \\ \]

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración predeterminada. Si el tema usa el estilo visual de Aero, debe evitar invalidar los valores predeterminados en esta sección.

 

El color de los elementos, como las barras de desplazamiento, el texto y los botones, son personalizables. El archivo. theme especifica los valores RGB que se van a cambiar para estos elementos. Los valores invalidan los valores predeterminados del estilo visual y se usan cuando el tema se basa en temas de Windows clásico, Windows 7 Basic o contraste alto.

A continuación se describe un ejemplo de cómo se establecen los colores.


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a>\[Sección de \\ cursores del panel de control \]

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, el sistema utiliza cursores predeterminados.

 

Un tema también puede cambiar la apariencia de los cursores. Para ello, cree archivos. cur para reemplazar los cursores predeterminados de Windows. El ejemplo siguiente es de un archivo. theme que define los cursores de un tema denominado *Sports*.


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a>\[Sección escritorio del panel de control \\ \]

> [!Note]  
> Esta sección es obligatoria. Si no incluye esta sección en el archivo. theme, el sistema omite el tema y no muestra el tema en el panel de control.

 

Puede crear un fondo de escritorio personalizado y especificar una ruta de acceso al archivo de imagen. En el ejemplo siguiente se muestra cómo modificar la apariencia del escritorio.


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a>\[Sección de presentación \]

**Windows 7 y versiones posteriores.**

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, el sistema usa la imagen de fondo del escritorio especificada en la \[ sección escritorio del panel de control \\ \] . Si incluye esta sección, debe especificar la configuración de la presentación aquí.

 

El fondo del tema puede ser una presentación de imágenes almacenadas localmente o de imágenes atendidas por una fuente RSS. La \[ \] sección de presentación de diapositivas del archivo contiene los siguientes atributos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interval = número de milisegundos</td>
<td>Obligatorio. Interval es un número que determina la frecuencia con la que cambia el fondo. Se mide en milisegundos.</td>
</tr>
<tr class="even">
<td>Orden aleatorio = 0 o 1</td>
<td>Obligatorio. Orden aleatorio: identifica si el fondo está en orden aleatorio.<br/> 0 = Deshabilitado<br/> 1 = Habilitado<br/></td>
</tr>
<tr class="odd">
<td>Fuente RSS = dirección URL de la fuente RSS</td>
<td>Obligatorio si no se especifica ImagesRootPath. Fuente RSS especifica una fuente RSS para utilizarla como presentación en segundo plano. Para que la fuente funcione, debe hacer referencia a las imágenes de alta resolución que se adhieren a la &quot; norma de alojamientos &quot; utilizada por la <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">plataforma RSS de Windows</a>. Debido a esta limitación, los archivos. theme que incluyen una fuente RSS deben crearse manualmente. <br/>
<blockquote>
[!Note]<br />
No se puede especificar fuente RSS y ImagesRootPath.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>ImagesRootPath = ruta de acceso a la carpeta de imágenes</td>
<td>Obligatorio si no se especifica fuente RSS. ImagesRootPath especifica una ruta de acceso a un conjunto de imágenes que se desea utilizar como presentación en segundo plano. Las imágenes de las subcarpetas no se incluyen en la presentación.<br/> ImagesRootPath admite las sustituciones de variables de entorno en la ruta de acceso.<br/>
<blockquote>
[!Note]<br />
No se puede especificar fuente RSS y ImagesRootPath.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Item<em>N</em>PATH = PATH (s) a imágenes específicas</td>
<td>Para su uso con ImagesRootPath. <br/> La ruta de acceso del elemento<em>N</em>especifica las rutas a imágenes específicas, de modo que puede limitar la presentación a imágenes particulares en lugar de a todas las imágenes de una carpeta. Si no se especifica ninguna ruta, se usan todas las imágenes de la ruta de acceso ImagesRootPath en la presentación, incluidas las imágenes agregadas después de crear e instalar el tema.<br/> La ruta de acceso del elemento<em>N</em>es compatible con las sustituciones de variables de entorno en la ruta de acceso. <em>N</em> es 0, 1, 2, etc. <br/></td>
</tr>
</tbody>
</table>



 

En los siguientes ejemplos se muestra cómo un archivo. theme especifica la presentación para incluir un conjunto de imágenes almacenadas localmente.


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



En el ejemplo siguiente se muestra una plantilla para un archivo. theme que crea una presentación de fondo de escritorio mediante imágenes de una fuente RSS. Siga estos pasos para personalizar la plantilla:

1.  Copie el ejemplo siguiente y péguelo en un editor de texto.
2.  Reemplace {ThemeName} por el nombre que desea que aparezca en la galería de temas del panel de control de personalización.
3.  Reemplace {rssfeedurl} por la ruta de acceso completa a una fuente RSS compatible.
4.  Guarde los cambios como un archivo con la extensión ". theme".


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a>\[Sección de métricas \]

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración de estilo visual predeterminada.

 

Las métricas del sistema se pueden especificar en un archivo. theme. Las métricas del sistema son las dimensiones de varios elementos para mostrar, como el ancho del borde de la ventana, el alto del icono o el ancho de la barra de desplazamiento. Los valores NonclientMetrics y IconMetrics son estructuras binarias definidas por NONCLIENTMETRICS y ICONMETRICS en Winuser. h. A continuación se describe un ejemplo de cómo cambiar las métricas del sistema.


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a>\[Sección de estilos visuales \]

> [!Note]  
> Esta sección es obligatoria. Si no incluye esta sección en el archivo. theme, el sistema omite el tema y no muestra el tema en el panel de control.

 

Puede proporcionar información específica sobre el tamaño y el color de los elementos del escritorio en los archivos. msstyles. Las secciones color y tamaño de los archivos. theme se pueden reemplazar por archivos. msstyles que permiten modificar los elementos del escritorio con más detalle. Estos archivos se especifican en la sección de estilos visuales de un archivo. theme. A continuación se encuentra un ejemplo de una sección de estilos visuales.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Agregar un elemento de ruta de acceso a un archivo. msstyles es opcional. Si proporciona una ruta de acceso, debe quitar las secciones métricas y color del archivo. theme. Cuando se quitan estas secciones, los colores, las fuentes y los tamaños de un tema proceden del archivo. msstyles y coinciden con la intención del autor de. msstyles. Si no se quitan las secciones de métricas y de color, puede que las ventanas o las aplicaciones tengan problemas de dibujo.

**Windows Vista/Windows 7:** Cuando la ruta de acceso señala a Aero. msstyles, puede especificar el color de cristal deseado, tal como se muestra en el ejemplo siguiente.

**Windows 7:** Cuando la ruta de acceso señala a Aero. msstyles, también puede especificar el valor de transparencia deseado, tal como se muestra en el ejemplo siguiente.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Si los valores de ColorizationColor y Transparency coinciden exactamente con un color del sistema, el panel de control de personalización muestra el nombre del sistema para el color. De lo contrario, el color se etiqueta como "Custom".

A continuación se muestra una sección de VisualStyles para el tema básico de Windows 7.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



A continuación se muestra una sección de VisualStyles para el tema clásico de Windows.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



A continuación se muestra una sección de VisualStyles para un contraste alto tema negro.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[\]Secciones sonidos y \[ AppEvents \] (sonidos)

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración de sonido predeterminada.

 

El usuario puede seleccionar el icono de **sonido** en el panel de control para asociar sonidos a los eventos que se producen en las aplicaciones. Por ejemplo, un archivo. wav puede reproducirse cuando se abre una aplicación. Un archivo. theme puede especificar archivos. wav para reemplazar los predeterminados. El ejemplo siguiente muestra cómo hacerlo.


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



**Windows 7 y versiones posteriores:** Se puede especificar un nombre de esquema de sonido en lugar de enumerar cada sonido por separado.


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



El valor de SchemeName especifica el nombre de la combinación de sonidos o el nombre de la combinación de sonidos localizada, tal como se muestra en el ejemplo anterior.

### <a name="boot-section"></a>\[Sección de arranque \]

> [!Note]  
> **Los protectores de pantalla están en desuso en la actualización de aniversario de Windows 10 y versiones posteriores.**

 

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo. theme, no se utiliza ningún protector de pantalla.

 

En el archivo. theme, puede especificar el protector de pantalla para Windows que se va a usar. Esto se muestra en el ejemplo siguiente.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[\]Sección MasterThemeSelector

> [!Note]  
> Esta sección es obligatoria. Si no incluye esta sección en el archivo. theme, el sistema omite el tema y no muestra el tema en el panel de control.

 

La sección selector de tema maestro del archivo. theme siempre debe incluirse como una etiqueta que indica que el archivo es válido. No tiene la opción de elegir valores para este parámetro. Esto se muestra a continuación.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Ejemplo de un archivo de tema

En el ejemplo siguiente se muestra un archivo. theme completo.


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a>Instalación de archivos de tema

Cuando se inicializa Windows, el sistema operativo enumera los subdirectorios de primer nivel de% WinDir% \\ Resources \\ para identificar los temas disponibles. Los archivos de tema predeterminados del sistema se encuentran en% WinDir% \\ Resources \\ themes. Los archivos de tema del usuario se almacenan en% WINDIR% \\ users \\ <username> \\ AppData \\ temas locales de \\ Microsoft \\ Windows \\ .

Un archivo. theme tiene asociaciones de archivo. por lo tanto, las aplicaciones de instalador de temas pueden llamar a [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) en un archivo. theme para abrir la ventana de **Personalización** del panel de control en el tema especificado.

## <a name="theme-packs"></a>Paquetes de temas

**Windows 7 y versiones posteriores.** Un paquete de temas es un archivo. cab que contiene no solo el archivo. theme sino también los archivos necesarios para implementar el tema en otro equipo, como archivos de sonido e imágenes. Los usuarios pueden crear paquetes de temas a través del panel de control de personalización.

Entre los tipos de archivo admitidos se incluyen los siguientes:



| Tipo de archivo    | Extensión                           |
|--------------|-------------------------------------|
| Tema        | .theme                              |
| Imagen        | . jpg,. JPEG,. bmp,. dib,. tif,. png |
| Sonido        | .wav                                |
| Cursor del mouse | . cur,. ani                          |
| Icono de escritorio | .ico                                |
| Logotipo de marca   | .png                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre los estilos visuales](visual-styles-overview.md)
</dt> </dl>

