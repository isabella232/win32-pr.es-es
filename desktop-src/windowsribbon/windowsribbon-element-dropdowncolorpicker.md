---
title: Elemento DropDownColorPicker
description: Representa un Drop-Down selector de color que cuando se hace clic muestra una paleta de muestras de color.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker, elemento de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442906"
---
# <a name="dropdowncolorpicker-element"></a>Elemento DropDownColorPicker

Representa una [lista desplegable Selector de colores](windowsribbon-controls-dropdowncolorpicker.md)control que cuando se hace clic muestra una paleta de muestras de color.

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
<th>Requerido</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ChipSize</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Tamaño de cada chip de color o muestra. <br/> Restringido a uno de los siguientes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Pequeño)<br/> </dt> <dd> Cada chip de color es un cuadrado de 11 x 11 píxeles. <br/> </dd> <dt><span></span><span></span><strong></strong> (Medio)<br/> </dt> <dd> Cada chip de color es un cuadrado de 16 x 16 píxeles. <br/> </dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Cada chip de color es un cuadrado de 24 x 24 píxeles. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Plantillas de diseño que especifican el tipo <a href="windowsribbon-controls-dropdowncolorpicker.md">de lista desplegable Selector de colores</a>. <br/> Se restringe a uno de los siguientes valores (si no se declara ningún atributo opcional relacionado con una <em>colorTemplate,</em> se muestra la vista predeterminada):<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Predeterminada. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Establecer el <em>atributo ColorTemplate</em> en <code>ThemeColors</code> habilita la funcionalidad siguiente:<br/>
<ul>
<li>Delimitador SplitButton.</li>
<li><strong>El</strong> botón de color automático se muestra de forma predeterminada.</li>
<li>Cuadrícula <strong>de muestra de colores</strong> de tema de Windows.</li>
<li><strong>Cuadrícula de muestra</strong> de colores estándar.</li>
<li><strong>La cuadrícula de</strong> muestra Colores recientes es opcional.</li>
<li><strong>Iniciador del cuadro</strong> de diálogo Más colores.</li>
<li><strong>No se muestra</strong> ningún botón de color de forma predeterminada.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Establecer el <em>atributo ColorTemplate</em> en <code>StandardColors</code> habilita la funcionalidad siguiente:<br/>
<ul>
<li>Delimitador SplitButton.</li>
<li><strong>El</strong> botón de color automático se muestra de forma predeterminada.</li>
<li><strong>Cuadrícula de muestra</strong> de colores estándar.</li>
<li><strong>Iniciador del cuadro</strong> de diálogo Más colores.</li>
<li><strong>No se muestra</strong> ningún botón de color de forma predeterminada.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Establecer el <em>atributo ColorTemplate</em> en <code>HighlightColors</code> habilita la funcionalidad siguiente:<br/>
<ul>
<li>Delimitador SplitButton.</li>
<li><strong>Cuadrícula de muestra</strong> de colores estándar sin encabezado.</li>
<li><strong>No se muestra</strong> ningún botón de color de forma predeterminada.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Columnas</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Número de columnas de chip de color (o muestra).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Muestra (u oculta) el <strong>botón Color</strong> automático. <br/> Válido solo cuando <code>StandardColors</code> se especifica o para el atributo <code>ThemeColors</code> <em>ColorTemplate.</em> <br/> Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Muestra (u oculta) el <strong>botón Sin</strong> color. <br/> Válido para todos <em>los valores de ColorTemplate.</em><br/> Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> recientes. <br/> Válido solo cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Número de filas de chip de color (o muestra) en el <strong>área Colores</strong> estándar.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Número de filas de chip de color (o muestra) en el área <strong>Colores del</strong> tema.<br/> Válido solo cuando <code>ThemeColors</code> se especifica para el atributo <em>ColorTemplate.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Cualquier valor entero positivo entre 1 y 256, ambos incluidos.<br/> </dd> </dl></td>
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



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md) [**o SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para los tres tipos de lista [Selector de colores](windowsribbon-controls-dropdowncolorpicker.md).

En esta sección de código se muestran las declaraciones command para tres **elementos DropDownColorPicker.**


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



En esta sección de código se muestran los tres tipos de declaraciones de control **DropDownColorPicker.**


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

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** Sí



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de Selector de colores desplegable](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Ejemplo de DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





