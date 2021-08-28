---
title: Mapas de bits (Reproductor de Windows Media SDK)
description: Mapas de bits
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Reproductor de Windows Media Máscaras móviles, mapas de bits
- máscaras, mapas de bits
- referencia de máscaras, mapas de bits
- mapas de bits en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ff4689c052162d8addfb9a66aeb6b227916f0e22e21de3e3572ea265380664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123865"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Mapas de bits (Reproductor de Windows Media SDK)

Debe usar una o varias imágenes en la máscara y cada imagen debe definirse en el archivo de definición de máscara. Si no define una imagen en esta sección, la máscara no podrá usarla.

El término "mapa de bits" se usa en toda la referencia en un sentido genérico y hace referencia a imágenes de mapa de bits con una extensión .bmp, imágenes GIF con una extensión .gif, imágenes JPEG con una extensión .jpg e imágenes PNG con una extensión .png.

La sección Mapas de bits del archivo de definición de máscara comienza con esta línea:


```C++
[ Bitmaps ]

```



A continuación, debe agregar una o varias líneas que contengan información sobre cada una de las imágenes de la máscara.

Una línea típica podría ser:


```C++
    Background  Background.bmp  0,0

```



Puede usar la siguiente plantilla para la sección Mapas de bits del archivo de definición de máscara:


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Debe usar el orden siguiente para obtener información de mapa de bits para cada línea de la sección Mapa de bits. Se requiere cada parte de la línea.

1.  [Tipo de mapa de bits](bitmap-type.md)
2.  [Nombre de archivo](file-name.md)
3.  [Coordenadas](coordinates.md)

Para obtener un ejemplo de código de mapa de bits, vea [Sample Bitmap Section](sample-bitmap-section.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de máscara**](skin-reference.md)
</dt> </dl>

 

 




