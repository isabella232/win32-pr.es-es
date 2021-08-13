---
title: String.Id propiedad
description: Representa el identificador único de un recurso de cadena.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441655"
---
# <a name="stringid-property"></a>String.Id propiedad

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
| [**Cadena**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**elemento String.**](windowsribbon-element-string.md)

El valor de **String.Id** debe ser único.

El identificador está asociado a una definición de cadena en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .

Este elemento contiene un valor de la unión de los tipos *xs:positiveInteger* y *xs:string.* El valor está restringido a un valor entero entre 2 y 59999, ambos incluidos o 0x2 y 0xea5f en hexadecimal, inclusivo.

La longitud máxima es de 10 caracteres con ceros iniciales opcionales.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de [**un elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con **una String.Id** de datos.


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



 

 





