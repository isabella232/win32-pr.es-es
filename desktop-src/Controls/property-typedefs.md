---
title: Identificadores de propiedad (Windows controles)
description: Este tema contiene información sobre los valores definidos que se usan para recuperar propiedades de estilos visuales. Las definiciones se encuentran en Vssym32.h.
ms.assetid: b0e22022-fea9-43d1-8ef0-7a1c518760f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0869ac80332a5dbdb146ee255f5c9e73f4a812
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167606"
---
# <a name="property-identifiers-windows-controls"></a>Identificadores de propiedad (Windows controles)

Este tema contiene información sobre los valores definidos que se usan para recuperar propiedades de estilos visuales. Las definiciones se encuentran en Vssym32.h.

## <a name="property-types"></a>Tipos de propiedades

En la tabla siguiente se enumeran los tipos de propiedad primitivos. Las aplicaciones no suelen usar los valores de la primera columna, sino que proporcionan un medio para clasificar los identificadores de propiedad.



| Tipo de datos       | Descripción                              | Tipo devuelto                          | Función de recuperación                                                                                                     |
|-----------------|------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| TMT \_ BOOL       | **TRUE** o **FALSE**                    | Boolean                                | [**GetThemeBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebool), [ **GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool)                                       |
| TMT \_ COLOR      | Valor de color RGB                          | [**Estructura COLORREF**](/windows/desktop/gdi/colorref) | [**GetThemeColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor), [ **GetThemeSysColor**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesyscolor)                                   |
| TMT \_ DISKSTREAM | Secuencia de disco                              | **HINSTANCE**                          | [**GetThemeStream**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestream)                                                                               |
| TMT \_ ENUM       | Valor enumerado                         | Enumeración                            | [**GetThemeEnumValue**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeenumvalue).                                                                        |
| NOMBRE DE ARCHIVO TMT \_   | Nombre de archivo relativo al directorio del tema | **Matriz WCHAR**                        | [**GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename)                                                                           |
| FUENTE \_ TMT       | Descripción de fuente                         | [**Estructura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)   | [**GetThemeFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefont), [ **GetThemeSysFont**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysfont)                                       |
| TMT \_ HBITMAP    | Bitmap                                   | **Identificador HBITMAP**                     | [**GetThemeBitmap**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemebitmap)                                                                               |
| TMT \_ INT        | Número firmado                            | Entero                                | [**GetThemeInt,**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeint) [**GetThemeSysInt**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysint), [**GetThemeMetric**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememetric) |
| TMT \_ INTLIST    | Lista de enteros                         | [**INTLIST (estructura)**](/windows/desktop/api/UxTheme/ns-uxtheme-intlist)   | [**GetThemeIntList**](/windows/desktop/api/UxTheme/nf-uxtheme-getthemeintlist)                                                                             |
| MÁRGENES DE TMT \_    | Márgenes: izquierda, superior, derecha e inferior    | [**Estructura MARGINS**](/windows/desktop/api/Uxtheme/ns-uxtheme-margins)   | [**GetThemeMargins**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthememargins)                                                                             |
| TMT \_ POSITION   | Ubicación de un elemento                      | [**Point (estructura)**](/previous-versions//dd162805(v=vs.85))       | [**GetThemePosition**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemeposition)                                                                           |
| TMT \_ RECT       | Tamaño y ubicación de un rectángulo         | [**Rect (estructura)**](/previous-versions//dd162897(v=vs.85))         | [**GetThemeRect**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemerect)                                                                                   |
| TMT \_ SIZE       | Tamaño de un elemento                          | [**Estructura SIZE**](/previous-versions//dd145106(v=vs.85))         | [**GetThemePartSize**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemepartsize)                                                                           |
| TMT \_ STRING     | Cadena de Unicode                           | **Matriz WCHAR**                        | [**GetThemeString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemestring), [ **GetThemeSysString**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring)                               |



 

## <a name="property-ids"></a>Identificadores de propiedad

Estos son los valores definidos para las propiedades de tema, agrupados por tipo de datos.

**TMT \_ BOOL**



| id                        | Notas                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALWAYSSHOWSIZINGBAR  | **TRUE** si siempre se debe mostrar la barra de tamaño asociada a la parte y el estado.                                                                                                                           |
| TMT \_ AUTOSIZE             | **TRUE** si el área de título no cliente asociada a la parte y el estado varía con el ancho del texto.                                                                                                                 |
| TMT \_ BGFILL               | **TRUE** si las imágenes de tamaño verdadero asociadas a la parte y el estado se van a dibujar en el relleno de fondo.                                                                                                        |
| TMT \_ BORDERONLY           | **TRUE** si la imagen asociada a la parte y el estado solo debe tener dibujado su borde.                                                                                                                     |
| TMT \_ COMPOSITED           | **TRUE** si el control asociado con el elemento y el estado controlará su propia composición de imágenes.                                                                                                           |
| TMT \_ COMPOSITEDOPAQUE     |                                                                                                                                                                                                                 |
| DRAWBORDERS DE TMT \_          |                                                                                                                                                                                                                 |
| TMT \_ FLATMENUS            | Vea [**GetThemeSysBool**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysbool).                                                                                                                                                                 |
| GLIFO \_ DE TMT            | **TRUE** si el glifo asociado a la parte y el estado se debe dibujar sin fondo.                                                                                                                  |
| TMT \_ GLYPHTRANSPARENT     | **TRUE** si el glifo asociado a la parte y el estado tiene áreas transparentes. Vea [**GetThemeColor para**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemecolor) obtener la definición del valor de GLYPHCOLOR de TMT \_ que define el color transparente. |
| TMT \_ INTEGRALSIZING       | **TRUE** si la imagen truesize o el borde asociado con la parte y el estado deben tener un tamaño de 2.                                                                                                     |
| TMT \_ LOCALIZEDMIRRORIMAGE |                                                                                                                                                                                                                 |
| TMT \_ MIRRORIMAGE          | **TRUE** si la imagen asociada a la parte y el estado se debe voltear si la ventana se está visualizando en modo de lectura de derecha a izquierda.                                                                         |
| TMT \_ NOETCHEDEFFECT       |                                                                                                                                                                                                                 |
| TMT \_ SCALEDBACKGROUND     |                                                                                                                                                                                                                 |
| TMT \_ SOURCEGROW           | **TRUE** si la imagen asociada con el elemento y el estado escalará un tamaño mayor si es necesario.                                                                                                                |
| TMT \_ SOURCESHRINK         | **TRUE** si la imagen asociada con el elemento y el estado escalará un tamaño menor si es necesario.                                                                                                               |
| TMT \_ TEXTAPPLYOVERLAY     |                                                                                                                                                                                                                 |
| TMT \_ TEXTGLOW             |                                                                                                                                                                                                                 |
| TMT \_ TEXTITALIC           |                                                                                                                                                                                                                 |
| TMT \_ TRANSPARENTE          |                                                                                                                                                                                                                 |
| TMT \_ UNIFORMSIZING        | **TRUE** si la imagen asociada al elemento y al estado debe tener el mismo alto y ancho.                                                                                                                      |
| TMT \_ USERPICTURE          | **TRUE** si la imagen asociada al elemento y el estado se basa en el usuario actual.                                                                                                                          |



 

**TMT \_ COLOR**



| id                           | Notas                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ACCENTCOLORHINT         | Color que se usa como sugerencia de color de acento para controles personalizados.                                                                                                                                    |
| TMT \_ ACTIVEBORDER            |                                                                                                                                                                                                |
| TMT \_ ACTIVECAPTION           |                                                                                                                                                                                                |
| TMT \_ APPWORKSPACE            |                                                                                                                                                                                                |
| TMT \_ BACKGROUND              |                                                                                                                                                                                                |
| TMT \_ BLENDCOLOR              | Color que se usa como color de mezcla.                                                                                                                                                               |
| TMT \_ BODYTEXTCOLOR           |                                                                                                                                                                                                |
| TMT \_ BORDERCOLOR             | Color del borde asociado con la parte y el estado.                                                                                                                                    |
| TMT \_ BORDERCOLORHINT         | Color utilizado como sugerencia de color de borde para controles personalizados.                                                                                                                                     |
| TMT \_ BTNFACE                 |                                                                                                                                                                                                |
| TMT \_ BTIGHIGHLIGHT            |                                                                                                                                                                                                |
| TMT \_ BTNSHADOW               |                                                                                                                                                                                                |
| TMT \_ BTNTEXT                 |                                                                                                                                                                                                |
| TMT \_ BUTTONALTERNATEFACE     |                                                                                                                                                                                                |
| TMT \_ CAPTIONTEXT             |                                                                                                                                                                                                |
| TMT \_ DKSHADOW3D              |                                                                                                                                                                                                |
| TMT \_ EDGEDKSHADOWCOLOR       | Color de sombra oscuro del borde asociado a esta parte y estado.                                                                                                                         |
| TMT \_ EDGEFILLCOLOR           | Color de relleno del borde asociado a esta parte y estado.                                                                                                                                |
| TMT \_ EDGEHIGHLIGHTCOLOR      | Color de resaltado del borde asociado a esta parte y estado.                                                                                                                           |
| TMT \_ EDGELIGHTCOLOR          | Color claro del borde asociado a esta parte y estado.                                                                                                                               |
| TMT \_ EDGESHADOWCOLOR         | Color de sombra del borde asociado a esta parte y estado.                                                                                                                              |
| TMT \_ FILLCOLOR               | Color del relleno de fondo asociado con la parte y el estado.                                                                                                                           |
| TMT \_ FILLCOLORHINT           | Color que se usa como sugerencia de color de relleno para controles personalizados.                                                                                                                                       |
| TMT \_ FROMCOLOR1              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR2              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR3              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR4              |                                                                                                                                                                                                |
| TMT \_ FROMCOLOR5              |                                                                                                                                                                                                |
| TMT \_ GLOWCOLOR               | Color del efecto de efecto de iluminado generado al llamar [**a DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon) con esta parte y el estado.                                                                                    |
| GLIFO DE \_ TMTTEXTCOLOR          | Color que usará el glifo basado en fuente asociado a esta parte y estado.                                                                                                              |
| GLIFO DE \_ TMTTRANSPARENTCOLOR   | Color del glifo transparente asociado a esta parte y estado. Si el valor de GLYPHTRANSPARENT de TMT para esta parte y el estado es TRUE, las partes del glifo que usan este \_ color no se dibujan.  |
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
| TMT \_ HIGHLIGHT               |                                                                                                                                                                                                |
| TMT \_ HIGHLIGHTTEXT           |                                                                                                                                                                                                |
| SEGUIMIENTO \_ DE TMT             |                                                                                                                                                                                                |
| TMT \_ INACTIVEBORDER          |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTION         |                                                                                                                                                                                                |
| TMT \_ INACTIVECAPTIONTEXT     |                                                                                                                                                                                                |
| TMT \_ INFOBK                  |                                                                                                                                                                                                |
| TMT \_ INFOTEXT                |                                                                                                                                                                                                |
| TMT \_ LIGHT3D                 |                                                                                                                                                                                                |
| MENÚ \_ TMT                    |                                                                                                                                                                                                |
| BARRA DE MENÚS DE TMT \_                 |                                                                                                                                                                                                |
| MENÚ \_ DE TMTHILIGHT             |                                                                                                                                                                                                |
| TMT \_ MENUTEXT                |                                                                                                                                                                                                |
| BARRA DE DESPLAZAMIENTO DE TMT \_               |                                                                                                                                                                                                |
| TMT \_ SHADOWCOLOR             | Color de la sombra dibujada debajo del texto asociado a esta parte y estado.                                                                                                             |
| TMT \_ TEXTBORDERCOLOR         | Color del borde de texto asociado a esta parte y estado.                                                                                                                              |
| TMT \_ TEXTCOLOR               | Color del texto asociado a esta parte y estado.                                                                                                                                     |
| TMT \_ TEXTCOLORHINT           |                                                                                                                                                                                                |
| TMT \_ TEXTSHADOWCOLOR         | Color de la sombra de texto asociada a esta parte y estado.                                                                                                                              |
| TMT \_ TRANSPARENTCOLOR        | Color transparente asociado a esta parte y estado. Si el valor TRANSPARENTE de TMT para esta parte y el estado es TRUE, las partes del gráfico que usan este \_ color no se dibujan.           |
| VENTANA \_ TMT                  |                                                                                                                                                                                                |
| WINDOWFRAME de TMT \_             |                                                                                                                                                                                                |
| TMT \_ WINDOWTEXT              |                                                                                                                                                                                                |



 

**TMT \_ DISKSTREAM**



| id              | Notas |
|-----------------|-------|
| TMT \_ ATLASIMAGE |       |



 

**TMT \_ ENUM**



| Enumeración         | Valores de propiedad                                                                                                                                                                                                                                            | Notas                                                                                                                                                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| BGTYPE              | BT \_ IMAGEFILE, BT \_ BORDERFILL                                                                                                                                                                                                                              | Tipo de dibujo básico para esta parte.                                                                                                                |
| BORDERTYPE          | BT \_ RECT, BT \_ ROUNDRECT, BT \_ ELLIPSE                                                                                                                                                                                                                       | Tipo de borde dibujado si esta parte es un relleno de borde.                                                                                              |
| CONTENTALIGNMENT    | CA \_ LEFT, CA \_ CENTER, CA \_ RIGHT                                                                                                                                                                                                                            | Alineación del texto del título asociado a esta parte.                                                                                      |
| FILLTYPE            | FT \_ SOLID, FT \_ VERTGRADIENT, FT \_ HORZGRADIENT, FT \_ RADIALGRADIENT, FT \_ TILEIMAGE                                                                                                                                                                           | Tipo de forma de relleno dibujada si esta parte es un relleno de borde.                                                                                          |
| GLYPHTYPE           | GT \_ NONE, GT \_ IMAGEGLYPH, GT \_ FONTGLYPH                                                                                                                                                                                                                    | Tipo de glifo dibujado en esta parte.                                                                                                                |
| GLYPHFONTSIZINGTYPE | GFST \_ NONE, GFST \_ SIZE, GFST \_ PPP                                                                                                                                                                                                                          | Tipo de método que se usa para seleccionar entre glifos de distinto tamaño.                                                                                    |
| IGN              | HA \_ LEFT, HA \_ CENTER, HA \_ RIGHT                                                                                                                                                                                                                            | Alineación horizontal si esta parte usa una imagen de tamaño real.                                                                                        |
| ICONEFFECT          | ICE \_ NONE, ICE \_ GLOW, ICE \_ SHADOW, ICE \_ PULSE, ICE \_ ALPHA                                                                                                                                                                                                  | Tipo de efecto que se mostrará cuando se dibuje esta parte [**mediante DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                             |
| IMAGELAYOUT         | IL \_ VERTICAL, IL \_ HORIZONTAL                                                                                                                                                                                                                               | Tipo de alineación utilizado cuando se dibujan varias imágenes.                                                                                           |
| IMAGESELECTTYPE     | IST \_ NONE, IST \_ SIZE, IST \_ PPP                                                                                                                                                                                                                             | Tipo de método que se usa para seleccionar entre imágenes de tamaño para esta parte. Vea el valor IMAGEFILE1 de TMT \_ [**de GetThemeFilename**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemefilename). |
| OFFSETTYPE          | OT \_ TOPLEFT, OT \_ TOPRIGHT, OT \_ TOPMIDDLE, OT \_ BOTTOMLEFT, OT \_ BOTTOMRIGHT, OT \_ BOTTOMMIDDLE, OT \_ MIDDLELEFT, OT \_ MIDDLERIGHT, OT \_ LEFTOFCAPTION, OT \_ RIGHTOFCAPTION, OT \_ LEFTOFLASTBUTTON, OT \_ RIGHTOFLASTBUTTON, OT \_ ABOVELASTBUTTON, OT \_ BELOWLASTBUTTON | Alineación de esta parte en la ventana.                                                                                                            |
| SIZINGTYPE          | ST \_ TRUESIZE, ST \_ STRETCH, ST \_ TILE, ST \_ TILEHORZ, ST \_ TILEVERT, ST \_ TILECENTER                                                                                                                                                                            | Método que se usa para cambiar el tamaño de una imagen si esta parte usa un archivo de imagen.                                                                                    |
| TEXTSHADOWTYPE      | TST \_ NONE, TST \_ SINGLE, TST \_ CONTINUOUS                                                                                                                                                                                                                    | Tipo de efecto de sombra que se va a dibujar detrás del texto asociado a esta parte.                                                                             |
| TRUESIZESCALINGTYPE | TSST \_ NONE, TSST \_ SIZE, TSST \_ PPP                                                                                                                                                                                                                          | Tipo de escalado que se usa si esta parte usa una imagen de tamaño real.                                                                                       |
| VALIGN              | VA \_ TOP, VA \_ CENTER, VA \_ BOTTOM                                                                                                                                                                                                                            | Alineación vertical si esta parte usa una imagen de tamaño real.                                                                                          |



 

**NOMBRE DE ARCHIVO DE TMT \_**



| id                  | Notas                                                                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ GLYPHIMAGEFILE | Nombre de archivo de la imagen de glifo asociada a esta parte y estado.                                                                        |
| TMT \_ IMAGEFILE      | Nombre de archivo de la imagen asociada a este elemento y estado, o el nombre de archivo base para varias imágenes asociadas a esta parte y estado. |
| TMT \_ IMAGEFILE1     | Nombre de archivo de la primera imagen a escala asociada a esta parte y estado, para admitir diferentes resoluciones.                            |
| TMT \_ IMAGEFILE2     | Nombre de archivo de la segunda imagen escalada.                                                                                                     |
| TMT \_ IMAGEFILE3     | Nombre de archivo de la tercera imagen escalada.                                                                                                      |
| TMT \_ IMAGEFILE4     | Nombre de archivo de la cuarta imagen escalada.                                                                                                     |
| TMT \_ IMAGEFILE5     | Nombre de archivo de la quinta imagen escalada.                                                                                                      |



 

**FUENTE \_ TMT**



| id                    | Notas                                                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------|
| TMT \_ BODYFONT         |                                                                                                      |
| TMT \_ CAPTIONFONT      |                                                                                                      |
| TMT \_ GLYPHFONT        | Fuente con la que se dibujará el glifo asociado a esta parte, si se usan glifos basados en fuentes. |
| TMT \_ HEADING1FONT     |                                                                                                      |
| TMT \_ HEADING2FONT     |                                                                                                      |
| ICONO DE \_ TMTTITLEFONT    |                                                                                                      |
| TMT \_ MENUFONT         |                                                                                                      |
| TMT \_ MSGBOXFONT       |                                                                                                      |
| TMT \_ SMALLCAPTIONFONT |                                                                                                      |
| TMT \_ STATUSFONT       |                                                                                                      |



 

**TMT \_ INT**



| id                       | Notas                                                                                                                                                                                                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TMT \_ ALPHALEVEL          | Valor alfa (0-255) utilizado para [**DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                                                         |
| TMT \_ ALPHATHRESHOLD      | Valor alfa mínimo (0-255) que un píxel debe considerarse opaco.                                                                                                                                  |
| TMT \_ ANIMATIONDELAY      |                                                                                                                                                                                                                  |
| TMT \_ ANIMATIONDURATION   |                                                                                                                                                                                                                  |
| TMT \_ BORDERSIZE          | Grosor del borde dibujado si esta parte usa un relleno de borde.                                                                                                                                               |
| TMT \_ CHARSET             |                                                                                                                                                                                                                  |
| COLORIZATIONCOLOR de TMT \_   |                                                                                                                                                                                                                  |
| \_COLORIZATIONOPACITY de TMT |                                                                                                                                                                                                                  |
| FOTOGRAMAS \_ TMTPERSECOND     |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE1            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE2            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE3            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE4            |                                                                                                                                                                                                                  |
| TMT \_ FROMHUE5            |                                                                                                                                                                                                                  |
| TMT \_ GLOWINTENSITY       |                                                                                                                                                                                                                  |
| TMT \_ GLYPHINDEX          | Índice de caracteres en la fuente seleccionada que se usará para el glifo, si la parte usa un glifo basado en fuentes.                                                                                                 |
| TMT \_ GRADIENTRATIO1      | Cantidad del primer color de degradado (TMT \_ GRADIENTCOLOR1) que se usará al dibujar la parte. Este valor puede ser de 0 a 255, pero este valor más los valores de cada uno de los valores GRADIENTRATIO deben sumar hasta 255. |
| TMT \_ GRADIENTRATIO2      | Cantidad del segundo color de degradado (TMT \_ GRADIENTCOLOR2) que se usará al dibujar la parte.                                                                                                                        |
| TMT \_ GRADIENTRATIO3      | Cantidad del tercer color de degradado (TMT \_ GRADIENTCOLOR3) que se usará al dibujar la parte.                                                                                                                         |
| TMT \_ GRADIENTRATIO4      | Cantidad del cuarto color de degradado (TMT \_ GRADIENTCOLOR4) que se usará al dibujar la parte.                                                                                                                        |
| TMT \_ GRADIENTRATIO5      | Cantidad del quinto color de degradado (TMT \_ GRADIENTCOLOR5) que se usará al dibujar la parte.                                                                                                                         |
| TMT \_ HEIGHT              | Alto de la parte.                                                                                                                                                                                          |
| TMT \_ IMAGECOUNT          | Número de imágenes de estado presentes en un archivo de imagen.                                                                                                                                                             |
| TMT \_ MINCOLORDEPTH       |                                                                                                                                                                                                                  |
| TMT \_ MINDPI1             | Los puntos mínimos por pulgada (ppp) para los que se diseñó el primer archivo de imagen.                                                                                                                                      |
| TMT \_ MINDPI2             | Ppp mínimo para el que se diseñó el segundo archivo de imagen.                                                                                                                                                     |
| TMT \_ MINDPI3             | Ppp mínimo para el que se diseñó el tercer archivo de imagen.                                                                                                                                                      |
| TMT \_ MINDPI4             | Ppp mínimo para el que se diseñó el cuarto archivo de imagen.                                                                                                                                                     |
| TMT \_ MINDPI5             | Ppp mínimo para el que se diseñó el quinto archivo de imagen.                                                                                                                                                      |
| OPACIDAD DE TMT \_             |                                                                                                                                                                                                                  |
| TMT \_ PIXELSPERFRAME      |                                                                                                                                                                                                                  |
| TMT \_ PROGRESSCHUNKSIZE   | El tamaño de las formas de "fragmento" del control de progreso que definen hasta qué punto ha progresado una operación.                                                                                                                 |
| TMT \_ PROGRESSSPACESIZE   | Tamaño total de todos los "fragmentos" del control de progreso.                                                                                                                                                          |
| TMT \_ ROUNDCORNERHEIGHT   | Redondeo (del 0 al 100 por ciento) de las esquinas de la parte.                                                                                                                                                          |
| TMT \_ ROUNDCORNERWIDTH    | Redondeo (del 0 al 100 por ciento) de las esquinas de la parte.                                                                                                                                                          |
| SATURACIÓN DE TMT \_          | Cantidad de saturación (0-255) que se aplicará a un icono dibujado [**mediante DrawThemeIcon**](/windows/desktop/api/Uxtheme/nf-uxtheme-drawthemeicon).                                                                                                         |
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
| TMT \_ TRUESIZESTRETCHMARK | Porcentaje del tamaño original de una imagen de tamaño verdadero en el que se va a extender la imagen.                                                                                                                        |
| TMT \_ WIDTH               | Ancho de la parte.                                                                                                                                                                                           |



 

**TMT \_ INTLIST**



| id                       | Notas |
|--------------------------|-------|
| TRANSICIONES \_ DE TMTDURATIONS |       |



 

**MÁRGENES DE TMT \_**



| id                  | Notas                                                                   |
|---------------------|-------------------------------------------------------------------------|
| TMT \_ CAPTIONMARGINS | Márgenes que definen dónde se puede colocar el texto del título dentro de una parte. |
| TMT \_ CONTENTMARGINS | Márgenes que definen dónde se puede colocar el contenido dentro de una parte.      |
| TMT \_ SIZINGMARGINS  | Márgenes usados para dimensionar una imagen de tamaño no verdadero.                      |



 

**TMT \_ POSITION**



| id                    | Notas                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------|
| TMT \_ MINSIZE          | Tamaño mínimo para el que se puede usar el archivo de imagen normal antes de pasar al siguiente archivo de imagen más pequeño.   |
| TMT \_ MINSIZE1         | Tamaño mínimo para el que se puede usar el primer archivo de imagen pequeño.                                            |
| TMT \_ MINSIZE2         | Tamaño mínimo para el que se puede usar el segundo archivo de imagen pequeño.                                           |
| TMT \_ MINSIZE3         | Tamaño mínimo para el que se puede usar el tercer archivo de imagen pequeño.                                            |
| TMT \_ MINSIZE4         | Tamaño mínimo para el que se puede usar el cuarto archivo de imagen pequeño.                                           |
| TMT \_ MINSIZE5         | Tamaño mínimo para el que se puede usar el quinto archivo de imagen pequeño.                                            |
| TMT \_ NORMALSIZE       | Tamaño de la imagen normal asociada a esta parte.                                                      |
| DESPLAZAMIENTO \_ DE TMT           | Desplazamiento de posición de la alineación de esta parte. La alineación se define mediante el valor \_ OFFSETTYPE de TMT. |
| TMT \_ TEXTSHADOWOFFSET | Desplazamiento del texto en el que se dibujan las sombras de texto.                                                    |



 

**TMT \_ RECT**



| id                       | Notas                         |
|--------------------------|-------------------------------|
| TMT \_ ANIMATIONBUTTONRECT |                               |
| TMT \_ ATLASRECT           |                               |
| TMT \_ SEPLITRECT     |                               |
| TMT \_ DEFAULTPANESIZE     | Tamaño predeterminado del elemento. |



 

**TMT \_ SIZE**



| id                      | Notas                     |
|-------------------------|---------------------------|
| TMT \_ CAPTIONBARHEIGHT   | Alto de la barra de título.       |
| TMT \_ CAPTIONBARWIDTH    | Ancho de la barra de título.        |
| MENÚ \_ TMTBARHEIGHT      | Alto de la barra de menús.          |
| MENÚ \_ TMTBARWIDTH       | Ancho de la barra de menús.           |
| TMT \_ PADDEDBORDERWIDTH  | Ancho de borde acolchado.      |
| TMT \_ SCROLLBARHEIGHT    | Alto de la barra de desplazamiento.        |
| TMT \_ SCROLLBARWIDTH     | Ancho de la barra de desplazamiento.         |
| TMT \_ SIZINGBORDERWIDTH  | Ancho de un borde de tamaño. |
| TMT \_ SMCAPTIONBARHEIGHT | Alto de la barra de título.       |
| TMT \_ SMCAPTIONBARWIDTH  | Ancho de la barra de título.        |



 

**TMT \_ STRING**



| id                   | Notas                                               |
|----------------------|-----------------------------------------------------|
| TMT \_ ALIAS           |                                                     |
| TMT \_ ATLASINPUTIMAGE |                                                     |
| TMT \_ AUTHOR          |                                                     |
| TMT \_ CLASSICVALUE    |                                                     |
| TMT \_ COLORSCHEMES    |                                                     |
| TMT \_ COMPANY         |                                                     |
| TMT \_ COPYRIGHT       |                                                     |
| TMT \_ CSSNAME         | Vea [**GetThemeSysString.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring) |
| DESCRIPCIÓN \_ DE TMT     |                                                     |
| TMT \_ DISPLAYNAME     |                                                     |
| TMT \_ LASTUPDATED     |                                                     |
| TAMAÑOS \_ DE TMT           |                                                     |
| TEXTO \_ TMT            | Texto que muestra el elemento.                     |
| INFORMACIÓN SOBRE HERRAMIENTAS DE TMT \_         |                                                     |
| Dirección URL de TMT \_             |                                                     |
| VERSIÓN DE \_ TMT         |                                                     |
| TMT \_ XMLNAME         | Vea [**GetThemeSysString.**](/windows/desktop/api/Uxtheme/nf-uxtheme-getthemesysstring) |
| NOMBRE \_ DE TMT            |                                                     |



 

 

 
