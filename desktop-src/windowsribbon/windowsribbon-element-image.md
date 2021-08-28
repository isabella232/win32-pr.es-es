---
title: Elemento Image (Windows Ribbon Framework)
description: Representa una imagen.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Elemento Image Windows Cinta de opciones
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b05f7c93ea1597d2dde4724ff0b24b53769cd9ea
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631683"
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
<td><strong>Id</strong><br/></td>
<td>xs:positiveInteger union xs:string<br/></td>
<td>No<br/></td>
<td>Identificador de recurso único. <br/> <br/>
<dt><span></span><span></span><strong></strong> (La unión de xs:positiveInteger y xs:string)<br/> </dt> <dd> Valor entero comprendido entre 2 y 59999, inclusivo o 0x2 y 0xea5f en hexadecimal, inclusivo. <br/> La longitud máxima es de 10 caracteres, incluidos ceros iniciales opcionales. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Cualquier secuencia de dígitos con un valor mínimo de 96. <br/> Si se omite MinDPI, el valor predeterminado es 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Origen</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:anyURI)<br/> </dt> <dd> Cualquier secuencia de caracteres que represente un URI. El valor uri es una ruta de acceso absoluta o relativa (al archivo de marcado de la cinta de opciones) a un recurso de imagen de tipo BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Símbolo de recurso para la imagen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Cadena formada por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado hasta un máximo de 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                               | Descripción                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image.Source**](windowsribbon-element-image-source.md)<br/> | Puede producirse como máximo una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para cada [**elemento Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command.LargeHighContrastImages.**](windowsribbon-element-command-largehighcontrastimages.md)

Cuando se proporciona una colección de recursos de imagen diseñados para admitir valores específicos de puntos de pantalla por  pulgada (ppp) al marco de la cinta de opciones a través de un conjunto de elementos **Image,** el marco usa la imagen con un valor de atributo *MinDPI* que coincide con la configuración de ppp de la pantalla actual.

Si no se declara ningún elemento **Image** con un valor *MinDPI* que  coincida con la configuración de ppp de la pantalla actual, el marco elige la imagen que tiene el valor *MinDPI* más próximo menos que el valor de ppp de la pantalla actual y escala verticalmente el recurso de imagen. De lo contrario, si no se declara ningún elemento **Image** con un valor de atributo *MinDPI* menor que el valor de ppp de pantalla actual, el marco elige el valor *MinDPI* más próximo mayor que el valor de ppp de pantalla actual y escala el recurso de imagen hacia abajo.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos **Image,** una colección de recursos de imagen diseñados para admitir cuatro configuraciones de ppp de pantalla específicas.


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

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Especificar recursos de imagen de cinta de opciones](windowsribbon-imageformats.md)
</dt> </dl>

 

 





