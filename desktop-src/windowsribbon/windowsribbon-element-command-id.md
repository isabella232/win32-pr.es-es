---
title: Propiedad Command.Id
description: Representa un identificador único para un comando.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Propiedad Command.Id cinta de opciones de Windows
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492532"
---
# <a name="commandid-property"></a>Propiedad Command.Id

Representa un identificador único para un comando.

## <a name="usage"></a>Uso

``` syntax
<Command.Id/>
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

Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).

El identificador está asociado a una definición de comando en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define cmdSave 25003 /* Save */` .

Este elemento contiene un valor de la Unión de tipos *xs: positiveInteger* y *xs: String* restringido a un valor entero comprendido entre 2 y 59999, ambos incluidos, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.

La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un elemento [**Command**](windowsribbon-element-command.md) con una declaración **Command.ID** .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





