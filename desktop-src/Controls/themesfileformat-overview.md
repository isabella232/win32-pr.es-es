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
# <a name="theme-file-format"></a><span data-ttu-id="071fc-105">Formato de archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-105">Theme File Format</span></span>

<span data-ttu-id="071fc-106">En este documento se describe el formato de los archivos de tema (. theme).</span><span class="sxs-lookup"><span data-stu-id="071fc-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="071fc-107">Un archivo. Theme es un archivo de texto. ini que se divide en secciones que especifican elementos visuales que aparecen en un escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="071fc-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="071fc-108">Los nombres de sección se incluyen entre corchetes ( \[ \] ) en el archivo. ini.</span><span class="sxs-lookup"><span data-stu-id="071fc-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="071fc-109">Se incorporó un nuevo formato de archivo,. themepack, con Windows 7 para ayudar a los usuarios a compartir temas.</span><span class="sxs-lookup"><span data-stu-id="071fc-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="071fc-110">Los temas se pueden seleccionar en el panel de control personalización solo en Windows 7 Home Premium o superior, o solo en Windows Server 2008 R2 cuando se instala el componente de escritorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="071fc-111">Los temas siguientes se describen en este artículo.</span><span class="sxs-lookup"><span data-stu-id="071fc-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="071fc-112">Crear un archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="071fc-113">Descripción de un archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="071fc-114">[\[\]Sección tema](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="071fc-115">[\[Sección de colores del panel de control \\ \]](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="071fc-116">[\[Sección de \\ cursores del panel de control \]](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="071fc-117">[\[Sección escritorio del panel de control \\ \]](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="071fc-118">[\[Sección de presentación \]](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="071fc-119">[\[Sección de métricas \]](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="071fc-120">[\[Sección de estilos visuales \]](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="071fc-121">[\[\]Secciones sonidos y \[ AppEvents \] (sonidos)](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="071fc-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="071fc-122">[\[Sección de arranque \]](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="071fc-123">[\[\]Sección MasterThemeSelector](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="071fc-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="071fc-124">Ejemplo de un archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="071fc-125">Instalación de archivos de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="071fc-126">Paquetes de temas</span><span class="sxs-lookup"><span data-stu-id="071fc-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="071fc-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="071fc-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="071fc-128">Crear un archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-128">Creating a Theme File</span></span>

<span data-ttu-id="071fc-129">Un archivo. theme permite cambiar la apariencia de determinados elementos del escritorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="071fc-130">Puede crear o modificar un archivo. theme de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="071fc-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="071fc-131">Modifique la configuración de personalización o de pantalla en el panel de control y guarde la configuración como un archivo. theme.</span><span class="sxs-lookup"><span data-stu-id="071fc-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="071fc-132">Consulte la ayuda de Windows para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="071fc-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="071fc-133">Cree un archivo. theme manualmente para obtener un mayor nivel de control sobre los detalles de su tema.</span><span class="sxs-lookup"><span data-stu-id="071fc-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="071fc-134">Para que el tema esté disponible para otros usuarios, debe proporcionar el archivo. theme, así como los archivos de imagen de fondo, protector de pantalla e iconos.</span><span class="sxs-lookup"><span data-stu-id="071fc-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="071fc-135">Puede hacerlo con un paquete de [temas](#theme-packs).</span><span class="sxs-lookup"><span data-stu-id="071fc-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="071fc-136">Descripción de un archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-136">Description of a Theme File</span></span>

<span data-ttu-id="071fc-137">Los archivos de tema tienen una serie de secciones obligatorias y opcionales.</span><span class="sxs-lookup"><span data-stu-id="071fc-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="071fc-138">A continuación se describen las secciones de los archivos. theme y se proporcionan ejemplos de cómo especificar los cambios para los distintos elementos.</span><span class="sxs-lookup"><span data-stu-id="071fc-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="071fc-139">\[\]Sección tema</span><span class="sxs-lookup"><span data-stu-id="071fc-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-140">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-140">This section is optional.</span></span> <span data-ttu-id="071fc-141">Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="071fc-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="071fc-142">La \[ sección del tema \] identifica el nombre del tema personalizado y especifica el logotipo de la marca del tema y los iconos del escritorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="071fc-143">La primera parte de la \[ sección del tema \] contiene los dos elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="071fc-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="071fc-144">Elemento</span><span class="sxs-lookup"><span data-stu-id="071fc-144">Element</span></span>                                                                                                                    | <span data-ttu-id="071fc-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="071fc-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="071fc-146">DisplayName = Nombre</span><span class="sxs-lookup"><span data-stu-id="071fc-146">DisplayName=name</span></span><br/> <span data-ttu-id="071fc-147">or</span><span class="sxs-lookup"><span data-stu-id="071fc-147">or</span></span><br/> <span data-ttu-id="071fc-148">DisplayName = @module ,-stringId</span><span class="sxs-lookup"><span data-stu-id="071fc-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="071fc-149">ejemplo: DisplayName = @themeui.dll ,-2013</span><span class="sxs-lookup"><span data-stu-id="071fc-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="071fc-150">DisplayName es el nombre del tema que se mostrará en el panel de control de personalización.</span><span class="sxs-lookup"><span data-stu-id="071fc-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="071fc-151">Puede ser una cadena o una referencia a un nombre traducido.</span><span class="sxs-lookup"><span data-stu-id="071fc-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="071fc-152">Este campo es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-152">This field is optional.</span></span> <span data-ttu-id="071fc-153">Si falta, se utiliza el nombre de archivo de tema como nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="071fc-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="071fc-154">BrandImage = ruta de acceso de la imagen</span><span class="sxs-lookup"><span data-stu-id="071fc-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="071fc-155">ejemplo: BrandImage = c: \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="071fc-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="071fc-156">**Windows 7 y versiones posteriores** BrandImage especifica la ruta de acceso a un archivo gráfico de marca que se incorpora en la vista previa del tema en el panel de control de personalización.</span><span class="sxs-lookup"><span data-stu-id="071fc-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="071fc-157">El gráfico del icono debe ser un archivo PNG.</span><span class="sxs-lookup"><span data-stu-id="071fc-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="071fc-158">El gráfico se escala a 80x240 píxeles, por lo que se recomienda proporcionar una imagen de ese tamaño.</span><span class="sxs-lookup"><span data-stu-id="071fc-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="071fc-159">La galería de temas respeta las regiones transparentes del icono de la marca.</span><span class="sxs-lookup"><span data-stu-id="071fc-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="071fc-160">Este campo es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-160">This field is optional.</span></span> <span data-ttu-id="071fc-161">Si falta, no se muestra ningún logotipo como icono de tema.</span><span class="sxs-lookup"><span data-stu-id="071fc-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="071fc-162">En el resto de la \[ sección del tema se \] especifican iconos personalizados para características de escritorio como el equipo, mis documentos, la red y la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="071fc-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="071fc-163">Si no especifica iconos de escritorio personalizados, el escritorio muestra los iconos de escritorio predeterminados del sistema.</span><span class="sxs-lookup"><span data-stu-id="071fc-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="071fc-164">A continuación se muestran dos ejemplos de cómo un archivo. theme establece el icono del **equipo** .</span><span class="sxs-lookup"><span data-stu-id="071fc-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="071fc-165">A continuación se muestran los valores de los iconos de escritorio predeterminados de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="071fc-165">The following are values for the default desktop icons in Windows 7.</span></span>


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



### <a name="control-panelcolors-section"></a><span data-ttu-id="071fc-166">\[Sección de colores del panel de control \\ \]</span><span class="sxs-lookup"><span data-stu-id="071fc-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-167">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-167">This section is optional.</span></span> <span data-ttu-id="071fc-168">Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="071fc-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="071fc-169">Si el tema usa el estilo visual de Aero, debe evitar invalidar los valores predeterminados en esta sección.</span><span class="sxs-lookup"><span data-stu-id="071fc-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="071fc-170">El color de los elementos, como las barras de desplazamiento, el texto y los botones, son personalizables.</span><span class="sxs-lookup"><span data-stu-id="071fc-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="071fc-171">El archivo. theme especifica los valores RGB que se van a cambiar para estos elementos.</span><span class="sxs-lookup"><span data-stu-id="071fc-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="071fc-172">Los valores invalidan los valores predeterminados del estilo visual y se usan cuando el tema se basa en temas de Windows clásico, Windows 7 Basic o contraste alto.</span><span class="sxs-lookup"><span data-stu-id="071fc-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="071fc-173">A continuación se describe un ejemplo de cómo se establecen los colores.</span><span class="sxs-lookup"><span data-stu-id="071fc-173">Following is an example of how colors are set.</span></span>


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



### <a name="control-panelcursors-section"></a><span data-ttu-id="071fc-174">\[Sección de \\ cursores del panel de control \]</span><span class="sxs-lookup"><span data-stu-id="071fc-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-175">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-175">This section is optional.</span></span> <span data-ttu-id="071fc-176">Si no incluye esta sección en el archivo. theme, el sistema utiliza cursores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="071fc-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="071fc-177">Un tema también puede cambiar la apariencia de los cursores.</span><span class="sxs-lookup"><span data-stu-id="071fc-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="071fc-178">Para ello, cree archivos. cur para reemplazar los cursores predeterminados de Windows.</span><span class="sxs-lookup"><span data-stu-id="071fc-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="071fc-179">El ejemplo siguiente es de un archivo. theme que define los cursores de un tema denominado *Sports*.</span><span class="sxs-lookup"><span data-stu-id="071fc-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


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



### <a name="control-paneldesktop-section"></a><span data-ttu-id="071fc-180">\[Sección escritorio del panel de control \\ \]</span><span class="sxs-lookup"><span data-stu-id="071fc-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-181">Esta sección es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="071fc-181">This section is required.</span></span> <span data-ttu-id="071fc-182">Si no incluye esta sección en el archivo. theme, el sistema omite el tema y no muestra el tema en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="071fc-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="071fc-183">Puede crear un fondo de escritorio personalizado y especificar una ruta de acceso al archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="071fc-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="071fc-184">En el ejemplo siguiente se muestra cómo modificar la apariencia del escritorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-184">The following example shows how to modify the desktop appearance.</span></span>


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



### <a name="slideshow-section"></a><span data-ttu-id="071fc-185">\[Sección de presentación \]</span><span class="sxs-lookup"><span data-stu-id="071fc-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="071fc-186">**Windows 7 y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="071fc-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="071fc-187">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-187">This section is optional.</span></span> <span data-ttu-id="071fc-188">Si no incluye esta sección en el archivo. theme, el sistema usa la imagen de fondo del escritorio especificada en la \[ sección escritorio del panel de control \\ \] .</span><span class="sxs-lookup"><span data-stu-id="071fc-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="071fc-189">Si incluye esta sección, debe especificar la configuración de la presentación aquí.</span><span class="sxs-lookup"><span data-stu-id="071fc-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="071fc-190">El fondo del tema puede ser una presentación de imágenes almacenadas localmente o de imágenes atendidas por una fuente RSS.</span><span class="sxs-lookup"><span data-stu-id="071fc-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="071fc-191">La \[ \] sección de presentación de diapositivas del archivo contiene los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="071fc-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="071fc-192">Atributo</span><span class="sxs-lookup"><span data-stu-id="071fc-192">Attribute</span></span></th>
<th><span data-ttu-id="071fc-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="071fc-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="071fc-194">Interval = número de milisegundos</span><span class="sxs-lookup"><span data-stu-id="071fc-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="071fc-195">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-195">Required.</span></span> <span data-ttu-id="071fc-196">Interval es un número que determina la frecuencia con la que cambia el fondo.</span><span class="sxs-lookup"><span data-stu-id="071fc-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="071fc-197">Se mide en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="071fc-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="071fc-198">Orden aleatorio = 0 o 1</span><span class="sxs-lookup"><span data-stu-id="071fc-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="071fc-199">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-199">Required.</span></span> <span data-ttu-id="071fc-200">Orden aleatorio: identifica si el fondo está en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="071fc-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="071fc-201">0 = Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="071fc-201">0 = Disabled</span></span><br/> <span data-ttu-id="071fc-202">1 = Habilitado</span><span class="sxs-lookup"><span data-stu-id="071fc-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="071fc-203">Fuente RSS = dirección URL de la fuente RSS</span><span class="sxs-lookup"><span data-stu-id="071fc-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="071fc-204">Obligatorio si no se especifica ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="071fc-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="071fc-205">Fuente RSS especifica una fuente RSS para utilizarla como presentación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="071fc-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="071fc-206">Para que la fuente funcione, debe hacer referencia a las imágenes de alta resolución que se adhieren a la &quot; norma de alojamientos &quot; utilizada por la <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">plataforma RSS de Windows</a>.</span><span class="sxs-lookup"><span data-stu-id="071fc-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="071fc-207">Debido a esta limitación, los archivos. theme que incluyen una fuente RSS deben crearse manualmente.</span><span class="sxs-lookup"><span data-stu-id="071fc-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="071fc-208">No se puede especificar fuente RSS y ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="071fc-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="071fc-209">ImagesRootPath = ruta de acceso a la carpeta de imágenes</span><span class="sxs-lookup"><span data-stu-id="071fc-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="071fc-210">Obligatorio si no se especifica fuente RSS.</span><span class="sxs-lookup"><span data-stu-id="071fc-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="071fc-211">ImagesRootPath especifica una ruta de acceso a un conjunto de imágenes que se desea utilizar como presentación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="071fc-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="071fc-212">Las imágenes de las subcarpetas no se incluyen en la presentación.</span><span class="sxs-lookup"><span data-stu-id="071fc-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="071fc-213">ImagesRootPath admite las sustituciones de variables de entorno en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="071fc-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="071fc-214">No se puede especificar fuente RSS y ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="071fc-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="071fc-215">Item<em>N</em>PATH = PATH (s) a imágenes específicas</span><span class="sxs-lookup"><span data-stu-id="071fc-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="071fc-216">Para su uso con ImagesRootPath.</span><span class="sxs-lookup"><span data-stu-id="071fc-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="071fc-217">La ruta de acceso del elemento<em>N</em>especifica las rutas a imágenes específicas, de modo que puede limitar la presentación a imágenes particulares en lugar de a todas las imágenes de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="071fc-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="071fc-218">Si no se especifica ninguna ruta, se usan todas las imágenes de la ruta de acceso ImagesRootPath en la presentación, incluidas las imágenes agregadas después de crear e instalar el tema.</span><span class="sxs-lookup"><span data-stu-id="071fc-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="071fc-219">La ruta de acceso del elemento<em>N</em>es compatible con las sustituciones de variables de entorno en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="071fc-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="071fc-220"><em>N</em> es 0, 1, 2, etc.</span><span class="sxs-lookup"><span data-stu-id="071fc-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="071fc-221">En los siguientes ejemplos se muestra cómo un archivo. theme especifica la presentación para incluir un conjunto de imágenes almacenadas localmente.</span><span class="sxs-lookup"><span data-stu-id="071fc-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


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



<span data-ttu-id="071fc-222">En el ejemplo siguiente se muestra una plantilla para un archivo. theme que crea una presentación de fondo de escritorio mediante imágenes de una fuente RSS.</span><span class="sxs-lookup"><span data-stu-id="071fc-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="071fc-223">Siga estos pasos para personalizar la plantilla:</span><span class="sxs-lookup"><span data-stu-id="071fc-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="071fc-224">Copie el ejemplo siguiente y péguelo en un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="071fc-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="071fc-225">Reemplace {ThemeName} por el nombre que desea que aparezca en la galería de temas del panel de control de personalización.</span><span class="sxs-lookup"><span data-stu-id="071fc-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="071fc-226">Reemplace {rssfeedurl} por la ruta de acceso completa a una fuente RSS compatible.</span><span class="sxs-lookup"><span data-stu-id="071fc-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="071fc-227">Guarde los cambios como un archivo con la extensión ". theme".</span><span class="sxs-lookup"><span data-stu-id="071fc-227">Save the changes as a file with the ".theme" extension.</span></span>


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



### <a name="metrics-section"></a><span data-ttu-id="071fc-228">\[Sección de métricas \]</span><span class="sxs-lookup"><span data-stu-id="071fc-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-229">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-229">This section is optional.</span></span> <span data-ttu-id="071fc-230">Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración de estilo visual predeterminada.</span><span class="sxs-lookup"><span data-stu-id="071fc-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="071fc-231">Las métricas del sistema se pueden especificar en un archivo. theme.</span><span class="sxs-lookup"><span data-stu-id="071fc-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="071fc-232">Las métricas del sistema son las dimensiones de varios elementos para mostrar, como el ancho del borde de la ventana, el alto del icono o el ancho de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="071fc-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="071fc-233">Los valores NonclientMetrics y IconMetrics son estructuras binarias definidas por NONCLIENTMETRICS y ICONMETRICS en Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="071fc-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="071fc-234">A continuación se describe un ejemplo de cómo cambiar las métricas del sistema.</span><span class="sxs-lookup"><span data-stu-id="071fc-234">Following is an example of how to change system metrics.</span></span>


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



### <a name="visual-styles-section"></a><span data-ttu-id="071fc-235">\[Sección de estilos visuales \]</span><span class="sxs-lookup"><span data-stu-id="071fc-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-236">Esta sección es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="071fc-236">This section is required.</span></span> <span data-ttu-id="071fc-237">Si no incluye esta sección en el archivo. theme, el sistema omite el tema y no muestra el tema en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="071fc-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="071fc-238">Puede proporcionar información específica sobre el tamaño y el color de los elementos del escritorio en los archivos. msstyles.</span><span class="sxs-lookup"><span data-stu-id="071fc-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="071fc-239">Las secciones color y tamaño de los archivos. theme se pueden reemplazar por archivos. msstyles que permiten modificar los elementos del escritorio con más detalle.</span><span class="sxs-lookup"><span data-stu-id="071fc-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="071fc-240">Estos archivos se especifican en la sección de estilos visuales de un archivo. theme.</span><span class="sxs-lookup"><span data-stu-id="071fc-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="071fc-241">A continuación se encuentra un ejemplo de una sección de estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="071fc-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="071fc-242">Agregar un elemento de ruta de acceso a un archivo. msstyles es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="071fc-243">Si proporciona una ruta de acceso, debe quitar las secciones métricas y color del archivo. theme.</span><span class="sxs-lookup"><span data-stu-id="071fc-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="071fc-244">Cuando se quitan estas secciones, los colores, las fuentes y los tamaños de un tema proceden del archivo. msstyles y coinciden con la intención del autor de. msstyles.</span><span class="sxs-lookup"><span data-stu-id="071fc-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="071fc-245">Si no se quitan las secciones de métricas y de color, puede que las ventanas o las aplicaciones tengan problemas de dibujo.</span><span class="sxs-lookup"><span data-stu-id="071fc-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="071fc-246">**Windows Vista/Windows 7:** Cuando la ruta de acceso señala a Aero. msstyles, puede especificar el color de cristal deseado, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="071fc-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="071fc-247">**Windows 7:** Cuando la ruta de acceso señala a Aero. msstyles, también puede especificar el valor de transparencia deseado, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="071fc-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="071fc-248">Si los valores de ColorizationColor y Transparency coinciden exactamente con un color del sistema, el panel de control de personalización muestra el nombre del sistema para el color.</span><span class="sxs-lookup"><span data-stu-id="071fc-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="071fc-249">De lo contrario, el color se etiqueta como "Custom".</span><span class="sxs-lookup"><span data-stu-id="071fc-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="071fc-250">A continuación se muestra una sección de VisualStyles para el tema básico de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="071fc-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="071fc-251">A continuación se muestra una sección de VisualStyles para el tema clásico de Windows.</span><span class="sxs-lookup"><span data-stu-id="071fc-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="071fc-252">A continuación se muestra una sección de VisualStyles para un contraste alto tema negro.</span><span class="sxs-lookup"><span data-stu-id="071fc-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="071fc-253">\[\]Secciones sonidos y \[ AppEvents \] (sonidos)</span><span class="sxs-lookup"><span data-stu-id="071fc-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="071fc-254">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-254">This section is optional.</span></span> <span data-ttu-id="071fc-255">Si no incluye esta sección en el archivo. theme, el sistema utiliza la configuración de sonido predeterminada.</span><span class="sxs-lookup"><span data-stu-id="071fc-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="071fc-256">El usuario puede seleccionar el icono de **sonido** en el panel de control para asociar sonidos a los eventos que se producen en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="071fc-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="071fc-257">Por ejemplo, un archivo. wav puede reproducirse cuando se abre una aplicación.</span><span class="sxs-lookup"><span data-stu-id="071fc-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="071fc-258">Un archivo. theme puede especificar archivos. wav para reemplazar los predeterminados.</span><span class="sxs-lookup"><span data-stu-id="071fc-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="071fc-259">El ejemplo siguiente muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="071fc-259">The following example shows how to do this.</span></span>


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



<span data-ttu-id="071fc-260">**Windows 7 y versiones posteriores:** Se puede especificar un nombre de esquema de sonido en lugar de enumerar cada sonido por separado.</span><span class="sxs-lookup"><span data-stu-id="071fc-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="071fc-261">El valor de SchemeName especifica el nombre de la combinación de sonidos o el nombre de la combinación de sonidos localizada, tal como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="071fc-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="071fc-262">\[Sección de arranque \]</span><span class="sxs-lookup"><span data-stu-id="071fc-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-263">**Los protectores de pantalla están en desuso en la actualización de aniversario de Windows 10 y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="071fc-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="071fc-264">Esta sección es opcional.</span><span class="sxs-lookup"><span data-stu-id="071fc-264">This section is optional.</span></span> <span data-ttu-id="071fc-265">Si no incluye esta sección en el archivo. theme, no se utiliza ningún protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="071fc-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="071fc-266">En el archivo. theme, puede especificar el protector de pantalla para Windows que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="071fc-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="071fc-267">Esto se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="071fc-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="071fc-268">\[\]Sección MasterThemeSelector</span><span class="sxs-lookup"><span data-stu-id="071fc-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="071fc-269">Esta sección es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="071fc-269">This section is required.</span></span> <span data-ttu-id="071fc-270">Si no incluye esta sección en el archivo. theme, el sistema omite el tema y no muestra el tema en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="071fc-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="071fc-271">La sección selector de tema maestro del archivo. theme siempre debe incluirse como una etiqueta que indica que el archivo es válido.</span><span class="sxs-lookup"><span data-stu-id="071fc-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="071fc-272">No tiene la opción de elegir valores para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="071fc-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="071fc-273">Esto se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="071fc-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="071fc-274">Ejemplo de un archivo de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-274">Example of a Theme File</span></span>

<span data-ttu-id="071fc-275">En el ejemplo siguiente se muestra un archivo. theme completo.</span><span class="sxs-lookup"><span data-stu-id="071fc-275">The following example shows a complete .theme file.</span></span>


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



## <a name="installing-theme-files"></a><span data-ttu-id="071fc-276">Instalación de archivos de tema</span><span class="sxs-lookup"><span data-stu-id="071fc-276">Installing Theme Files</span></span>

<span data-ttu-id="071fc-277">Cuando se inicializa Windows, el sistema operativo enumera los subdirectorios de primer nivel de% WinDir% \\ Resources \\ para identificar los temas disponibles.</span><span class="sxs-lookup"><span data-stu-id="071fc-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="071fc-278">Los archivos de tema predeterminados del sistema se encuentran en% WinDir% \\ Resources \\ themes.</span><span class="sxs-lookup"><span data-stu-id="071fc-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="071fc-279">Los archivos de tema del usuario se almacenan en% WINDIR% \\ users \\ <username> \\ AppData \\ temas locales de \\ Microsoft \\ Windows \\ .</span><span class="sxs-lookup"><span data-stu-id="071fc-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="071fc-280">Un archivo. theme tiene asociaciones de archivo. por lo tanto, las aplicaciones de instalador de temas pueden llamar a [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) en un archivo. theme para abrir la ventana de **Personalización** del panel de control en el tema especificado.</span><span class="sxs-lookup"><span data-stu-id="071fc-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="071fc-281">Paquetes de temas</span><span class="sxs-lookup"><span data-stu-id="071fc-281">Theme Packs</span></span>

<span data-ttu-id="071fc-282">**Windows 7 y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="071fc-282">**Windows 7 and later.**</span></span> <span data-ttu-id="071fc-283">Un paquete de temas es un archivo. cab que contiene no solo el archivo. theme sino también los archivos necesarios para implementar el tema en otro equipo, como archivos de sonido e imágenes.</span><span class="sxs-lookup"><span data-stu-id="071fc-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="071fc-284">Los usuarios pueden crear paquetes de temas a través del panel de control de personalización.</span><span class="sxs-lookup"><span data-stu-id="071fc-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="071fc-285">Entre los tipos de archivo admitidos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="071fc-285">Supported file types include the following:</span></span>



| <span data-ttu-id="071fc-286">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="071fc-286">File type</span></span>    | <span data-ttu-id="071fc-287">Extensión</span><span class="sxs-lookup"><span data-stu-id="071fc-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="071fc-288">Tema</span><span class="sxs-lookup"><span data-stu-id="071fc-288">Theme</span></span>        | <span data-ttu-id="071fc-289">.theme</span><span class="sxs-lookup"><span data-stu-id="071fc-289">.theme</span></span>                              |
| <span data-ttu-id="071fc-290">Imagen</span><span class="sxs-lookup"><span data-stu-id="071fc-290">Image</span></span>        | <span data-ttu-id="071fc-291">. jpg,. JPEG,. bmp,. dib,. tif,. png</span><span class="sxs-lookup"><span data-stu-id="071fc-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="071fc-292">Sonido</span><span class="sxs-lookup"><span data-stu-id="071fc-292">Sound</span></span>        | <span data-ttu-id="071fc-293">.wav</span><span class="sxs-lookup"><span data-stu-id="071fc-293">.wav</span></span>                                |
| <span data-ttu-id="071fc-294">Cursor del mouse</span><span class="sxs-lookup"><span data-stu-id="071fc-294">Mouse cursor</span></span> | <span data-ttu-id="071fc-295">. cur,. ani</span><span class="sxs-lookup"><span data-stu-id="071fc-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="071fc-296">Icono de escritorio</span><span class="sxs-lookup"><span data-stu-id="071fc-296">Desktop icon</span></span> | <span data-ttu-id="071fc-297">.ico</span><span class="sxs-lookup"><span data-stu-id="071fc-297">.ico</span></span>                                |
| <span data-ttu-id="071fc-298">Logotipo de marca</span><span class="sxs-lookup"><span data-stu-id="071fc-298">Brand logo</span></span>   | <span data-ttu-id="071fc-299">.png</span><span class="sxs-lookup"><span data-stu-id="071fc-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="071fc-300">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="071fc-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="071fc-301">Información general sobre los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="071fc-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

