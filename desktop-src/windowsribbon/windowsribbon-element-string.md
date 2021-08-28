---
title: Elemento String
description: Representa un recurso de cadena.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Cinta de opciones Windows elemento String
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a34a417b6ad4d57bea83fcae13d810b22114271
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630961"
---
# <a name="string-element"></a>Elemento String

Representa un recurso de cadena.

## <a name="usage"></a>Uso

``` syntax
<String
  Content = "xs:string"
  Id = "xs:positiveInteger or xs:string"
  Symbol = "xs:string">
  child elements
</String>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Contenido</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Identificador de recurso único. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Valor entero comprendido entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo. <br/> La longitud máxima es de 10 caracteres, incluidos ceros iniciales opcionales. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Símbolo de recurso para la cadena.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.<br/> La longitud máxima es de 100 caracteres.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Descripción                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**String.Content**](windowsribbon-element-string-content.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Puede producirse como máximo una vez<br/> <br/> |
| [**String.Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command.Keytip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**elemento Command.LabelTitle,**](windowsribbon-element-command-labeltitle.md) [**Command.LabelDescription,**](windowsribbon-element-command-labeldescription.md) [**Command.Keytip,**](windowsribbon-element-command-keytip.md) [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)o [**Command.TooltipDescription.**](windowsribbon-element-command-tooltipdescription.md)

La definición de cadena se agrega al archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .

La cadena se agrega a una tabla de cadenas en el archivo de recursos de la cinta de opciones donde el marco de la cinta de opciones genera un nombre e identificador si no se declara ninguno.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) con una **declaración String.**


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="element-information"></a>Información de elemento

- **Sistema mínimo admitido:** Windows 7 
- **Puede estar vacío:** No



 

 





