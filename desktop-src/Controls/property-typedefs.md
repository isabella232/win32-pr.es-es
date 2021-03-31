---
title: Identificadores de propiedad (controles de Windows)
description: Este tema contiene información acerca de los valores definidos que se usan para recuperar propiedades de estilos visuales. Las definiciones se encuentran en Vssym32. h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0869ac80332a5dbdb146ee255f5c9e73f4a812
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800608"
---
# <a name="property-identifiers-windows-controls"></a>Identificadores de propiedad (controles de Windows)

Este tema contiene información acerca de los valores definidos que se usan para recuperar propiedades de estilos visuales. Las definiciones se encuentran en Vssym32. h.

## <a name="property-types"></a>Tipos de propiedades

En la tabla siguiente se enumeran los tipos de propiedad primitivos. Los valores de la primera columna no se suelen usar en las aplicaciones, pero proporcionan un medio para clasificar los identificadores de propiedad.



| Tipo de datos       | Descripción                              | Tipo devuelto                          | Función de recuperación                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ bool       | **True** o **false**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| COLOR de TMT \_      | Valor de color RGB                          | Estructura [**COLORREF**](/windows/desktop/gdi/colorref) | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | Secuencia de disco                              | **HINSTANCE**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| \_enumeración TMT       | Valor enumerado                         | Enumeración                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| \_nombre de archivo TMT   | Nombre de archivo relativo al directorio de temas | Matriz **WCHAR**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| \_fuente TMT       | Descripción de fuente                         | [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) (estructura)   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| \_hBitmap TMT    | Bitmap                                   | Identificador de **hBitmap**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ int        | Número con signo                            | Entero                                | [**GetThemeInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint), [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint), [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ Intl    | Lista de enteros                         | Estructura [**Intl**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| \_márgenes TMT    | Márgenes: izquierda, superior, derecha e inferior    | [**Margins**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins) (estructura)   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| \_posición TMT   | Ubicación de un elemento                      | [**Point**](/previous-versions//dd162805(v=vs.85)) (estructura)       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ Rect       | Tamaño y ubicación de un rectángulo         | [**Rect**](/previous-versions//dd162897(v=vs.85)) (estructura)         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| tamaño de TMT \_       | Tamaño de un elemento                          | Estructura de [**tamaño**](/previous-versions//dd145106(v=vs.85))         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| \_cadena TMT     | Cadena de Unicode                           | Matriz **WCHAR**                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>Identificadores de propiedad

A continuación se muestran los valores definidos para las propiedades del tema, agrupadas por tipo de datos.

**TMT \_ bool**



| id                        | Notas                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | **True** si se debe mostrar siempre la barra de tamaño asociada a la parte y el estado.                                                                                                                           |
| AutoSize de TMT \_             | **True** si el área de título no cliente asociada a la parte y el estado varían con el ancho del texto.                                                                                                                 |
| TMT \_ BGFILL               | **True** si las imágenes de tamaño real asociadas a la parte y el estado se van a dibujar en el relleno de fondo.                                                                                                        |
| TMT \_ BORDERONLY           | **True** si la imagen asociada a la parte y el estado solo deben dibujar su borde.                                                                                                                     |
| TMT \_ compuesto           | **True** si el control asociado a la parte y el estado controlarán su propia composición de imágenes.                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| TMT \_ DRAWBORDERS          |                                                                                                                                                                                                                 |
| TMT \_ FLATMENUS            | Vea [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| TMT \_ GLYPHONLY            | **True** si el glifo asociado a la parte y el estado deben dibujarse sin un fondo.                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | **True** si el glifo asociado a la parte y el estado tienen áreas transparentes. Consulte [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) para obtener la definición del valor de TMT \_ GLYPHCOLOR que define el color transparente. |
| TMT \_ INTEGRALSIZING       | **True** si la imagen o el borde truesize asociados a la parte y el estado deben ajustarse a un factor de 2.                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **True** si se debe voltear la imagen asociada a la parte y el estado si la ventana se ve en modo de lectura de derecha a izquierda.                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | **True** si la imagen asociada a la parte y el estado se escalarán más grande en tamaño si es necesario.                                                                                                                |
| TMT \_ SOURCESHRINK         | **True** si la imagen asociada a la parte y el estado se escalarán más pequeños en tamaño si es necesario.                                                                                                               |
| TMT \_ TEXTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| TMT \_ TEXTGLOW             |                                                                                                                                                                                                                 |
| TMT \_ TEXTITALIC           |                                                                                                                                                                                                                 |
| \_transparente TMT          |                                                                                                                                                                                                                 |
| TMT \_ UNIforming        | **True** si la imagen asociada a la parte y el estado deben tener el mismo alto y ancho.                                                                                                                      |
| TMT \_ USERPICTURE          | **True** si la imagen asociada a la parte y el estado se basa en el usuario actual.                                                                                                                          |



 

**COLOR de TMT \_**



| id                           | Notas                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | Color utilizado como sugerencia de color de énfasis para los controles personalizados.                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| Fondo de TMT \_              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | Color utilizado como color de combinación.                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| TMT \_ BORDERCOLOR             | Color del borde asociado a la parte y al estado.                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | Color utilizado como una sugerencia de color de borde para los controles personalizados.                                                                                                                                     |
| TMT \_ BTNFACE                 |                                                                                                                                                                                                |
| TMT \_ BTNHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BTNTEXT                 |                                                                                                                                                                                                |
| TMT \_ BUTTONALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | Color de sombra oscura del borde asociado a esta parte y estado.                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | Color de relleno del borde asociado a esta parte y estado.                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | Color de resaltado del borde asociado a esta parte y estado.                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | Color claro del borde asociado a esta parte y estado.                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | Color de sombra del borde asociado a esta parte y estado.                                                                                                                              |
| \_FILLCOLOR TMT               | Color del relleno de fondo asociado a la parte y al estado.                                                                                                                           |
| TMT \_ FILLCOLORHINT           | Color utilizado como sugerencia de color de relleno para los controles personalizados.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ GLOWCOLOR               | Color del resplandor generado llamando a [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) con esta parte y estado.                                                                                    |
| TMT \_ GLYPHTEXTCOLOR          | Color que utilizará el glifo basado en fuentes asociado a esta parte y el estado.                                                                                                              |
| TMT \_ GLYPHTRANSPARENTCOLOR   | Color del glifo transparente asociado a esta parte y estado. Si el \_ valor de GLYPHTRANSPARENT de TMT para esta parte y el estado es **true**, no se dibujan partes del glifo que usan este color. |
| TMT \_ GRADIENTACTIVECAPTION   |                                                                                                                                                                                                |
| TMT \_ GRADIENTCOLOR1          | Primer color del degradado asociado a esta parte y estado.                                                                                                                           |
| TMT \_ GRADIENTCOLOR2          | Segundo color del degradado.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR3          | Tercer color del degradado.                                                                                                                                                               |
| TMT \_ GRADIENTCOLOR4          | Cuarto color del degradado.                                                                                                                                                              |
| TMT \_ GRADIENTCOLOR5          | Quinto color del degradado.                                                                                                                                                               |
| TMT \_ GRADIENTINACTIVECAPTION |                                                                                                                                                                                                |
| TMT \_ GRAYTEXT                |                                                                                                                                                                                                |
| TMT \_ HEADING1TEXTCOLOR       |                                                                                                                                                                                                |
| TMT \_ HEADING2TEXTCOLOR       |                                                                                                                                                                                                |
| resaltado de TMT \_               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| TMT \_ HOTTRACKING             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ INFOTEXT                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| \_menú TMT                    |                                                                                                                                                                                                |
| \_barra de menús TMT                 |                                                                                                                                                                                                |
| TMT \_ MENUHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| TMT ( \_ barra de desplazamiento)               |                                                                                                                                                                                                |
| TMT \_ SHADOWCOLOR             | Color de la sombra dibujada debajo del texto asociado a esta parte y estado.                                                                                                             |
| TMT \_ TEXTBORDERCOLOR         | Color del borde del texto asociado a esta parte y estado.                                                                                                                              |
| TMT \_ TEXTCOLOR               | Color del texto asociado a esta parte y estado.                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | Color de la sombra de texto asociada a esta parte y estado.                                                                                                                              |
| TMT \_ TRANSPARENTCOLOR        | Color transparente asociado a esta parte y estado. Si el \_ valor transparente TMT para esta parte y el estado es **true**, no se dibujan partes del gráfico que utilizan este color.          |
| ventana de TMT \_                  |                                                                                                                                                                                                |
| TMT \_ WINDOWFRAME             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| id              | Notas |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**\_enumeración TMT**



| Enumeración         | Valores de propiedad                                                                                                                                                                                                                                            | Notas                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE, BT \_ BORDERFILL                                                                                                                                                                                                                              | Tipo de dibujo básico de esta parte.                                                                                                                |
| BORDERTYPE          | BT \_ Rect, BT \_ ROUNDRECT, \_ ELIPSe de BT                                                                                                                                                                                                                       | Tipo de borde dibujado si esta parte es un relleno de borde.                                                                                              |
| CONTENTALIGNMENT    | CA \_ izquierda, \_ centro de CA, CA \_ derecha                                                                                                                                                                                                                            | Alineación del texto en el título asociado a esta parte.                                                                                      |
| FILLTYPE            | FT \_ Solid, ft \_ VERTGRADIENT, ft \_ HORZGRADIENT, FT \_ RADIALGRADIENT, ft \_ TILEIMAGE                                                                                                                                                                           | Tipo de forma de relleno dibujada si esta parte es un relleno de borde.                                                                                          |
| GLYPHTYPE           | GT \_ None, gt \_ IMAGEGLYPH, gt \_ FONTGLYPH                                                                                                                                                                                                                    | El tipo de glifo dibujado en esta parte.                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ None, GFST \_ size, GFST \_ dpi                                                                                                                                                                                                                          | El tipo de método que se usa para seleccionar entre glifos de tamaño diferente.                                                                                    |
| HALIGN              | HA \_ salido, \_ centro de alta disponibilidad, ha \_ derecho                                                                                                                                                                                                                            | La alineación horizontal si esta parte utiliza una imagen de tamaño real.                                                                                        |
| ICONEFFECT          | ICE \_ ninguno, \_ resplandor de hielo, \_ sombra de hielo, \_ pulsos de hielo, hielo \_ alfa                                                                                                                                                                                                  | El tipo de efecto que se va a mostrar cuando se dibuja esta parte mediante [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                             |
| IMAGELAYOUT         | IL \_ vertical, Il \_ horizontal                                                                                                                                                                                                                               | El tipo de alineación que se utiliza cuando se dibujan varias imágenes.                                                                                           |
| IMAGESELECTTYPE     | TSI \_ ninguno, \_ tamaño de TSI, \_ dpi de TSI                                                                                                                                                                                                                             | El tipo de método que se usa para seleccionar entre las imágenes de tamaño de esta parte. Vea el \_ valor de TMT IMAGEFILE1 de [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OFFSETTYPE          | OT \_ de izquierda, OT a la \_ derecha, OT- \_ Middle, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, OT \_ MIDDLERIGHT, OT \_ LEFTOFCAPTION, OT \_ RIGHTOFCAPTION, OT \_ LEFTOFLASTBUTTON, OT \_ RIGHTOFLASTBUTTON, OT \_ ABOVELASTBUTTON, OT \_ BELOWLASTBUTTON | Alineación de esta parte en la ventana.                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE, St \_ Stretch, St \_ Tile, ST \_ TILEHORZ, St \_ TILEVERT, St \_ TILECENTER                                                                                                                                                                            | El método que se usa para ajustar el tamaño de una imagen si esta parte utiliza un archivo de imagen.                                                                                    |
| TEXTSHADOWTYPE      | TST \_ None, TST \_ Single, TST \_ Continuous                                                                                                                                                                                                                    | Tipo de efecto de sombra que se va a dibujar detrás del texto asociado a esta parte.                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ None, TSST \_ size, TSST \_ dpi                                                                                                                                                                                                                          | El tipo de escala que se usa si esta parte utiliza una imagen de tamaño real.                                                                                       |
| VALIGN              | \_parte superior, \_ centro de, va \_ abajo                                                                                                                                                                                                                            | La alineación vertical si esta parte utiliza una imagen de tamaño real.                                                                                          |



 

**\_nombre de archivo TMT**



| id                  | Notas                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYPHIMAGEFILE | Nombre de archivo de la imagen de glifo asociada a esta parte y estado.                                                                        |
| TMT \_ IMAGEFILE      | El nombre de archivo de la imagen asociada a esta parte y el estado, o el nombre de archivo base para varias imágenes asociadas a esta parte y estado. |
| TMT \_ IMAGEFILE1     | Nombre de archivo de la primera imagen escalada asociada a esta parte y el estado, para la compatibilidad con diferentes resoluciones.                            |
| TMT \_ IMAGEFILE2     | Nombre de archivo de la segunda imagen escalada.                                                                                                     |
| TMT \_ IMAGEFILE3     | Nombre de archivo de la tercera imagen escalada.                                                                                                      |
| TMT \_ IMAGEFILE4     | Nombre de archivo de la cuarta imagen escalada.                                                                                                     |
| TMT \_ IMAGEFILE5     | Nombre de archivo de la quinta imagen escalada.                                                                                                      |



 

**\_fuente TMT**



| id                    | Notas                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| TMT \_ GLYPHFONT        | La fuente con la que se dibujará el glifo asociado a esta parte, si se utilizan glifos basados en fuentes. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| TMT \_ ICONTITLEFONT    |                                                                                                      |
| TMT \_ MENUFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| TMT \_ STATUSFONT       |                                                                                                      |



 

**TMT \_ int**



| id                       | Notas                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | Valor alfa (0-255) que se usa para [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | Valor alfa mínimo (0-255) que debe tener un píxel para que se considere opaco.                                                                                                                                  |
| TMT \_ ANIMATIONDELAY      |                                                                                                                                                                                                                  |
| TMT \_ ANIMATIONDURATION   |                                                                                                                                                                                                                  |
| TMT \_ borde          | Grosor del borde dibujado si esta parte utiliza un relleno de borde.                                                                                                                                               |
| \_juego de caracteres TMT             |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONCOLOR   |                                                                                                                                                                                                                  |
| TMT \_ COLORIZATIONOPACITY |                                                                                                                                                                                                                  |
| TMT \_ FRAMESPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT \_ GLOWINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | Índice de carácter de la fuente seleccionada que se usará para el glifo, si el elemento utiliza un glifo basado en fuentes.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | La cantidad del primer color de degradado (TMT \_ GRADIENTCOLOR1) que se va a usar para dibujar el elemento. Este valor puede estar comprendido entre 0 y 255, pero este valor más los valores de cada uno de los valores de GRADIENTRATIO deben agregar hasta 255. |
| TMT \_ GRADIENTRATIO2      | La cantidad del segundo color de degradado (TMT \_ GRADIENTCOLOR2) que se va a usar para dibujar el elemento.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | La cantidad del tercer color de degradado (TMT \_ GRADIENTCOLOR3) que se va a usar para dibujar el elemento.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | Cantidad del cuarto color de degradado (TMT \_ GRADIENTCOLOR4) que se va a usar para dibujar el elemento.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | Cantidad del quinto color de degradado (TMT \_ GRADIENTCOLOR5) que se va a usar para dibujar el elemento.                                                                                                                         |
| alto de TMT \_              | Alto del elemento.                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | El número de imágenes de estado presentes en un archivo de imagen.                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | Los puntos por pulgada (PPP) mínimos para los que se diseñó el primer archivo de imagen.                                                                                                                                      |
| TMT \_ MINDPI2             | El valor mínimo de PPP para el que se diseñó el segundo archivo de imagen.                                                                                                                                                     |
| TMT \_ MINDPI3             | El valor mínimo de PPP para el que se diseñó el tercer archivo de imagen.                                                                                                                                                      |
| TMT \_ MINDPI4             | El valor mínimo de PPP para el que se diseñó el cuarto archivo de imagen.                                                                                                                                                     |
| TMT \_ MINDPI5             | El valor mínimo de PPP para el que se diseñó el quinto archivo de imagen.                                                                                                                                                      |
| \_opacidad TMT             |                                                                                                                                                                                                                  |
| TMT \_ PIXELSPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | Tamaño de las formas de control de progreso que definen hasta qué punto ha progresado una operación.                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | El tamaño total de todos los "fragmentos" del control de progreso.                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | La redondez (del 0 al 100 por ciento) de las esquinas del elemento.                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | La redondez (del 0 al 100 por ciento) de las esquinas del elemento.                                                                                                                                                          |
| saturación de TMT \_          | La cantidad de saturación (0-255) que se aplicará a un icono dibujado mediante [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                         |
| TMT \_ TEXTBORDERSIZE      | Grosor del borde dibujado alrededor de los caracteres de texto.                                                                                                                                                        |
| TMT \_ TEXTGLOWSIZE        |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR1            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR2            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR3            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR4            |                                                                                                                                                                                                                  |
| TMT \_ TOCOLOR5            |                                                                                                                                                                                                                  |
| TMT \_ TOHUE1              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE2              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE3              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE4              |                                                                                                                                                                                                                  |
| TMT \_ TOHUE5              |                                                                                                                                                                                                                  |
| TMT \_ TRUESIZESTRETCHMARK | Porcentaje de tamaño original de una imagen de tamaño real en el que se ajustará la imagen.                                                                                                                        |
| ancho de TMT \_               | Ancho del elemento.                                                                                                                                                                                           |



 

**TMT \_ Intl**



| id                       | Notas |
|--------------------------|-------|
| TMT \_ TRANSITIONDURATIONS |       |



 

**\_márgenes TMT**



| id                  | Notas                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | Los márgenes que definen dónde se puede colocar el texto de la leyenda dentro de un elemento. |
| TMT \_ CONTENTMARGINS | Los márgenes que definen dónde se puede colocar el contenido dentro de un elemento.      |
| TMT \_ SIZINGMARGINS  | Los márgenes usados para ajustar el tamaño de una imagen que no es de tamaño verdadero.                      |



 

**\_posición TMT**



| id                    | Notas                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MinSize          | El tamaño mínimo que puede usar el archivo de imagen normal antes de pasar al siguiente archivo de imagen más pequeño.   |
| TMT \_ MINSIZE1         | El tamaño mínimo para el que se puede usar el primer archivo de imagen pequeño.                                            |
| TMT \_ MINSIZE2         | El tamaño mínimo para el que se puede usar el segundo archivo de imagen pequeño.                                           |
| TMT \_ MINSIZE3         | El tamaño mínimo para el que se puede usar el tercer archivo de imagen pequeño.                                            |
| TMT \_ MINSIZE4         | El tamaño mínimo para el que se puede usar el cuarto archivo de imagen pequeño.                                           |
| TMT \_ MINSIZE5         | El tamaño mínimo para el que se puede usar el quinto archivo de imagen pequeño.                                            |
| TMT \_ NORMALSIZE       | Tamaño de la imagen normal asociada a esta parte.                                                      |
| \_desplazamiento TMT           | Desplazamiento de posición de la alineación de esta parte. La alineación se define mediante el valor de OFFSETTYPE de TMT \_ . |
| TMT \_ TEXTSHADOWOFFSET | Desplazamiento del texto en el que se dibujan las sombras del texto.                                                    |



 

**TMT \_ Rect**



| id                       | Notas                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| TMT \_ CUSTOMSPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | Tamaño predeterminado del elemento. |



 

**tamaño de TMT \_**



| id                      | Notas                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | Alto de la barra de título.       |
| TMT \_ CAPTIONBARWIDTH    | Ancho de la barra de título.        |
| TMT \_ MENUBARHEIGHT      | Alto de la barra de menús.          |
| TMT \_ MENUBARWIDTH       | Ancho de la barra de menús.           |
| TMT \_ PADDEDBORDERWIDTH  | Ancho de borde rellenado.      |
| TMT \_ SCROLLBARHEIGHT    | Alto de la barra de desplazamiento.        |
| TMT \_ SCROLLBARWIDTH     | Ancho de la barra de desplazamiento.         |
| TMT \_ SIZINGBORDERWIDTH  | Ancho de un borde de ajuste de tamaño. |
| TMT \_ SMCAPTIONBARHEIGHT | Alto de la barra de título.       |
| TMT \_ SMCAPTIONBARWIDTH  | Ancho de la barra de título.        |



 

**\_cadena TMT**



| id                   | Notas                                               |
|----------------------|-----------------------------------------------------|
| \_alias TMT           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| autor de TMT \_          |                                                     |
| TMT \_ CLASSICVALUE    |                                                     |
| TMT \_ COLORSCHEMES    |                                                     |
| \_empresa TMT         |                                                     |
| COPYRIGHT de TMT \_       |                                                     |
| TMT \_ CSSNAME         | Vea [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| Descripción de TMT \_     |                                                     |
| TMT \_ DISPLAYNAME     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| tamaños de TMT \_           |                                                     |
| \_texto TMT            | Texto que muestra el elemento.                     |
| \_información sobre herramientas de TMT         |                                                     |
| \_dirección URL de TMT             |                                                     |
| versión de TMT \_         |                                                     |
| TMT \_ XMLNAME         | Vea [**GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring). |
| nombre de TMT \_            |                                                     |



 

 

 
