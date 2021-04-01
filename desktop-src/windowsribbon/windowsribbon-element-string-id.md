---
title: Propiedad String.Id
description: Representa el identificador único de un recurso de cadena.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Propiedad String.Id cinta de opciones de Windows
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150933"
---
# <a name="stringid-property"></a>Propiedad String.Id

Representa el identificador único de un recurso de cadena.

## <a name="usage"></a>Uso

``` syntax
<String.Id/>
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

El valor de **String.ID** debe ser único.

El identificador está asociado a una definición de cadena en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .

Este elemento contiene un valor de la Unión de tipos *xs: positiveInteger* y *xs: String*. El valor se limita a un valor entero comprendido entre 2 y 59999, ambos incluidos, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.

La longitud máxima es de 10 caracteres con ceros a la izquierda opcionales.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración **String.ID** .


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



 

 





