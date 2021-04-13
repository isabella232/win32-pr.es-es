---
title: Elemento FontControl
description: Representa un control de fuente, que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- FontControl cinta de opciones de Windows
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2020
ms.locfileid: "104420512"
---
# <a name="fontcontrol-element"></a>Elemento FontControl

Representa un [control de fuente](windowsribbon-controls-fontcontrol.md), que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.

## <a name="usage"></a>Uso

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
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
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Predeterminada. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Establecer el atributo <em>FontType</em> en <code>FontOnly</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li>Cuadro combinado de <strong>familia de fuentes</strong> .</li>
<li>Cuadro combinado de <strong>tamaño de fuente</strong> .</li>
<li><p>Botones de alternancia <strong>negrita</strong>, <strong>cursiva</strong>, <strong>subrayado</strong>y <strong>tachado</strong> .</p>
<blockquote>
[!Note]<br />
Los botones de alternancia <strong>tachado</strong> y <strong>subrayado</strong> se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> y <em>IsUnderlineButtonVisible</em> en <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Establecer el atributo <em>FontType</em> en <code>FontWithColor</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li>Cuadro combinado de <strong>familia de fuentes</strong> .</li>
<li>Cuadro combinado de <strong>tamaño de fuente</strong> .</li>
<li><strong>Aumentar</strong> el tamaño de la fuente y <strong>reducir</strong> los botones de incremento y decremento de fuente.</li>
<li><p>Botones de alternancia <strong>negrita</strong>, <strong>cursiva</strong>, <strong>subrayado</strong>y <strong>tachado</strong> .</p>
<blockquote>
[!Note]<br />
Los botones de alternancia <strong>tachado</strong> y <strong>subrayado</strong> se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> y <em>IsUnderlineButtonVisible</em> en <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Selector de colores de <strong>color de texto</strong> .</li>
<li><p>Selector de colores de <strong>color de resaltado de texto</strong> .</p>
<blockquote>
[!Note]<br />
Este control está oculto de forma predeterminada, pero se puede mostrar estableciendo el atributo <em>IsHighlightButtonVisible</em> en <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Establecer el atributo <em>FontType</em> en <code>RichFont</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li>Cuadro combinado de <strong>familia de fuentes</strong> .</li>
<li>Cuadro combinado de <strong>tamaño de fuente</strong> .</li>
<li><strong>Aumentar</strong> el tamaño de la fuente y <strong>reducir</strong> los botones de incremento y decremento de fuente.</li>
<li><p>Botones de alternancia <strong>negrita</strong>, <strong>cursiva</strong>, <strong>subrayado</strong>y <strong>tachado</strong> .</p>
<blockquote>
[!Note]<br />
Los botones de alternancia <strong>tachado</strong> y <strong>subrayado</strong> se muestran de forma predeterminada y no se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> y <em>IsUnderlineButtonVisible</em> en <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Selector de colores de <strong>color de texto</strong> .</li>
<li><p>Selector de colores de <strong>color de resaltado de texto</strong> .</p>
<blockquote>
[!Note]<br />
Este control se muestra de forma predeterminada y no se puede ocultar estableciendo el atributo <em>IsHighlightButtonVisible</em> en <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Botones <strong>de alternancia de subíndice y</strong> <strong>superíndice</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 y versiones más recientes</strong><br/> Restringido a uno de los siguientes valores: <br/>
<blockquote>
[!Note]<br />
Los botones de aumentar y reducir nunca se muestran en <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos): <br/>
<blockquote>
[!Note]<br />
El resaltado de color solo está disponible desde un <strong>FontControl</strong> cuando el valor del atributo <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .<br/> Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontWithColor</code> o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Valor predeterminado cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> .<br/> Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> o <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos): <br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos): <br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Solo es válido cuando el valor de <em>FontType</em> es igual a <code>FontOnly</code> o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Tamaño de punto máximo que se va a mostrar.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Un valor entero entre 1 y 9999, ambos incluidos.<br/> El valor predeterminado es <strong>9999</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Tamaño de punto mínimo que se va a mostrar.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Un valor entero entre 1 y 9999, ambos incluidos.<br/> El valor predeterminado es <strong>1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Solo muestra las fuentes TrueType y OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Predeterminada. No se aplica ninguna restricción en el tipo de fuentes que se muestran.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/>
<blockquote>
[!Note]<br />
Las fuentes verticales van precedidas de un símbolo @ en la lista de <strong>familias de fuentes</strong> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> reales<br/> </dt> <dd> Predeterminada. Muestra las fuentes verticales que se establecen para <strong>mostrarse</strong> en el panel de control <strong>fuentes</strong> . <br/> </dd> <dt><span></span><span></span><strong></strong> es<br/> </dt> <dd> Permite que una aplicación que no admite texto vertical oculte ninguna fuente vertical que esté configurada para <strong>mostrarse</strong> en el panel de control <strong>fuentes</strong> .<br/>
<blockquote>
[!Note]<br />
En Windows Vista, el panel de control <strong>fuentes</strong> no ofrece la funcionalidad <strong>Mostrar</strong> u <strong>ocultar</strong> . En este caso, el atributo <em>ShowVerticalFonts</em> debe establecerse en <code>False</code> .
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                               |
|-----------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/> |
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>               |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Observaciones

Opcional.

Puede aparecer como máximo una vez por cada elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)o [**MenuGroup**](windowsribbon-element-menugroup.md) .

Cualquier atributo de comando **FontControl** declarado en el marcado, como [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), se reemplaza por los atributos de los controles individuales que componen el **FontControl**.

Cualquier intento de seleccionar una muestra de color del selector de colores de un [control de fuente](windowsribbon-controls-fontcontrol.md) puede producir una infracción de acceso si no hay ningún controlador de comandos asociado al control.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para los tres tipos de [control de fuente](windowsribbon-controls-fontcontrol.md).

En esta sección de código se muestran las declaraciones de comandos de **FontControl** , cada una con una declaración de contenedor de [**Grupo**](windowsribbon-element-group.md) .


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



En esta sección de código se muestran las declaraciones de control de **FontControl** en las que cada **FontControl** y [**Grupo**](windowsribbon-element-group.md) se declaran en una sola pestaña.


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | Sí       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Ejemplo de FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





