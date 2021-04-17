---
title: String. Content (propiedad)
description: Representa el contenido de un recurso de cadena.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Propiedad String. Content (cinta de Windows)
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8912264e4f55568c190212227d2e305f9d676a1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705129"
---
# <a name="stringcontent-property"></a>String. Content (propiedad)

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
| [**String@**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede aparecer como máximo una vez para cada elemento de [**cadena**](windowsribbon-element-string.md) .

Este elemento contiene un valor de tipo *xs: String*. El valor está restringido a una cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.

La longitud máxima es sin límite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración **String. Content** .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





