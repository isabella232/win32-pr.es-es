---
title: String. Symbol (propiedad)
description: Representa el nombre de un recurso de cadena.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Propiedad String. Symbol de la cinta de opciones de Windows
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905044"
---
# <a name="stringsymbol-property"></a>String. Symbol (propiedad)

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
| [**String@**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede aparecer como máximo una vez para cada elemento de [**cadena**](windowsribbon-element-string.md) .

El símbolo está asociado a una definición de cadena en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .

Este elemento contiene un valor de tipo *xs: String*. El valor está restringido a una cadena formada por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.

La longitud máxima es de 100 caracteres.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración **String. Symbol** .


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



 

 





