---
title: Elemento String
description: Representa un recurso de cadena.
ms.assetid: 83e5bdbb-ef86-4942-af40-2e327360ee67
keywords:
- Elemento de cadena cinta de Windows
topic_type:
- apiref
api_name:
- String
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 577d318292081dddf4e2839967642c6115a474d6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076808"
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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td><dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>IDENTIFICADOR de recurso único. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos. <br/> La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Símbolo de recurso de la cadena.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado.<br/> La longitud máxima es de 100 caracteres.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Descripción                                   |
|---------------------------------------------------------------------------|-----------------------------------------------|
| [**Cadena. contenido**](windowsribbon-element-string-content.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |
| [**String.Id**](windowsribbon-element-string-id.md)<br/>           | Puede aparecer como máximo una vez<br/> <br/> |
| [**String. Symbol**](windowsribbon-element-string-symbol.md)<br/>   | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                           |
|---------------------------------------------------------------------------------------------------|
| [**Command. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                         |
| [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>     |
| [**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                 |
| [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/> |
| [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>             |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**comando Command. LabelTitle**](windowsribbon-element-command-labeltitle.md), Command [**. LabelDescription**](windowsribbon-element-command-labeldescription.md), [**Command. KeyTip**](windowsribbon-element-command-keytip.md), [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)o [**Command. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md) .

La definición de cadena se agrega al archivo de encabezado de la cinta de opciones, por ejemplo, `#define strSave 59999` .

La cadena se agrega a una tabla de cadenas en el archivo de recursos de la cinta de opciones, donde el marco de la cinta de opciones genera un nombre y un ID. Si no se declara ninguno.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado de un elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) con una declaración de **cadena** .


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



 

 





