---
title: Mapas de bits (SDK de Windows Media Player)
description: Mapas de bits
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Máscaras móviles de Windows Media Player, mapas de bits
- máscaras, mapas de bits
- referencia para máscaras, mapas de bits
- mapas de bits en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488656"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Mapas de bits (SDK de Windows Media Player)

Debe usar una o varias imágenes en la máscara y cada imagen debe definirse en el archivo de definición de máscara. Si no define una imagen en esta sección, la máscara no podrá utilizarla.

El término "mapa de bits" se usa en toda la referencia en un sentido genérico y hace referencia a las imágenes de mapa de bits con una extensión. bmp, imágenes GIF con una extensión. gif, imágenes JPEG con una extensión. jpg y imágenes PNG con una extensión. png.

La sección de mapas de bits del archivo de definición de máscara comienza con esta línea:


```C++
[ Bitmaps ]

```



A continuación, debe agregar una o más líneas que contengan información sobre cada una de las imágenes de la máscara.

Una línea típica podría ser:


```C++
    Background  Background.bmp  0,0

```



Puede usar la siguiente plantilla para la sección de mapas de bits del archivo de definición de máscara:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Debe utilizar el orden siguiente para obtener información de mapa de bits para cada línea de la sección mapa de bits. Cada parte de la línea es obligatoria.

1.  [Tipo de mapa de bits](bitmap-type.md)
2.  [Nombre de archivo](file-name.md)
3.  [Unas](coordinates.md)

Para obtener un ejemplo de código de mapa de bits, consulte la [sección de mapa de bits de ejemplo](sample-bitmap-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




