---
description: Puede rellenar una forma cerrada con una textura mediante la clase Image y la clase TextureBrush.
ms.assetid: 12e1e132-a93f-4438-8a1d-9036a43a8fd8
title: Rellenar una forma con una textura de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3f1bf6ba04311310ab1985de1d1aaccd45db43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156188"
---
# <a name="filling-a-shape-with-an-image-texture"></a><span data-ttu-id="f2e92-103">Rellenar una forma con una textura de imagen</span><span class="sxs-lookup"><span data-stu-id="f2e92-103">Filling a Shape with an Image Texture</span></span>

<span data-ttu-id="f2e92-104">Puede rellenar una forma cerrada con una textura mediante la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y la clase [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="f2e92-104">You can fill a closed shape with a texture by using the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) class.</span></span>

<span data-ttu-id="f2e92-105">En el ejemplo siguiente se rellena una elipse con una imagen.</span><span class="sxs-lookup"><span data-stu-id="f2e92-105">The following example fills an ellipse with an image.</span></span> <span data-ttu-id="f2e92-106">El código crea un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y, a continuación, pasa la dirección de ese objeto de **imagen** como argumento a un constructor [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) .</span><span class="sxs-lookup"><span data-stu-id="f2e92-106">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, and then passes the address of that **Image** object as an argument to a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) constructor.</span></span> <span data-ttu-id="f2e92-107">La tercera instrucción de código escala la imagen y la cuarta instrucción rellena la elipse con copias repetidas de la imagen escalada:</span><span class="sxs-lookup"><span data-stu-id="f2e92-107">The third code statement scales the image, and the fourth statement fills the ellipse with repeated copies of the scaled image:</span></span>


```
Image image(L"ImageFile.jpg");
TextureBrush tBrush(&image);
stat = tBrush.SetTransform(&Matrix(75.0/640.0, 0.0f, 0.0f,
   75.0/480.0, 0.0f, 0.0f));
stat = graphics.FillEllipse(&tBrush,Rect(0, 150, 150, 250));
```



<span data-ttu-id="f2e92-108">En el ejemplo de código anterior, el método [**TextureBrush:: SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) establece la transformación que se aplica a la imagen antes de dibujarse.</span><span class="sxs-lookup"><span data-stu-id="f2e92-108">In the preceding code example, the [**TextureBrush::SetTransform**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-texturebrush-settransform) method sets the transformation that is applied to the image before it is drawn.</span></span> <span data-ttu-id="f2e92-109">Supongamos que la imagen original tiene un ancho de 640 píxeles y un alto de 480 píxeles.</span><span class="sxs-lookup"><span data-stu-id="f2e92-109">Assume that the original image has a width of 640 pixels and a height of 480 pixels.</span></span> <span data-ttu-id="f2e92-110">La transformación reduce la imagen a 75 × 75, estableciendo los valores de escalado horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="f2e92-110">The transform shrinks the image to 75 ×75, by setting the horizontal and vertical scaling values.</span></span>

> [!Note]  
> <span data-ttu-id="f2e92-111">En el ejemplo anterior, el tamaño de la imagen es 75 × 75 y el tamaño de la elipse es 150 × 250.</span><span class="sxs-lookup"><span data-stu-id="f2e92-111">In the preceding example, the image size is 75 ×75, and the ellipse size is 150 ×250.</span></span> <span data-ttu-id="f2e92-112">Dado que la imagen es más pequeña que la elipse que está rellenando, la elipse se coloca en mosaico con la imagen.</span><span class="sxs-lookup"><span data-stu-id="f2e92-112">Because the image is smaller than the ellipse it is filling, the ellipse is tiled with the image.</span></span> <span data-ttu-id="f2e92-113">La disposición en mosaico significa que la imagen se repite horizontal y verticalmente hasta que se alcanza el límite de la forma.</span><span class="sxs-lookup"><span data-stu-id="f2e92-113">Tiling means that the image is repeated horizontally and vertically until the boundary of the shape is reached.</span></span> <span data-ttu-id="f2e92-114">Para obtener más información sobre el mosaico, vea [organizar una forma en mosaico con una imagen](-gdiplus-tiling-a-shape-with-an-image-use.md).</span><span class="sxs-lookup"><span data-stu-id="f2e92-114">For more information on tiling, see [Tiling a Shape with an Image](-gdiplus-tiling-a-shape-with-an-image-use.md).</span></span>

 

 

 



