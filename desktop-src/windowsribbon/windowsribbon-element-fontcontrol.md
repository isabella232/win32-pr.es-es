---
title: Elemento FontControl
description: Representa un control de fuente, que es un contenedor especializado de controles individuales dedicados a la manipulación de fuentes.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- FontControl, elemento Windows Cinta de opciones
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7b068246da9b26a4b3547e27abd1a9b60c8fd70de10e4edd2438463a156633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202527"
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
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0x2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Predeterminada. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Establecer el <em>atributo FontType</em> en <code>FontOnly</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li><strong>Cuadro combinado de familia</strong> de fuentes.</li>
<li><strong>Cuadro combinado Tamaño de</strong> fuente.</li>
<li><p><strong>Botones</strong>de alternancia Negrita, <strong>Cursiva,</strong>Subrayado <strong>y Tachado.</strong> <strong></strong></p>
<blockquote>
[!Note]<br />
Los <strong>botones</strong> de alternancia Tachado y Subrayado se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> en <strong></strong> <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Establecer el <em>atributo FontType</em> en <code>FontWithColor</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li><strong>Cuadro combinado de familia</strong> de fuentes.</li>
<li><strong>Cuadro combinado tamaño de</strong> fuente.</li>
<li><strong>Aumentar la fuente y</strong> <strong>reducir los botones</strong> de incremento y decremento de tamaño de fuente de fuente.</li>
<li><p><strong>Botones</strong>de alternancia Negrita, <strong>Cursiva,</strong>Subrayado <strong>y Tachado.</strong> <strong></strong></p>
<blockquote>
[!Note]<br />
Los <strong>botones</strong> de alternancia Tachado y Subrayado se muestran de forma predeterminada, pero se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> en <strong></strong> <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Selector de color</strong> de texto.</li>
<li><p><strong>Selector de color de resaltado</strong> de texto.</p>
<blockquote>
[!Note]<br />
Este control está oculto de forma predeterminada, pero se puede mostrar estableciendo el <em>atributo IsHighlightButtonVisible</em> en <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Establecer el <em>atributo FontType</em> en <code>RichFont</code> habilita la siguiente funcionalidad:<br/>
<ul>
<li><strong>Cuadro combinado de familia</strong> de fuentes.</li>
<li><strong>Cuadro combinado tamaño de</strong> fuente.</li>
<li><strong>Aumentar la fuente y</strong> <strong>reducir los botones</strong> de incremento y decremento de tamaño de fuente de fuente.</li>
<li><p><strong>Botones</strong>de alternancia Negrita, <strong>Cursiva,</strong>Subrayado <strong>y Tachado.</strong> <strong></strong></p>
<blockquote>
[!Note]<br />
Los <strong>botones</strong> de alternancia Tachado y Subrayado se muestran de forma predeterminada y no se pueden ocultar estableciendo los atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> en <strong></strong> <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Selector de color</strong> de texto.</li>
<li><p><strong>Selector de color de resaltado</strong> de texto.</p>
<blockquote>
[!Note]<br />
Este control se muestra de forma predeterminada y no se puede ocultar estableciendo el <em>atributo IsHighlightButtonVisible</em> en <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Botones de alternancia</strong> <strong>de subíndice</strong> y superíndice.</li>
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
Los botones Aumentar/Reducir nunca se muestran en <a href="windowsribbon-element-minitoolbar.md"><strong>la barra miniherramienta</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valor predeterminado cuando el valor <em>de FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Valor predeterminado cuando el valor <em>de FontType</em> es igual a <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos): <br/>
<blockquote>
[!Note]<br />
El resaltado de colores solo está disponible desde <strong>un FontControl</strong> cuando el valor del <em>atributo FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valor predeterminado cuando el valor <em>de FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .<br/> Solo es válido cuando el valor <em>de FontType</em> es <code>FontWithColor</code> igual a o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Valor predeterminado cuando el valor <em>de FontType</em> es igual a <code>FontOnly</code> .<br/> Solo es válido cuando el valor <em>de FontType</em> es <code>FontOnly</code> igual a o <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Solo es válido cuando el valor <em>de FontType</em> es <code>FontOnly</code> igual a o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Predeterminada. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Solo es válido cuando el valor <em>de FontType</em> es <code>FontOnly</code> igual a o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Tamaño máximo de punto que se mostrará.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Valor entero comprendido entre 1 y 9999, ambos incluidos.<br/> El valor predeterminado <strong>es 9999.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Tamaño mínimo de punto que se mostrará.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Valor entero comprendido entre 1 y 9999, ambos incluidos.<br/> El valor predeterminado <strong>es 1.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Muestra solo fuentes TrueType y OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Predeterminada. No se coloca ninguna restricción en el tipo de fuentes que se muestra.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Restringido a uno de los siguientes valores (0 y 1 no son válidos):<br/>
<blockquote>
[!Note]<br />
Las fuentes verticales van precedidas de un símbolo @ en la <strong>lista Familia de</strong> fuentes.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Predeterminada. Muestra las fuentes verticales establecidas en <strong>Mostrar en</strong> el panel <strong>de</strong> control Fuentes. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Permite que una aplicación que no admite texto vertical oculte las fuentes verticales establecidas en <strong>Mostrar</strong> en el panel <strong>de</strong> control Fuentes.<br/>
<blockquote>
[!Note]<br />
En Windows Vista, el panel de control <strong>Fuentes</strong> no ofrece <strong>la funcionalidad Mostrar</strong> u <strong>Ocultar.</strong> En este caso, el <em>atributo ShowVerticalFonts</em> debe establecerse en <code>False</code> .
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



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md) [**o MenuGroup.**](windowsribbon-element-menugroup.md)

Los **atributos del comando FontControl** declarados en el marcado, como [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command.TooltipTitle,**](windowsribbon-element-command-tooltiptitle.md)se reemplazan por los atributos de los controles individuales que componen **FontControl**.

Cualquier intento de seleccionar una muestra de color del selector de colores de un [control](windowsribbon-controls-fontcontrol.md) de fuentes puede producir una infracción de acceso si no hay ningún controlador de comandos asociado al control.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para los tres tipos de [Control de fuentes](windowsribbon-controls-fontcontrol.md).

En esta sección de código se muestran las declaraciones del comando **FontControl,** cada una con una [**declaración de**](windowsribbon-element-group.md) contenedor Group.


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



En esta sección de código se muestran las declaraciones de control **FontControl** en las que cada **FontControl** y [**Group**](windowsribbon-element-group.md) se declaran en una sola pestaña.


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

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** Sí



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Ejemplo de FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





