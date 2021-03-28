---
description: Al rellenar una forma, debe pasar la dirección de un objeto Brush a uno de los métodos Fill de la clase Graphics.
ms.assetid: 42e36c32-ed20-4c5f-bcba-004d795babe3
title: Dibujar con pinceles opacos y semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877f922fff21f964349afbe1762cc458e60391b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156196"
---
# <a name="drawing-with-opaque-and-semitransparent-brushes"></a><span data-ttu-id="a9939-103">Dibujar con pinceles opacos y semitransparentes</span><span class="sxs-lookup"><span data-stu-id="a9939-103">Drawing with Opaque and Semitransparent Brushes</span></span>

<span data-ttu-id="a9939-104">Al rellenar una forma, debe pasar la dirección de un objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) a uno de los métodos Fill de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a9939-104">When you fill a shape, you must pass the address of a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="a9939-105">El único parámetro del constructor [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) es un objeto de [**color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="a9939-105">The one parameter of the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor is a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="a9939-106">Para rellenar una forma opaca, establezca el componente alfa del color en 255.</span><span class="sxs-lookup"><span data-stu-id="a9939-106">To fill an opaque shape, set the alpha component of the color to 255.</span></span> <span data-ttu-id="a9939-107">Para rellenar una forma semitransparente, establezca el componente alfa en cualquier valor entre 1 y 254.</span><span class="sxs-lookup"><span data-stu-id="a9939-107">To fill a semitransparent shape, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="a9939-108">Cuando se rellena una forma semitransparente, el color de la forma se mezcla con los colores del fondo.</span><span class="sxs-lookup"><span data-stu-id="a9939-108">When you fill a semitransparent shape, the color of the shape is blended with the colors of the background.</span></span> <span data-ttu-id="a9939-109">El componente alfa especifica cómo se mezclan los colores de la forma y el fondo; los valores alfa cercanos a 0 dan más peso en los colores de fondo y los valores alfa cercanos a 255 colocan más peso en el color de la forma.</span><span class="sxs-lookup"><span data-stu-id="a9939-109">The alpha component specifies how the shape and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the shape color.</span></span>

<span data-ttu-id="a9939-110">En el ejemplo siguiente se dibuja una imagen y, a continuación, se rellenan tres elipses que se superponen a la imagen.</span><span class="sxs-lookup"><span data-stu-id="a9939-110">The following example draws an image and then fills three ellipses that overlap the image.</span></span> <span data-ttu-id="a9939-111">La primera elipse usa un componente alfa de 255, por lo que es opaca.</span><span class="sxs-lookup"><span data-stu-id="a9939-111">The first ellipse uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="a9939-112">La segunda y tercera elipses usan un componente alfa de 128, por lo que son semitransparentes; puede ver la imagen de fondo a través de las elipses.</span><span class="sxs-lookup"><span data-stu-id="a9939-112">The second and third ellipses use an alpha component of 128, so they are semitransparent; you can see the background image through the ellipses.</span></span> <span data-ttu-id="a9939-113">La llamada a [**Graphics:: SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) hace que se realice la combinación de la tercera elipse junto con la corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="a9939-113">The call to [**Graphics::SetCompositingQuality**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third ellipse to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 50, 50, image.GetWidth(), image.GetHeight());
SolidBrush opaqueBrush(Color(255, 0, 0, 255));
SolidBrush semiTransBrush(Color(128, 0, 0, 255));
graphics.FillEllipse(&opaqueBrush, 35, 45, 45, 30);
graphics.FillEllipse(&semiTransBrush, 86, 45, 45, 30);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.FillEllipse(&semiTransBrush, 40, 90, 86, 30);
```



<span data-ttu-id="a9939-114">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="a9939-114">The following illustration shows the output of the preceding code.</span></span>

![Ilustración en la que se muestra una imagen superpuesta por tres elipses: una opaca, una ligeramente transparente, una muy transparente](images/compqualellipse.png)

 

 



