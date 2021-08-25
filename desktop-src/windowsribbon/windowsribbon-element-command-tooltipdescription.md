---
title: Propiedad Command.TooltipDescription
description: Representa una descripción de información sobre herramientas.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- Command.TooltipDescription, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dd356ae3bcfa5949e8469240330a3a09a11f01b5a919ed02f4eb55683fbc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933215"
---
# <a name="commandtooltipdescription-property"></a>Propiedad Command.TooltipDescription

Representa una descripción de información sobre herramientas.

## <a name="usage"></a>Uso

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
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

**Command.TooltipDescription** puede contener un valor de tipo *xs:string* restringido a cualquier secuencia de caracteres, incluidos los espacios en blanco y los caracteres de salto de línea.

> [!Note]  
> Use la referencia de caracteres XML de juego de caracteres universales (UCS) `&#xA;` para especificar un salto de línea.

 

La longitud máxima no está desenlazada.

Si no se proporciona ningún valor para **Command.TooltipDescription**, se [**requiere**](windowsribbon-element-string.md) el elemento secundario String.

> [!Note]  
> Si **Command.TooltipDescription contiene** un valor y un elemento secundario [**String,**](windowsribbon-element-string.md) **String** tiene prioridad.

 

**Command.TooltipDescription solo** admite la alineación izquierda.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un [**elemento Command**](windowsribbon-element-command.md) con una **declaración Command.TooltipDescription.**


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

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





