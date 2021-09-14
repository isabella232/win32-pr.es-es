---
title: Propiedad Command.Comment
description: Representa un comentario, o anotación, para un comando.
ms.assetid: 4ac5c7d4-9627-4703-bd3c-594d9497ba24
keywords:
- Command.Comment, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.Comment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7df2131234623dd30fc90339634a932eca5bd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360974"
---
# <a name="commandcomment-property"></a>Propiedad Command.Comment

Representa un comentario, o anotación, para un comando.

## <a name="usage"></a>Uso

``` syntax
<Command.Comment/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**comando**](windowsribbon-element-command.md).

El comentario está asociado a una definición de comando en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define cmdSave 25003 /* Save */` .

Este elemento contiene un valor de tipo *xs:string.*

La longitud máxima es de 250 caracteres.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de [**un elemento Command**](windowsribbon-element-command.md) con una declaración **Command.Comment.**


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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





