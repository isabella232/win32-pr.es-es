---
title: Selector de colores de Drop-Down
description: El marco de la cinta de opciones de Windows proporciona un control de selector de colores Drop-Down especializado que expone una variedad de valores de color a través de un botón de expansión y del selector de colores desplegables personalizables.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104421514"
---
# <a name="drop-down-color-picker"></a>Selector de colores de Drop-Down

El marco de la cinta de opciones de Windows proporciona un control de selector de colores Drop-Down especializado que expone una variedad de valores de color a través de un botón de expansión y del selector de colores desplegables personalizables.

-   [Introducción](#introduction)
-   [marcado](#markup)
-   [Código](#code)
    -   [Propiedades](#properties)
    -   [Controladores de comandos](#command-handlers)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Mediante la emulación de la apariencia y la funcionalidad de la Microsoft Office selector de color, el marco de la cinta de opciones puede beneficiarse de la coherencia y la familiaridad en una amplia gama de aplicaciones.

## <a name="markup"></a>marcado

Al igual que todos los controles de la cinta de opciones, el selector de colores Drop-Down se implementa y personaliza fácilmente mediante marcado. El marco de trabajo proporciona una serie de atributos de elemento para que el selector de colores de Drop-Down exponga varios niveles de funcionalidad. En la tabla siguiente se enumeran los atributos del selector de colores de Drop-Down.



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
<td>ColorTemplate</td>
<td>Plantillas de diseño que especifican el tipo de Drop-Down selector de colores.<br/> Hay tres plantillas, cada una de las cuales especifica un diseño de control y valores predeterminados para los atributos y las claves de propiedad asociados. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>Chip</td>
<td>Tamaño de cada chip de color (o muestra).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Columnas</td>
<td>El número de columnas de chip de color (o muestra).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Nombre de la declaración de comando asociada. <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>Muestra u oculta el botón <strong>automático</strong> .<br/> Válido solo cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>Muestra u oculta el botón <strong>sin color</strong> .<br/> Válido para todos los valores de <em>ColorTemplate</em> .<br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>El número de filas del chip de color (o muestra) en el área de <strong>colores recientes</strong> .<br/> Válido solo cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td>El número de filas del chip de color (o muestra) en el área <strong>colores estándar</strong> .<br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td>El número de filas del chip de color (o muestra) en el área <strong>colores del tema</strong> .<br/> Válido solo cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

En las siguientes capturas de pantalla se muestran los diseños predeterminados del selector de colores Drop-Down para las tres plantillas de color.



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ \] ![ captura de pantalla de nueva línea del elemento dropdowncolorpicker con el atributo colortemplate establecido en ' ThemeColors '. ](images/markup/colortemplate.themedcolors.1.png) \[ newline\] | `standardcolors`: \[ \] ![ captura de pantalla de nueva línea del elemento dropdowncolorpicker con el atributo colortemplate establecido en ' standardcolors '. ](images/markup/colortemplate.standardcolors.3.png) \[ newline\] | `highlightcolors`: \[ \] ![ captura de pantalla de nueva línea del elemento dropdowncolorpicker con el atributo colortemplate establecido en ' highlightcolors '.](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

El marcado básico necesario para cada tipo de selector de color de Drop-Down se muestra en los ejemplos siguientes:

> [!Note]  
> El selector de colores Drop-Down es un control de [botón](windowsribbon-controls-button.md) válido en una plantilla [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

 


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a>Código

Como control especializado que admite la personalización, cualquier implementación de la Drop-Down selector de colores que aprovecha estas funcionalidades requiere código de aplicación especializado para administrar propiedades y controlar los comandos emitidos por el control.

### <a name="properties"></a>Propiedades

El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control selector de color Drop-Down.

Normalmente, una propiedad del selector de colores Drop-Down se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad. Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

En la tabla siguiente se enumeran las claves de propiedades que están asociadas con el control selector de color Drop-Down.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Clave de propiedad</th>
<th>Descripción</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Define la etiqueta del botón de color <strong>automático</strong> .<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Define el valor de color seleccionado como <a href="/windows/win32/gdi/colorref">COLORREF</a>.<br/> Solo es válido cuando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tiene un valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Define el tipo de color seleccionado.<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Define la capacidad de un control para responder a la interacción del usuario.<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Define la cadena de caracteres para una etiqueta de control.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Define la imagen grande de contraste alto que se va a mostrar para un control.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.<br/> Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Define la imagen grande que se va a mostrar para un control.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.<br/> Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Define la etiqueta para el botón <strong>más colores...</strong> .<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Define la etiqueta para el botón <strong>sin color</strong> .<br/> Válido para todos los valores de <em>ColorTemplate</em> .<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Define la etiqueta de la categoría de <strong>colores recientes</strong> .<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . Esta es la única plantilla que contiene categorías etiquetadas.<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Define la pequeña imagen de contraste alto que se va a mostrar para un control.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.<br/> Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Define la imagen pequeña que se va a mostrar para un control.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.<br/> Para obtener más información sobre los formatos de imagen, vea <a href="windowsribbon-imageformats.md">especificar recursos de imagen de la cinta</a>de opciones.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Define una matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para las muestras de un selector de color Drop-Down.<br/> Cada Drop-Down selector de color <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula. <br/>
<blockquote>
[!Note]<br />
Se muestran los valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> de las <em>columnas</em> <em>StandardColorGridRows</em> x iniciales de la matriz. Si la matriz define menos colores que el número de <code>StandardColors</code> muestras declaradas en el marcado, se muestran espacios vacíos para los chips que faltan.
</blockquote>
<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Define la etiqueta de la categoría de <strong>colores estándar</strong> .<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . Esta es la única plantilla que contiene categorías etiquetadas.<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Define una matriz de cadenas de información sobre herramientas de muestrario de colores para la <code>StandardColors</code> cuadrícula.<br/> Cada Drop-Down selector de color <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula. <br/>
<blockquote>
[!Note]<br />
Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en la <code>StandardColors</code> cuadrícula. Si se proporcionan menos etiquetas que el número de muestras de la <code>StandardColors</code> cuadrícula, se proporciona un valor predeterminado para las muestras de remainining.
</blockquote>
<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Define una matriz de valores <a href="/windows/win32/gdi/colorref">COLORREF</a> para las muestras de un selector de color Drop-Down.<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Se muestran los valores de <a href="/windows/win32/gdi/colorref">COLORREF</a> de las <em>columnas</em> <em>ThemeColorGridRows</em> x iniciales de la matriz. Si la matriz define menos colores que el número de <code>ThemeColors</code> muestras declaradas en el marcado, se muestran espacios vacíos para los chips que faltan.
</blockquote>
<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Define la matriz de cadenas de la información sobre herramientas del muestrario de colores para la <code>ThemeColors</code> cuadrícula.<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en la <code>ThemeColors</code> cuadrícula. Si se proporcionan menos etiquetas que el número de muestras de la <code>ThemeColors</code> cuadrícula, se proporciona un valor predeterminado para las muestras de remainining.
</blockquote>
<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Define la etiqueta de la categoría de <strong>colores del tema</strong> .<br/> Solo es válido cuando <em>ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . Esta es la única plantilla que contiene categorías etiquetadas.<br/></td>
<td>Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Define la cadena de caracteres para una descripción de la información sobre herramientas asociada a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Define la cadena de caracteres para la información sobre herramientas de un comando.<br/></td>
<td>Solo se puede actualizar a través de la invalidación.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Controladores de comandos

El método [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) se usa para personalizar un selector de colores Drop-Down a través de las claves de propiedad indicadas anteriormente. En el ejemplo siguiente se muestra cómo establecer las muestras de color de un selector de colores Drop-Down, en función de una preferencia de estilo personalizado o una cuadrícula de muestra personalizada que se declara en el marcado.


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



En el ejemplo siguiente se muestra una implementación del método [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expone el Drop-Down colores del muestrario del selector de colores a la aplicación de la cinta de opciones.


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Biblioteca de controles de Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Propiedades del selector de colores](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> <dt>

[Ejemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

