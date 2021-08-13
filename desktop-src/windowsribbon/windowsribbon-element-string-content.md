---
title: Propiedad String.Content
description: Representa el contenido de un recurso de cadena.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- String.Content, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526062956c6ab7498caac8712ba932d6e7ac1f2dd6307359183d2529e35fc8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439510"
---
# <a name="stringcontent-property"></a>Propiedad String.Content

Representa el contenido de un recurso de cadena.

## <a name="usage"></a>Uso

``` syntax
<String.Content/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cadena**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**elemento String.**](windowsribbon-element-string.md)

Este elemento contiene un valor de tipo *xs:string.* El valor está restringido a una cadena compuesta de cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

La longitud máxima no está desenlazada.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **declaración String.Content.**


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





