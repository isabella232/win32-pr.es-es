---
title: Image. Source (propiedad)
description: Representa la ruta de acceso al directorio de una imagen.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Imagen. Source (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801898"
---
# <a name="imagesource-property"></a>Image. Source (propiedad)

Representa la ruta de acceso al directorio de una imagen.

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
| [**Impresión**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**imagen**](windowsribbon-element-image.md).

Este elemento contiene un valor de tipo *xs: anyURI* o cualquier secuencia de caracteres que representa un identificador uniforme de recursos (URI). El valor del URI es una ruta de acceso absoluta o relativa (en el archivo de marcado de la cinta de opciones) del directorio de un recurso de imagen de tipo Bitmap (BMP).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos de [**imagen**](windowsribbon-element-image.md) , una colección de recursos de imagen que están diseñados para admitir cuatro configuraciones de PPP de pantalla específicas. La propiedad **Image. Source** se usa para especificar la ruta de acceso al recurso de imagen.


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





