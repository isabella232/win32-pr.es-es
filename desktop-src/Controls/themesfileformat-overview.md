---
title: Formato de archivo de tema
description: En este documento se describe el formato de los archivos theme (.theme). Un archivo .theme es un .ini de texto que se divide en secciones, que especifican los elementos visuales que aparecen en un Windows escritorio. Los nombres de sección se encapsulan entre corchetes (\ \ ) en el .ini archivo.
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67fc2d73e54e4f9c319108c2b29ed62fb58266f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472320"
---
# <a name="theme-file-format"></a>Formato de archivo de tema

En este documento se describe el formato de los archivos theme (.theme). Un archivo .theme es un .ini de texto que se divide en secciones, que especifican los elementos visuales que aparecen en un Windows escritorio. Los nombres de sección se encapsulan entre corchetes ( \[ \] ) en el .ini archivo.

Se introdujo un nuevo formato de archivo, .themepack, con Windows 7 para ayudar a los usuarios a compartir temas. Los temas se pueden seleccionar en personalización Panel de control solo en Windows 7 Home Premium o posterior, o solo en Windows Server 2008 R2 cuando se instala el componente Desktop.

En este artículo se tratan los temas siguientes.

-   [Crear un archivo de tema](#creating-a-theme-file)
-   [Descripción de un archivo de tema](#description-of-a-theme-file)
    -   [\[Sección \] tema](#theme-section)
    -   [\[Panel de control de \\ colores \]](#control-panelcolors-section)
    -   [\[Panel de control de \\ cursores \]](#control-panelcursors-section)
    -   [\[Panel de control \\ Desktop \]](#control-paneldesktop-section)
    -   [\[Sección \] presentación](#slideshow-section)
    -   [\[Sección \] métricas](#metrics-section)
    -   [\[Sección Estilos \] visuales](#visual-styles-section)
    -   [\[Secciones \] \[ Sonidos y \] AppEvents (sonidos)](#sounds-and-appevents-sections-sounds)
    -   [\[Sección \] de arranque](#boot-section)
    -   [\[Sección MasterThemeSelector \]](#masterthemeselector-section)
-   [Ejemplo de un archivo de tema](#example-of-a-theme-file)
-   [Instalación de archivos de tema](#installing-theme-files)
-   [Paquetes de temas](#theme-packs)
-   [Temas relacionados](#related-topics)

## <a name="creating-a-theme-file"></a>Crear un archivo de tema

Un archivo .theme permite cambiar la apariencia de determinados elementos de escritorio. Puede crear o modificar un archivo .theme de dos maneras:

-   Modifique la personalización o muestre la configuración Panel de control y guarde la configuración como un archivo .theme. Consulte la Windows ayuda para obtener instrucciones.
-   Cree manualmente un archivo .theme para obtener un mayor nivel de control sobre los detalles del tema.

Para que el tema esté disponible para otros usuarios, debe proporcionar el archivo .theme, así como la imagen de fondo, el protector de pantalla y los archivos de iconos. Puede hacerlo con un paquete [de temas](#theme-packs).

## <a name="description-of-a-theme-file"></a>Descripción de un archivo de tema

Los archivos de tema tienen varias secciones obligatorias y opcionales. A continuación se describen las secciones de los archivos .theme y se proporcionan ejemplos de cómo especificar cambios para los distintos elementos.

### <a name="theme-section"></a>\[Sección \] tema

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, el sistema usa la configuración predeterminada.

 

La sección Tema identifica el nombre del tema personalizado y especifica el logotipo de marca del tema y los iconos \[ \] de escritorio.

La primera parte de la \[ sección Tema contiene los dos elementos \] siguientes:



| Elemento                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName=name<br/> o<br/> DisplayName= @module ,-stringId<br/> ejemplo: DisplayName= @themeui.dll ,-2013 | DisplayName es el nombre del tema que se mostrará en el cuadro de diálogo Personalization Panel de control. Puede ser una cadena o una referencia a un nombre localizado.<br/> Este campo es opcional. Si falta, el nombre de archivo del tema se usa como nombre del tema.<br/>                                                                                                                                                                                                                                         |
| BrandImage=path to image<br/> ejemplo: BrandImage=c: \\ Fabrikam \\brand.png<br/>                                 | **Windows 7 y versiones posteriores** BrandImage especifica la ruta de acceso a un archivo gráfico con marca que se incorpora en la versión preliminar del tema en el panel personalización Panel de control.<br/> El gráfico de iconos debe ser un archivo PNG. El gráfico se escala a 80 x 240 píxeles, por lo que se recomienda proporcionar una imagen de ese tamaño. La galería de temas respeta las regiones transparentes del icono de marca.<br/> Este campo es opcional. Si falta, no se muestra ningún logotipo como icono de tema.<br/> |



 

El resto de la sección Tema especifica iconos personalizados para características de escritorio como \[ \] Equipo, Mis documentos, Red y papelera de reciclaje. Si no especifica iconos de escritorio personalizados, el escritorio muestra los iconos de escritorio predeterminados del sistema.

A continuación se muestran dos ejemplos de cómo un archivo .theme establece el **icono Equipo.**


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



A continuación se muestran los valores de los iconos de escritorio predeterminados Windows 7.


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



### <a name="control-panelcolors-section"></a>\[Panel de control de \\ colores \]

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, el sistema usa la configuración predeterminada. Si el tema usa el estilo visual Dea, debe evitar reemplazar los valores predeterminados de esta sección.

 

El color de los elementos, como las barras de desplazamiento, el texto y los botones, son personalizables. El archivo .theme especifica los valores RGB que se cambiarán para estos elementos. Los valores reemplazan los valores predeterminados del estilo Windows visual y se usan cuando el tema se basa en los temas clásico, Windows 7 Básico o contraste alto.

A continuación se muestra un ejemplo de cómo se establecen los colores.


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



### <a name="control-panelcursors-section"></a>\[Panel de control de \\ cursores \]

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, el sistema usa cursores predeterminados.

 

Un tema también puede cambiar la apariencia de los cursores. Para ello, cree archivos .cur para reemplazar los cursores de Windows predeterminados. El ejemplo siguiente es de un archivo .theme que define los cursores de un tema denominado *Sports*.


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



### <a name="control-paneldesktop-section"></a>\[Panel de control \\ Desktop \]

> [!Note]  
> Esta sección es obligatoria. Si no incluye esta sección en el archivo .theme, el sistema omite el tema y no muestra el tema en Panel de control.

 

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



### <a name="slideshow-section"></a>\[Sección \] presentación

**Windows 7 y versiones posteriores.**

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, el sistema usa la imagen de fondo del escritorio especificada en la \[ Panel de control \\ \] Desktop. Si incluye esta sección, debe especificar aquí la configuración de la presentación de diapositivas.

 

El fondo del tema puede ser una presentación de diapositivas de imágenes almacenadas localmente o de imágenes atendidas por una fuente RSS. La \[ sección Presentación del archivo contiene los atributos \] siguientes:




| Atributo | Descripción | 
|-----------|-------------|
| Interval=número de milisegundos | Necesario. Interval es un número que determina la frecuencia con la que cambia el fondo. Se mide en milisegundos. | 
| Shuffle=0 o 1 | Necesario. Shuffle identifica si se orden aleatorio en segundo plano.<br /> 0 = Deshabilitado<br /> 1 = Habilitado<br /> | 
| RSSFeed=URL a fuente RSS | Obligatorio si no se especifica ImagesRootPath. RSSFeed especifica una fuente RSS que se usará como presentación en segundo plano. Para que la fuente funcione, debe hacer referencia a imágenes de alta resolución que se adhieren al estándar de "gabinetes" que usa Windows <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">plataforma RSS.</a> Debido a esta limitación, los archivos .theme que incluyen una fuente RSS deben crearse manualmente. <br /><blockquote>[!Note]<br />No puede especificar RSSFeed e ImagesRootPath.</blockquote><br /><br /> | 
| ImagesRootPath=path to image folder | Obligatorio si no se especifica RSSFeed. ImagesRootPath especifica una ruta de acceso a un conjunto de imágenes que desea usar como presentación en segundo plano. Las imágenes de subcarpetas no se incluyen en la presentación de diapositivas.<br /> ImagesRootPath admite sustituciones de variables de entorno en la ruta de acceso.<br /><blockquote>[!Note]<br />No puede especificar RSSFeed e ImagesRootPath.</blockquote><br /><br /> | 
| Item<em>N</em>Path=path(s) to specific image(s) | Para su uso con ImagesRootPath. <br /> Ruta<em>de acceso</em>del elemento N especifica rutas de acceso a imágenes específicas, por lo que puede limitar la presentación de diapositivas a imágenes concretas en lugar de a todas las imágenes de una carpeta. Si no se especifica ninguna ruta de acceso, todas las imágenes de la ruta de acceso ImagesRootPath se usan en la presentación de diapositivas, incluidas las imágenes agregadas después de crear e instalar el tema.<br /> La ruta<em>de acceso</em>del elemento N admite sustituciones de variables de entorno en la ruta de acceso. <em>N</em> es 0, 1, 2, y así sucesivamente. <br /> | 




 

En los ejemplos siguientes se muestra cómo un archivo .theme especifica la presentación de diapositivas para incluir un conjunto de imágenes almacenadas localmente.


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



El ejemplo siguiente es una plantilla para un archivo .theme que crea una presentación de diapositivas de fondo de escritorio mediante imágenes de una fuente RSS. Siga estos pasos para personalizar la plantilla:

1.  Copie el ejemplo siguiente y péguelo en un editor de texto.
2.  Reemplace {themename} por el nombre que desea que aparezca en la galería de temas Panel de control personalización.
3.  Reemplace {rssfeedurl} por la ruta de acceso completa a una fuente RSS compatible.
4.  Guarde los cambios como un archivo con la extensión ".theme".


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



### <a name="metrics-section"></a>\[Sección \] métricas

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, el sistema usa la configuración de estilo visual predeterminada.

 

Puede especificar métricas del sistema en un archivo .theme. Las métricas del sistema son las dimensiones de varios elementos de visualización, como el ancho del borde de la ventana, el alto del icono o el ancho de la barra de desplazamiento. Los valores NonclientMetrics e IconMetrics son estructuras binarias definidas por NONCLIENTMETRICS e ICONMETRICS en winuser.h. A continuación se muestra un ejemplo de cómo cambiar las métricas del sistema.


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



### <a name="visual-styles-section"></a>\[Sección Estilos \] visuales

> [!Note]  
> Esta sección es obligatoria. Si no incluye esta sección en el archivo .theme, el sistema omite el tema y no muestra el tema en Panel de control.

 

Puede proporcionar información específica sobre el tamaño y el color de los elementos de escritorio en los archivos .msstyles. Las secciones de color y tamaño de los archivos .theme se pueden reemplazar por archivos .msstyles que permiten modificar los elementos de escritorio con más detalle. Estos archivos se especifican en la sección de estilos visuales de un archivo .theme. A continuación se muestra un ejemplo de una sección de estilos visuales.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



Agregar un elemento Path a un archivo .msstyles es opcional. Si proporciona una ruta de acceso, debe quitar las secciones de métricas y colores del archivo .theme. Cuando se quitan estas secciones, los colores, las fuentes y los tamaños de un tema proceden del archivo .msstyles y coinciden con la intención del autor de .msstyles. Si no se quitan las secciones de métricas y colores, Windows o aplicaciones tienen problemas de dibujo.

**Windows Vista/Windows 7:** Cuando la ruta de acceso apunta a Aero.msstyles, puede especificar el color de cristal deseado, como se muestra en el ejemplo siguiente.

**Windows 7:** Cuando la ruta de acceso apunta a Aero.msstyles, también puede especificar el valor de transparencia deseado, como se muestra en el ejemplo siguiente.


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



Si los valores ColorizationColor y Transparency coinciden exactamente con un color del sistema, el Panel de control personalización muestra el nombre del sistema para el color. De lo contrario, el color se etiqueta como "Personalizado".

A continuación se muestra una sección VisualStyles para el tema básico Windows 7.


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



A continuación se muestra una sección VisualStyles para el tema Windows clásico.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



A continuación se muestra una sección VisualStyles para un tema contraste alto Black.


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a>\[Secciones \] \[ Sonidos y \] AppEvents (sonidos)

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, el sistema usa la configuración de sonido predeterminada.

 

El usuario puede seleccionar el **icono Sonido** de Panel de control para asociar sonidos a eventos que se producen en las aplicaciones. Por ejemplo, un archivo .wav se puede reproducir cuando se abre una aplicación. Un archivo .theme puede especificar archivos .wav para reemplazar los predeterminados. El ejemplo siguiente muestra cómo hacerlo.


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



El valor SchemeName especifica el nombre del esquema de sonido o el nombre del esquema de sonido localizado, como se muestra en el ejemplo anterior.

### <a name="boot-section"></a>\[Sección \] de arranque

> [!Note]  
> **Los protectores de pantalla están en desuso en Windows 10 actualización de aniversario y más allá.**

 

> [!Note]  
> Esta sección es opcional. Si no incluye esta sección en el archivo .theme, no se usa ningún protector de pantalla.

 

En el archivo .theme, puede especificar el protector de pantalla Windows usar. Esto se muestra en el ejemplo siguiente.


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a>\[MasterThemeSelector \] Section

> [!Note]  
> Esta sección es obligatoria. Si no incluye esta sección en el archivo .theme, el sistema omite el tema y no muestra el tema en Panel de control.

 

La sección del selector de temas maestros del archivo .theme siempre debe incluirse como una etiqueta que indique que el archivo es válido. No tiene una opción de valores para este parámetro. Esto se muestra a continuación.


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a>Ejemplo de un archivo de tema

En el ejemplo siguiente se muestra un archivo .theme completo.


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



## <a name="installing-theme-files"></a>Instalación de archivos de temas

Cuando Windows inicializa, el sistema operativo enumera los subdirectorios de primer nivel de %WinDir% Resources para identificar \\ \\ los temas disponibles. Los archivos de tema predeterminados del sistema se encuentran en %WinDir% \\ Temas de \\ recursos. Los archivos de tema de usuario se almacenan en %WinDir% \\ Users \\ <username> \\ AppData \\ Local Microsoft Windows \\ \\ \\ Themes.

Un archivo .theme tiene asociaciones de archivo; Por lo tanto, las aplicaciones del instalador de temas pueden llamar a [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) en un archivo .theme para abrir la ventana **Personalization** Panel de control al tema especificado.

## <a name="theme-packs"></a>Paquetes de temas

**Windows 7 y versiones posteriores.** Un paquete de temas es un archivo .cab que contiene no solo el archivo .theme, sino también los archivos necesarios para implementar el tema en otro equipo, como archivos de sonido e imágenes. Los usuarios pueden crear paquetes de temas a través de la página personalización Panel de control.

Entre los tipos de archivo admitidos se incluyen los siguientes:



| Tipo de archivo    | Extensión                           |
|--------------|-------------------------------------|
| Tema        | .theme                              |
| Imagen        | .jpg, .jpeg, .bmp, .dib, .tif, .png |
| Sonido        | .wav                                |
| Cursor del mouse | .cur, .ani                          |
| Icono de escritorio | .ico                                |
| Logotipo de marca   | .png                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre estilos visuales](visual-styles-overview.md)
</dt> </dl>

