---
title: Elemento DropDownColorPicker
description: Representa un Pickercontrol de color Drop-Down que, cuando se hace clic en él, muestra una paleta de muestras de color.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00185d14d9066b2cb85da4b23959e84df1827007
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "103786028"
---
# <a name="dropdowncolorpicker-element"></a>Elemento DropDownColorPicker

Representa un control de [selector de colores desplegable](windowsribbon-controls-dropdowncolorpicker.md)que, cuando se hace clic en él, muestra una paleta de muestras de color.

## <a name="usage"></a>Uso

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Chip</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Tamaño de cada chip o muestra de color. <br/> Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Pequeño<br/> </dt> <dd> Cada chip de color es un cuadrado de 11x11 píxeles. <br/> </dd> <dt><span></span><span></span><strong></strong> Medio<br/> </dt> <dd> Cada chip de color es un cuadrado de 16x16 píxeles. <br/> </dd> <dt><span></span><span></span><strong></strong> Amplíe<br/> </dt> <dd> Cada chip de color es un cuadrado de 24x24 píxeles. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Plantillas de diseño que especifican el tipo de <a href="windowsribbon-controls-dropdowncolorpicker.md">selector de colores desplegable</a>. <br/> Restringido a uno de los valores siguientes (si no se declaran atributos opcionales relacionados con un <em>ColorTemplate</em> , se muestra la vista predeterminada):<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Predeterminada. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Establecer el atributo <em>ColorTemplate</em> en <code>ThemeColors</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li>Delimitador de SplitButton.</li>
<li>De forma predeterminada, se muestra el botón color <strong>automático</strong> .</li>
<li>Cuadrícula del muestrario de <strong>colores del tema</strong> de Windows.</li>
<li>Cuadrícula de muestrario de <strong>colores estándar</strong> .</li>
<li>La cuadrícula del muestrario de <strong>colores recientes</strong> es opcional.</li>
<li>Selector de cuadro de diálogo <strong>más colores</strong> .</li>
<li><strong>No</strong> se muestra el botón color de color de forma predeterminada.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Establecer el atributo <em>ColorTemplate</em> en <code>StandardColors</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li>Delimitador de SplitButton.</li>
<li>De forma predeterminada, se muestra el botón color <strong>automático</strong> .</li>
<li>Cuadrícula de muestrario de <strong>colores estándar</strong> .</li>
<li>Selector de cuadro de diálogo <strong>más colores</strong> .</li>
<li><strong>No</strong> se muestra el botón color de color de forma predeterminada.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Establecer el atributo <em>ColorTemplate</em> en <code>HighlightColors</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li>Delimitador de SplitButton.</li>
<li>Cuadrícula del muestrario de <strong>colores estándar</strong> sin encabezado.</li>
<li><strong>No</strong> se muestra el botón color de color de forma predeterminada.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Columnas</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>El número de columnas de chip de color (o muestra).<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Muestra u oculta el botón color <strong>automático</strong> . <br/> Solo es válido <code>StandardColors</code> cuando <code>ThemeColors</code> se especifica o para el atributo <em>ColorTemplate</em> . <br/> Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Muestra u oculta el botón <strong>sin color</strong> . <br/> Válido para todos los valores de <em>ColorTemplate</em> .<br/> Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>El número de filas del chip de color (o muestra) en el área de <strong>colores recientes</strong> . <br/> Solo es válido cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>El número de filas del chip de color (o muestra) en el área <strong>colores estándar</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>El número de filas del chip de color (o muestra) en el área <strong>colores del tema</strong> .<br/> Solo es válido cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo comprendido entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una o varias veces para cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**splitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para los tres tipos de [selector de colores desplegables](windowsribbon-controls-dropdowncolorpicker.md).

En esta sección de código se muestran las declaraciones de comando para tres elementos **DropDownColorPicker** .


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



En esta sección de código se muestran los tres tipos de declaraciones de control de **DropDownColorPicker** .


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | Sí       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de selector de colores desplegables](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Ejemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





