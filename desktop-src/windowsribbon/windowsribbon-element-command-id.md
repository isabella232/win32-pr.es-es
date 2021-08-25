---
title: Command.Id propiedad
description: Representa un identificador único para un comando.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.Id propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c542cbf4103c6063a177990d454a45e5f937745720c7c0a7bc5c60c4c1047e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931624"
---
# <a name="commandid-property"></a>Command.Id propiedad

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



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**comando**](windowsribbon-element-command.md).

El identificador está asociado a una definición de comando en el archivo de encabezado de la cinta de opciones, por ejemplo, `#define cmdSave 25003 /* Save */` .

Este elemento contiene un valor de la unión de tipos *xs:positiveInteger* y *xs:string* restringido a un valor entero comprendido entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo.

La longitud máxima es de 10 caracteres, incluidos ceros iniciales opcionales.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un [**elemento Command**](windowsribbon-element-command.md) con una **Command.Id** de datos.


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



 

 





