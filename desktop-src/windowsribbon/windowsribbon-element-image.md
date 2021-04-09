---
title: Elemento Image (marco de cinta de Windows)
description: Representa una imagen.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Cinta de opciones de Windows (elemento)
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104148977"
---
# <a name="image-element"></a>Elemento Image

Representa una imagen.

## <a name="usage"></a>Uso

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
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
<td><strong>Id</strong><br/></td>
<td>XS: positiveInteger Union XS: String<br/></td>
<td>No<br/></td>
<td>IDENTIFICADOR de recurso único. <br/> <br/>
<dt><span></span><span></span><strong></strong> (La Unión de XS: positiveInteger y XS: String)<br/> </dt> <dd> Un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos. <br/> La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Cualquier secuencia de dígitos con un valor mínimo de 96. <br/> Si se omite MinDPI, el valor predeterminado es 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Origen</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (XS: anyURI)<br/> </dt> <dd> Cualquier secuencia de caracteres que representa un identificador URI. El valor del URI es una ruta de acceso absoluta o relativa (en el archivo de marcado de la cinta de opciones) a un recurso de imagen de tipo BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Símbolo de recurso de la imagen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Cadena formada por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado hasta un máximo de 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Descripción                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Imagen. origen**](windowsribbon-element-image-source.md)<br/> | Puede aparecer como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse una o varias veces para cada elemento [**Command. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) .

Cuando una colección de recursos de imagen diseñada para admitir la configuración específica de puntos por pulgada (PPP) se proporciona al marco de la cinta de opciones a través de un conjunto de elementos de **imagen** , el marco de trabajo usa la **imagen** con un valor de atributo *MinDPI* que coincide con la configuración de PPP de la pantalla actual.

Si no se declara ningún elemento de **imagen** con un valor de *MinDPI* que coincida con la configuración de PPP de pantalla actual, el marco de trabajo selecciona la **imagen** que tiene el valor de *MinDPI* más cercano menor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia arriba. De lo contrario, si no se declara ningún elemento de **imagen** con un valor de atributo *MinDPI* inferior al valor de PPP de pantalla actual, el marco de trabajo selecciona el valor de *MinDPI* más cercano mayor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia abajo.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos de **imagen** , una colección de recursos de imagen que están diseñados para admitir cuatro configuraciones de PPP de pantalla específicas.


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Especificar recursos de imagen de cinta](windowsribbon-imageformats.md)
</dt> </dl>

 

 





