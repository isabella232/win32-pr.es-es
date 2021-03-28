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
# <a name="tiling-a-shape-with-an-image"></a><span data-ttu-id="fd00c-103">Colocar en mosaico una forma con una imagen</span><span class="sxs-lookup"><span data-stu-id="fd00c-103">Tiling a Shape with an Image</span></span>

<span data-ttu-id="fd00c-104">Del mismo modo que se pueden colocar mosaicos junto a otros para cubrir un piso, las imágenes rectangulares se pueden colocar una junto a la otra para rellenar (mosaico) una forma.</span><span class="sxs-lookup"><span data-stu-id="fd00c-104">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="fd00c-105">Para colocar en mosaico el interior de una forma, use un pincel de textura.</span><span class="sxs-lookup"><span data-stu-id="fd00c-105">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="fd00c-106">Cuando se construye un objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , uno de los argumentos que se pasan al constructor es la dirección de un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="fd00c-106">When you construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, one of the arguments you pass to the constructor is the address of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="fd00c-107">Cuando se usa el pincel de textura para pintar el interior de una forma, la forma se rellena con copias repetidas de esta imagen.</span><span class="sxs-lookup"><span data-stu-id="fd00c-107">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>

<span data-ttu-id="fd00c-108">La propiedad modo de ajuste del objeto [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) determina cómo se orienta la imagen a medida que se repite en una cuadrícula rectangular.</span><span class="sxs-lookup"><span data-stu-id="fd00c-108">The wrap mode property of the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="fd00c-109">Puede hacer que todos los mosaicos de la cuadrícula tengan la misma orientación, o puede hacer que la imagen se voltee de una posición de la cuadrícula a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-109">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="fd00c-110">El volteo puede ser horizontal, vertical o ambos.</span><span class="sxs-lookup"><span data-stu-id="fd00c-110">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="fd00c-111">En los siguientes ejemplos se muestra la disposición en mosaico con distintos tipos de volteo.</span><span class="sxs-lookup"><span data-stu-id="fd00c-111">The following examples demonstrate tiling with different types of flipping.</span></span>

## <a name="tiling-an-image"></a><span data-ttu-id="fd00c-112">Mosaico de una imagen</span><span class="sxs-lookup"><span data-stu-id="fd00c-112">Tiling an Image</span></span>

<span data-ttu-id="fd00c-113">En este ejemplo se usa la siguiente imagen 75 × 75 para colocar en mosaico un rectángulo de 200 × 200:</span><span class="sxs-lookup"><span data-stu-id="fd00c-113">This example uses the following 75 ×75 image to tile a 200 ×200 rectangle:</span></span>

![Ilustración utilizada como base de otras ilustraciones de este tema: una casa y un árbol en segundo plano y centrado en un rectángulo](images/tile1.png)


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="fd00c-115">En la ilustración siguiente se muestra cómo se coloca en mosaico el rectángulo con la imagen.</span><span class="sxs-lookup"><span data-stu-id="fd00c-115">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="fd00c-116">Tenga en cuenta que todos los mosaicos tienen la misma orientación; no hay ningún volteo.</span><span class="sxs-lookup"><span data-stu-id="fd00c-116">Note that all tiles have the same orientation; there is no flipping.</span></span>

![Ilustración en la que se muestra la imagen base repetida horizontal y verticalmente en un rectángulo grande](images/tile2.png)

 

## <a name="flipping-an-image-horizontally-while-tiling"></a><span data-ttu-id="fd00c-118">Voltear una imagen horizontalmente mientras se organiza en mosaico</span><span class="sxs-lookup"><span data-stu-id="fd00c-118">Flipping an Image Horizontally While Tiling</span></span>

<span data-ttu-id="fd00c-119">En este ejemplo se usa una imagen 75 × 75 para rellenar un rectángulo de 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="fd00c-119">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="fd00c-120">El modo de ajuste se establece para voltear la imagen horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-120">The wrap mode is set to flip the image horizontally.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipX);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="fd00c-121">En la ilustración siguiente se muestra cómo se coloca en mosaico el rectángulo con la imagen.</span><span class="sxs-lookup"><span data-stu-id="fd00c-121">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="fd00c-122">Tenga en cuenta que cuando se desplaza de un mosaico al siguiente en una fila determinada, la imagen se voltea horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-122">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>

![Ilustración en la que se muestra la imagen base repetida horizontalmente, pero las instancias con números pares se invierten horizontalmente](images/tile3.png)

 

## <a name="flipping-an-image-vertically-while-tiling"></a><span data-ttu-id="fd00c-124">Voltear una imagen verticalmente mientras se organiza en mosaico</span><span class="sxs-lookup"><span data-stu-id="fd00c-124">Flipping an Image Vertically While Tiling</span></span>

<span data-ttu-id="fd00c-125">En este ejemplo se usa una imagen 75 × 75 para rellenar un rectángulo de 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="fd00c-125">This example uses a 75 ×75 image to fill a 200 ×200 rectangle.</span></span> <span data-ttu-id="fd00c-126">El modo de ajuste se establece para voltear la imagen verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-126">The wrap mode is set to flip the image vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="fd00c-127">En la ilustración siguiente se muestra cómo se coloca en mosaico el rectángulo con la imagen.</span><span class="sxs-lookup"><span data-stu-id="fd00c-127">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="fd00c-128">Tenga en cuenta que cuando se desplaza de un mosaico al siguiente en una columna determinada, la imagen se voltea verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-128">Note that as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![Ilustración en la que se muestra la imagen base repetida horizontal y verticalmente, pero las filas pares se invierten verticalmente](images/tile4.png)

 

## <a name="flipping-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="fd00c-130">Voltear una imagen horizontal y verticalmente mientras se organiza en mosaico</span><span class="sxs-lookup"><span data-stu-id="fd00c-130">Flipping an Image Horizontally and Vertically While Tiling</span></span>

<span data-ttu-id="fd00c-131">En este ejemplo se usa una imagen 75 × 75 para colocar en mosaico un rectángulo de 200 × 200.</span><span class="sxs-lookup"><span data-stu-id="fd00c-131">This example uses a 75 ×75 image to tile a 200 ×200 rectangle.</span></span> <span data-ttu-id="fd00c-132">El modo de ajuste se establece para voltear la imagen tanto horizontal como verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-132">The wrap mode is set to flip the image both horizontally and vertically.</span></span>


```
Image image(L"HouseAndTree.png");
TextureBrush tBrush(&image);
Pen blackPen(Color(255, 0, 0, 0));
stat = tBrush.SetWrapMode(WrapModeTileFlipXY);
stat = graphics.FillRectangle(&tBrush, Rect(0, 0, 200, 200));
stat = graphics.DrawRectangle(&blackPen, Rect(0, 0, 200, 200));
```



<span data-ttu-id="fd00c-133">En la ilustración siguiente se muestra cómo se coloca el rectángulo en mosaico por la imagen.</span><span class="sxs-lookup"><span data-stu-id="fd00c-133">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="fd00c-134">Tenga en cuenta que cuando se desplaza de un mosaico al siguiente en una fila determinada, la imagen se voltea horizontalmente y, cuando se desplaza de un mosaico al siguiente en una columna determinada, la imagen se voltea verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fd00c-134">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>

![la ilustración en la que se muestran las instancias alternas de la imagen base de cada fila se voltea horizontalmente, y las filas alternas se voltean verticalmente.](images/tile5.png)

 

 



