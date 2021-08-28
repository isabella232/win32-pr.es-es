---
title: Drop-Down Selector de colores
description: El marco Windows cinta de opciones proporciona un control de Drop-Down Selector de colores especializado que expone una variedad de configuraciones de color a través de un botón de división y un selector de colores desplegable personalizable.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c96d14cc192d7a1d9394d2f71b40b9b38c7df1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467432"
---
# <a name="drop-down-color-picker"></a>Drop-Down Selector de colores

El marco Windows cinta de opciones proporciona un control de Drop-Down Selector de colores especializado que expone una variedad de configuraciones de color a través de un botón de división y un selector de colores desplegable personalizable.

-   [Introducción](#introduction)
-   [marcado](#markup)
-   [Código](#code)
    -   [Propiedades](#properties)
    -   [Controladores de comandos](#command-handlers)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Mediante la emulación de la apariencia y la funcionalidad del selector de colores Microsoft Office, el marco de la cinta de opciones puede beneficiarse de la coherencia y la familiaridad entre una amplia gama de aplicaciones y contribuir a ello.

## <a name="markup"></a>marcado

Al igual que todos los controles de la cinta de opciones, Drop-Down Selector de colores se implementa y personaliza fácilmente a través del marcado. El marco proporciona una serie de atributos de elemento para que el Drop-Down Selector de colores exponga varios niveles de funcionalidad. En la tabla siguiente se enumeran los Drop-Down Selector de colores atributos.




| Atributo | Descripción | 
|-----------|-------------|
| ColorTemplate | Plantillas de diseño que especifican el tipo de Drop-Down Selector de colores.<br /> Hay tres plantillas, cada una de las cuales especifica un diseño de control y valores predeterminados para los atributos asociados y las claves de propiedad. <br /><ul><li><code>ThemeColors</code></li><li><code>StandardColors</code></li><li><code>HighlightColors</code></li></ul> | 
| ChipSize | Tamaño de cada chip de color (o muestra).<br /><ul><li><code>Small</code></li><li><code>Medium</code></li><li><code>Large</code></li></ul> | 
| Columnas | Número de columnas de chip de color (o muestra).<br /> | 
| CommandName | Nombre de la declaración Command asociada. <br /> | 
| IsAutomaticColorButtonVisible | Muestra (u oculta) el <strong>botón</strong> Automático.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .<br /> | 
| IsNoColorButtonVisible | Muestra (u oculta) el <strong>botón Sin</strong> color.<br /> Válido para todos los <em>valores de ColorTemplate.</em><br /> | 
| RecentColorGridRows | Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> recientes.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .<br /> | 
| StandardColorGridRows | Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> estándar.<br /> | 
| ThemeColorGridRows | Número de filas de chip de color (o muestra) en el área <strong>Colores del</strong> tema.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> .<br /> | 




 

En las capturas de pantalla siguientes se muestran los Drop-Down Selector de colores diseños predeterminados para las tres plantillas de color.



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ captura de pantalla de nueva línea del elemento \] ![ dropdowncolorpicker con el atributo colortemplate establecido en "themecolors". ](images/markup/colortemplate.themedcolors.1.png) \[ Newline\] | `standardcolors`: \[ captura de pantalla de nueva línea del elemento \] ![ dropdowncolorpicker con el atributo colortemplate establecido en "standardcolors". ](images/markup/colortemplate.standardcolors.3.png) \[ Newline\] | `highlightcolors`: \[ captura de pantalla de nueva línea del elemento \] ![ dropdowncolorpicker con el atributo colortemplate establecido en "highlightcolors".](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

El marcado básico necesario para cada Drop-Down Selector de colores se muestra en los ejemplos siguientes:

> [!Note]  
> El Drop-Down Selector de colores es un control [Button](windowsribbon-controls-button.md) válido en una [**plantilla SizeDefinition.**](windowsribbon-element-sizedefinition.md)

 


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

Como control especializado que admite la personalización, cualquier implementación del Drop-Down Selector de colores que aproveche estas funcionalidades requiere código de aplicación especializado para administrar las propiedades y controlar los comandos emitidos por el control.

### <a name="properties"></a>Propiedades

El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el Drop-Down Selector de colores control .

Normalmente, una Drop-Down Selector de colores se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control mediante una llamada al método [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) controla el evento de invalidación y las actualizaciones de propiedad definidas.

El método de devolución de llamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) no se ejecuta y la aplicación consulta un valor de propiedad actualizado, hasta que el marco de trabajo requiera la propiedad . Por ejemplo, cuando se activa una pestaña y se muestra un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.

> [!Note]  
> En algunos casos, una propiedad se puede recuperar mediante el método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

En la tabla siguiente se enumeran las claves de propiedad asociadas al control Drop-Down Selector de colores control .




| Clave de propiedad | Descripción | Notas | 
|--------------|-------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a> | Define la etiqueta del <strong>botón</strong> Color automático.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a> | Define el valor de color seleccionado como <a href="/windows/win32/gdi/colorref">COLORREF.</a><br /> Solo es válido <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> tiene un valor de <code>UI_SWATCHCOLORTYPE_RGB</code> .<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> | Define el tipo de color seleccionado.<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Define la capacidad de un control para responder a la interacción del usuario.<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Define la cadena de caracteres de una etiqueta de control.<br /> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Define la imagen de contraste alto grande que se mostrará para un control.<br /> | Solo se puede actualizar a través de la invalidación.<br /> Para obtener más información sobre los formatos de imagen, vea Especificar recursos de imagen de cinta de <a href="windowsribbon-imageformats.md">opciones.</a><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Define la imagen grande que se mostrará para un control.<br /> | Solo se puede actualizar a través de la invalidación.<br /> Para obtener más información sobre los formatos de imagen, vea Especificar recursos de imagen de cinta de <a href="windowsribbon-imageformats.md">opciones.</a><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a> | Define la etiqueta del <strong>botón Más</strong> colores....<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> o <code>StandardColors</code> .<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a> | Define la etiqueta del botón <strong>Sin</strong> color.<br /> Válido para todos los <em>valores de ColorTemplate.</em><br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a> | Define la etiqueta de la <strong>categoría Colores</strong> recientes.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . Esta es la única plantilla que contiene categorías etiquetadas.<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Define la imagen pequeña de contraste alto que se mostrará para un control.<br /> | Solo se puede actualizar a través de la invalidación.<br /> Para obtener más información sobre los formatos de imagen, vea Especificar recursos de imagen de cinta de <a href="windowsribbon-imageformats.md">opciones.</a><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Define la imagen pequeña que se mostrará para un control .<br /> | Solo se puede actualizar a través de la invalidación.<br /> Para obtener más información sobre los formatos de imagen, vea Especificar recursos de imagen de cinta de <a href="windowsribbon-imageformats.md">opciones.</a><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a> | Define una matriz <a href="/windows/win32/gdi/colorref">de valores COLORREF</a> para las muestras de un Drop-Down Selector de colores.<br /> Cada Drop-Down Selector de colores <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula. <br /><blockquote>[!Note]<br />Se muestran los valores <a href="/windows/win32/gdi/colorref">COLORREF</a> de <em>la columna StandardColorGridRows</em> x <em>de</em> la matriz inicial. Si la matriz define menos colores que el número de muestras declaradas en el marcado, se muestran espacios vacíos para los chips <code>StandardColors</code> que faltan.</blockquote><br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a> | Define la etiqueta de la <strong>categoría Colores</strong> estándar.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . Esta es la única plantilla que contiene categorías etiquetadas.<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a> | Define una matriz de cadenas de información sobre herramientas de la muestra de color para la <code>StandardColors</code> cuadrícula.<br /> Cada Drop-Down Selector de colores <em>ColorTemplate</em> contiene una <code>StandardColors</code> cuadrícula. <br /><blockquote>[!Note]<br />Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en <code>StandardColors</code> la cuadrícula. Si se proporcionan menos etiquetas que el número de muestras de la cuadrícula, se proporciona un valor predeterminado para las muestras <code>StandardColors</code> que permanecen.</blockquote><br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a> | Define una matriz <a href="/windows/win32/gdi/colorref">de valores COLORREF</a> para las muestras de un Drop-Down Selector de colores.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . <br /><blockquote>[!Note]<br />Se muestran los valores <a href="/windows/win32/gdi/colorref">COLORREF</a> de <em>la columna ThemeColorGridRows</em> x <em>de</em> la matriz inicial. Si la matriz define menos colores que el número de muestras declaradas en el marcado, se muestran espacios vacíos para los chips <code>ThemeColors</code> que faltan.</blockquote><br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a> | Define la matriz de cadenas de información sobre herramientas de la muestra de color para la <code>ThemeColors</code> cuadrícula.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . <br /><blockquote>[!Note]<br />Solo se usan las sugerencias de herramientas necesarias para etiquetar las muestras de color que se muestran en <code>ThemeColors</code> la cuadrícula. Si se proporcionan menos etiquetas que el número de muestras de la cuadrícula, se proporciona un valor predeterminado para las muestras <code>ThemeColors</code> que permanecen.</blockquote><br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a> | Define la etiqueta de la categoría <strong>Colores del</strong> tema.<br /> Solo es válido <em>cuando ColorTemplate</em> tiene un valor de <code>ThemeColors</code> . Esta es la única plantilla que contiene categorías etiquetadas.<br /> | Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Define la cadena de caracteres para una descripción de información sobre herramientas asociada a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br /> | Solo se puede actualizar a través de la invalidación. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Define la cadena de caracteres para una información sobre herramientas de comandos.<br /> | Solo se puede actualizar a través de la invalidación. | 




 

### <a name="command-handlers"></a>Controladores de comandos

El [**método IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) se usa para personalizar un Drop-Down Selector de colores a través de las claves de propiedad enumeradas anteriormente. En el ejemplo siguiente se muestra cómo establecer las muestras de color de un Drop-Down Selector de colores, en función de una preferencia de estilo personalizado o una cuadrícula de muestra personalizada que se declara en el marcado.


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



En el ejemplo siguiente se muestra una implementación del método [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) que expone los colores Drop-Down Selector de colores muestra a la aplicación Ribbon.


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

[Windows Biblioteca de controles del marco de opciones](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcado DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Selector de colores propiedades](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Personalización de una cinta de opciones mediante definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> <dt>

[Ejemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

