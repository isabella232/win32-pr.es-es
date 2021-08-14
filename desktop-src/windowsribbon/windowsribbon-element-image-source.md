---
title: Propiedad Image.Source
description: Representa la ruta de acceso del directorio de una imagen.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Image.Source, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20612f0d25f914cb4c80ae77bb001a678af79e4605c3e1358ed7e33f6b19d805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202410"
---
# <a name="imagesource-property"></a>Propiedad Image.Source

Representa la ruta de acceso del directorio de una imagen.

## <a name="usage"></a>Uso

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                 |
|---------------------------------------------------------|
| [**Imagen**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**imagen**](windowsribbon-element-image.md).

Este elemento contiene un valor de tipo *xs:anyURI* o cualquier secuencia de caracteres que represente un identificador uniforme de recursos (URI). El valor uri es una ruta de acceso de directorio absoluta o relativa (con el archivo de marcado de la cinta) de un recurso de imagen de tipo bitmap (BMP).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos [**Image,**](windowsribbon-element-image.md) una colección de recursos de imagen diseñados para admitir cuatro valores de ppp de pantalla específicos. La **propiedad Image.Source** se usa para especificar la ruta de acceso al recurso de imagen.


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 





