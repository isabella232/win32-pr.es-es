---
title: Propiedad String.Symbol
description: Representa el nombre de un recurso de cadena.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- String.Symbol, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706875"
---
# <a name="stringsymbol-property"></a>Propiedad String.Symbol

Representa el nombre de un recurso de cadena.

## <a name="usage"></a>Uso

``` syntax
<String.Symbol/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**elemento String.**](windowsribbon-element-string.md)

El símbolo está asociado a una definición de cadena en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .

Este elemento contiene un valor de tipo *xs:string.* El valor está restringido a una cadena compuesta por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.

La longitud máxima es de 100 caracteres.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **declaración String.Symbol.**


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





