---
title: Command, elemento
description: Representa una definición de comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Elemento Command de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359308"
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
<td><strong>Comentario</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Se utiliza para anotar el elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> Longitud máxima: 250 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>XS: positiveInteger Union XS: String<br/></td>
<td>No<br/></td>
<td>IDENTIFICADOR de recurso único. <br/> <br/>
<dt><span></span><span></span><strong></strong> (La Unión de XS: positiveInteger y XS: String)<br/> </dt> <dd> Un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos. <br/> La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>KeyTip</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el método abreviado de teclado de un elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluido el espacio en blanco.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto que se muestra en un elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>LabelTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto que se muestra en un elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nombre</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Una cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de dígitos, letras o caracteres de subrayado.<br/> Longitud máxima: 100 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Una cadena que consta de una letra o un carácter de subrayado seguido de cualquier secuencia de dígitos, letras o caracteres de subrayado.<br/> Longitud máxima: 100 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TooltipDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto que se muestra en un elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>TooltipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Cadena que representa el texto que se muestra en un elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                     | Descripción                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Comando. Comment**](windowsribbon-element-command-comment.md)<br/>                                 | Puede aparecer como máximo una vez<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Puede aparecer como máximo una vez<br/> <br/> |
| [**Command. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                                   | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | Puede aparecer como máximo una vez<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Puede aparecer como máximo una vez<br/> <br/> |
| [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Puede producirse una o varias veces para cada elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .

Los elementos secundarios del elemento **Command** pueden aparecer en cualquier orden.

Normalmente, los recursos de comando se declaran en el marcado de la cinta de opciones, pero también se pueden establecer en tiempo de ejecución con una llamada a [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). Por ejemplo, es posible establecer la propiedad [ \_ \_ KeyTip PKEY](windowsribbon-reference-properties-uipkey-keytip.md) de la interfaz de usuario para un comando en lugar de declarar un valor en el marcado con el elemento [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .

En los casos en los que las propiedades de comando, como etiquetas e imágenes, no se pueden establecer con [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , se pueden invalidar con una llamada a [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). Después de la invalidación, el marco de trabajo consulta la aplicación host para ver los detalles del recurso.

> [!Note]  
> Un recurso no se puede restablecer desde la tabla de recursos de marcado una vez que se ha invalidado.

 

Una definición de comando se agrega al archivo de encabezado de marca de la cinta de opciones para cada **comando** declarado en el marcado.

El valor de *KeyTip* actúa como la tecla de aceleración para un comando, a menos que ese comando se exponga a través de un elemento de menú. En este caso, el marco de trabajo omite el valor de *KeyTip* y, en su lugar, usa un carácter precedido por una y comercial según lo especificado por *LabelTitle* o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario. Si el *LabelTitle* o la etiqueta PKEY de IU no especifican el carácter de y comercial \_ \_ , no se expone ningún KeyTip ni tecla de aceleración.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra un manifiesto de elementos **Command** para una pestaña **Home** .


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



 

