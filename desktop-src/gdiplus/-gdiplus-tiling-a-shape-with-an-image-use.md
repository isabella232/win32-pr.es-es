---
description: Del mismo modo que se pueden colocar mosaicos junto a otros para cubrir un piso, las imágenes rectangulares se pueden colocar una junto a la otra para rellenar (mosaico) una forma.
ms.assetid: c92aa519-647a-4cd9-b88e-b79be0116d05
title: Colocar en mosaico una forma con una imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65c0b6e2ce39f5bf5c43b0352b8997202aa7e856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154218"
---
# <a name="tiling-a-shape-with-an-image"></a>Colocar en mosaico una forma con una imagen

Del mismo modo que se pueden colocar mosaicos junto a otros para cubrir un piso, las imágenes rectangulares se pueden colocar una junto a la otra para rellenar (mosaico) una forma. Para colocar en mosaico el interior de una forma, use un pincel de textura. Cuando se construye un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , uno de los argumentos que se pasan al constructor es la dirección de un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) . Cuando se usa el pincel de textura para pintar el interior de una forma, la forma se rellena con copias repetidas de esta imagen.

La propiedad modo de ajuste del objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina cómo se orienta la imagen a medida que se repite en una cuadrícula rectangular. Puede hacer que todos los mosaicos de la cuadrícula tengan la misma orientación, o puede hacer que la imagen se voltee de una posición de la cuadrícula a la siguiente. El volteo puede ser horizontal, vertical o ambos. En los siguientes ejemplos se muestra la disposición en mosaico con distintos tipos de volteo.

## <a name="tiling-an-image"></a>Mosaico de una imagen

En este ejemplo se usa la siguiente imagen 75 × 75 para colocar en mosaico un rectángulo de 200 × 200:

![Ilustración utilizada como base de otras ilustraciones de este tema: una casa y un árbol en segundo plano y centrado en un rectángulo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se coloca en mosaico el rectángulo con la imagen. Tenga en cuenta que todos los mosaicos tienen la misma orientación; no hay ningún volteo.

![Ilustración en la que se muestra la imagen base repetida horizontal y verticalmente en un rectángulo grande](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a>Voltear una imagen horizontalmente mientras se organiza en mosaico

En este ejemplo se usa una imagen 75 × 75 para rellenar un rectángulo de 200 × 200. El modo de ajuste se establece para voltear la imagen horizontalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se coloca en mosaico el rectángulo con la imagen. Tenga en cuenta que cuando se desplaza de un mosaico al siguiente en una fila determinada, la imagen se voltea horizontalmente.

![Ilustración en la que se muestra la imagen base repetida horizontalmente, pero las instancias con números pares se invierten horizontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a>Voltear una imagen verticalmente mientras se organiza en mosaico

En este ejemplo se usa una imagen 75 × 75 para rellenar un rectángulo de 200 × 200. El modo de ajuste se establece para voltear la imagen verticalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se coloca en mosaico el rectángulo con la imagen. Tenga en cuenta que cuando se desplaza de un mosaico al siguiente en una columna determinada, la imagen se voltea verticalmente.

![Ilustración en la que se muestra la imagen base repetida horizontal y verticalmente, pero las filas pares se invierten verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a>Voltear una imagen horizontal y verticalmente mientras se organiza en mosaico

En este ejemplo se usa una imagen 75 × 75 para colocar en mosaico un rectángulo de 200 × 200. El modo de ajuste se establece para voltear la imagen tanto horizontal como verticalmente.


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



En la ilustración siguiente se muestra cómo se coloca el rectángulo en mosaico por la imagen. Tenga en cuenta que cuando se desplaza de un mosaico al siguiente en una fila determinada, la imagen se voltea horizontalmente y, cuando se desplaza de un mosaico al siguiente en una columna determinada, la imagen se voltea verticalmente.

![la ilustración en la que se muestran las instancias alternas de la imagen base de cada fila se voltea horizontalmente, y las filas alternas se voltean verticalmente.](images/tile5.png)

 

 



