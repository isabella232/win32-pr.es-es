---
title: Propiedad Command.LabelTitle
description: Representa un título de etiqueta.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Command.LabelTitle, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44995d3f17b165c38f9fe7490a33e5d140c8d2b375d5d6b625bb00e3228b21e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810795"
---
# <a name="commandlabeltitle-property"></a>Propiedad Command.LabelTitle

Representa un título de etiqueta.

## <a name="usage"></a>Uso

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                   | Descripción                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**comando**](windowsribbon-element-command.md).

**Command.LabelTitle puede** contener un valor de tipo *xs:string* restringido a cualquier secuencia de caracteres, incluidos los espacios en blanco y los caracteres de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML de juego de caracteres universales (UCS) `&#xA;` para especificar un salto de línea.

 

La longitud máxima no está desenlazada.

Si no se proporciona ningún valor para **Command.LabelTitle**, se [**requiere**](windowsribbon-element-string.md) el elemento secundario String.

> [!Note]  
> Si **Command.LabelTitle contiene** un valor y un elemento secundario [**String,**](windowsribbon-element-string.md) **String** tiene prioridad.

 

**Command.LabelTitle solo** admite la alineación izquierda.

Si un comando se expone a través de un elemento de menú y el valor de **Command.LabelTitle** o UI [ \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md) contiene una letra precedida de una y comercial, como se muestra en el ejemplo siguiente, esta letra se trata como una información sobre teclas y un acelerador de teclado para ese comando por el marco de la cinta de opciones.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Para mostrar una y comercial en una etiqueta, escape la designación de caracteres especiales con una y comercial doble ( ) como se muestra `&&` en el ejemplo siguiente.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un [**elemento Command**](windowsribbon-element-command.md) con una **declaración Command.LabelTitle.**


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[UI \_ PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





