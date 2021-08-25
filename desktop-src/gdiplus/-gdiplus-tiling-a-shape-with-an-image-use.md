---
description: Del mismo modo que los iconos se pueden colocar unos junto a otros para cubrir un suelo, se pueden colocar imágenes rectangulares unas junto a otras para rellenar (mosaico) una forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Cambiar el tamaño de una forma con una imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0fc04439db21191ddc110859ae628e975d50bf617db3da63189859070766b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943775"
---
# <a name="tiling-a-shape-with-an-image"></a>Cambiar el tamaño de una forma con una imagen

Del mismo modo que los iconos se pueden colocar unos junto a otros para cubrir un suelo, se pueden colocar imágenes rectangulares unas junto a otras para rellenar (mosaico) una forma. Para crear mosaicos en el interior de una forma, use un pincel de textura. Al construir un [**objeto TextureBrush,**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) uno de los argumentos que se pasan al constructor es la dirección de un [**objeto Image.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Cuando se usa el pincel de textura para pintar el interior de una forma, la forma se rellena con copias repetidas de esta imagen.

La propiedad wrap mode del [**objeto TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina cómo se orienta la imagen a medida que se repite en una cuadrícula rectangular. Puede hacer que todos los iconos de la cuadrícula tengan la misma orientación, o bien puede hacer que la imagen se voltee de una posición de cuadrícula a la siguiente. El volteo puede ser horizontal, vertical o ambos. En los ejemplos siguientes se muestra el tiling con diferentes tipos de volteo.

## <a name="tiling-an-image"></a>Aplicación de tilings a una imagen

En este ejemplo se usa la siguiente imagen de 75 ×75 para crear un mosaico de un rectángulo de 200 ×200:

![ilustración usada como base de otras ilustraciones de este tema: una casa y un árbol sobre el fondo y centrados en un rectángulo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se pone en mosaico el rectángulo con la imagen. Tenga en cuenta que todos los iconos tienen la misma orientación; no hay ninguna volteo.

![ilustración que muestra la imagen base repetida horizontal y verticalmente en un rectángulo grande](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling&quot;></a>Voltear una imagen horizontalmente durante el mosaico

En este ejemplo se usa una imagen de 75 ×75 para rellenar un rectángulo de 200 × 200. El modo de ajuste se establece para voltear la imagen horizontalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se pone en mosaico el rectángulo con la imagen. Tenga en cuenta que, a medida que se mueve de un icono a otro en una fila determinada, la imagen se volteará horizontalmente.

![ilustración que muestra la imagen base repetida horizontalmente, pero las instancias numeradas uniformes se invierten horizontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling&quot;></a>Voltear una imagen verticalmente durante el mosaico

En este ejemplo se usa una imagen de 75 ×75 para rellenar un rectángulo de 200 × 200. El modo de ajuste se establece para voltear la imagen verticalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se pone en mosaico el rectángulo con la imagen. Tenga en cuenta que, a medida que se mueve de un icono a otro en una columna determinada, la imagen se volteará verticalmente.

![ilustración que muestra la imagen base repetida horizontal y verticalmente, pero las filas numeradas uniformes se invierten verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling&quot;></a>Voltear una imagen horizontal y verticalmente durante el mosaico

En este ejemplo se usa una imagen de 75 ×75 para crear un mosaico de un rectángulo de 200 ×200. El modo de ajuste se establece para voltear la imagen tanto horizontal como verticalmente.


```
Image image(L&quot;HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo la imagen pone en mosaico el rectángulo. Tenga en cuenta que, a medida que se mueve de un icono al siguiente en una fila determinada, la imagen se volteará horizontalmente y, a medida que se mueve de un icono a otro en una columna determinada, la imagen se volteará verticalmente.

![ilustración que muestra las instancias alternas de la imagen base en cada fila se voltear horizontalmente y las filas alternas se voltear verticalmente](images/tile5.png)

 

 



