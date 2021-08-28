---
title: Command, elemento
description: Representa una definición de comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Elemento Command Windows Ribbon
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c29539c9c76342b8b88603ea3dd2926554228ac
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626951"
---
# <a name="command-element"></a>Command, elemento

Representa una definición de comando.

## <a name="usage"></a>Uso

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<td><strong>Comment</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Se usa para anotar el elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> Longitud máxima: 250 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>No<br/></td>
<td>Identificador de recurso único. <br/> <br/>
<dt><span></span><span></span><strong></strong> (La unión de xs:positiveInteger y xs:string)<br/> </dt> <dd> Valor entero comprendido entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo. <br/> La longitud máxima es de 10 caracteres, incluidos los ceros iniciales opcionales. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Keytip</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el método abreviado de teclado de un elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena compuesta de cualquier secuencia de caracteres, incluidos los espacios en blanco.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto mostrado en un elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>LabelTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto mostrado en un elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nombre</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de dígitos, letras o caracteres de subrayado.<br/> Longitud máxima: 100 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de dígitos, letras o caracteres de subrayado.<br/> Longitud máxima: 100 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TooltipDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto mostrado en un elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>TooltipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto mostrado en un elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                     | Descripción                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Command.Comment**](windowsribbon-element-command-comment.md)<br/>                                 | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.Keytip**](windowsribbon-element-command-keytip.md)<br/>                                   | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Puede producirse como máximo una vez<br/> <br/> |
| [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Comentarios

Necesario.

Puede producirse una o varias veces para cada [**elemento Application.Commands.**](windowsribbon-element-application-commands.md)

Los elementos secundarios del **elemento Command** pueden producirse en cualquier orden.

Normalmente, los recursos de comando se declaran en el marcado de la cinta de opciones, pero también se pueden establecer en tiempo de ejecución con una llamada a [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). Por ejemplo, es posible establecer la propiedad [ \_ PKEY \_ Keytip](windowsribbon-reference-properties-uipkey-keytip.md) de la interfaz de usuario para un comando en lugar de declarar un valor en el marcado con el [**elemento Command.Keytip.**](windowsribbon-element-command-keytip.md)

En los casos en los que las propiedades command, como etiquetas e imágenes, no se pueden establecer con [**SetUICommandProperty,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) se pueden invalidar con una llamada a [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). Después de la invalidación, el marco consulta la aplicación host para obtener los detalles del recurso.

> [!Note]  
> No se puede restablecer un recurso de la tabla de recursos de marcado después de que se haya invalidado.

 

Se agrega una definición de comando al archivo de encabezado de marcado de la cinta de opciones para cada **comando** declarado en el marcado.

El valor de *Keytip actúa como* acelerador de teclado para un comando a menos que ese comando se exponga a través de un elemento de menú. En este caso, el marco omite el valor *keytip* y, en su lugar, usa un carácter precedido por una y comercial, tal como se especifica en *LabelTitle* o [UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md). Si no se especifica ninguna yandida mediante *LabelTitle* o ui PKEY Label, no se expone ninguna tecla o acelerador \_ \_ de teclado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un manifiesto de **elementos Command** para una **pestaña** Inicio.


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



 

