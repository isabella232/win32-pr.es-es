---
description: Al dibujar una línea, debe pasar la dirección de un objeto Pen al método DrawLine de la clase Graphics.
ms.assetid: 4524908f-f9c2-4807-b045-eb9e43a6668b
title: Dibujo de líneas opacas y semitransparentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f751e5808440c1051b3cd996f7ebcb2df0ccbcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557437"
---
# <a name="drawing-opaque-and-semitransparent-lines"></a><span data-ttu-id="ca685-103">Dibujo de líneas opacas y semitransparentes</span><span class="sxs-lookup"><span data-stu-id="ca685-103">Drawing Opaque and Semitransparent Lines</span></span>

<span data-ttu-id="ca685-104">Al dibujar una línea, debe pasar la dirección de un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) al método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ca685-104">When you draw a line, you must pass the address of a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="ca685-105">Uno de los parámetros del constructor **Pen** es un objeto de [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="ca685-105">One of the parameters of the **Pen** constructor is a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="ca685-106">Para dibujar una línea opaca, establezca el componente alfa del color en 255.</span><span class="sxs-lookup"><span data-stu-id="ca685-106">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="ca685-107">Para dibujar una línea semitransparente, establezca el componente alfa en cualquier valor entre 1 y 254.</span><span class="sxs-lookup"><span data-stu-id="ca685-107">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>

<span data-ttu-id="ca685-108">Cuando se dibuja una línea semitransparente sobre un fondo, el color de la línea se mezcla con los colores del fondo.</span><span class="sxs-lookup"><span data-stu-id="ca685-108">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="ca685-109">El componente alfa especifica cómo se mezclan los colores de línea y de fondo; los valores alfa cercanos a 0 dan más peso en los colores de fondo y los valores alfa cercanos a 255 colocan más peso en el color de línea.</span><span class="sxs-lookup"><span data-stu-id="ca685-109">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weigh on the line color.</span></span>

<span data-ttu-id="ca685-110">En el ejemplo siguiente se dibuja una imagen y, a continuación, se dibujan tres líneas que usan la imagen como fondo.</span><span class="sxs-lookup"><span data-stu-id="ca685-110">The following example draws an image and then draws three lines that use the image as a background.</span></span> <span data-ttu-id="ca685-111">La primera línea usa un componente alfa de 255, por lo que es opaca.</span><span class="sxs-lookup"><span data-stu-id="ca685-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="ca685-112">La segunda y tercera líneas usan un componente alfa de 128, por lo que son semitransparentes; puede ver la imagen de fondo a través de las líneas.</span><span class="sxs-lookup"><span data-stu-id="ca685-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="ca685-113">La llamada a [**Graphics:: SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) hace que la combinación de la tercera línea se realice junto con la corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="ca685-113">The call to [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality) causes the blending for the third line to be done in conjunction with gamma correction.</span></span>


```
Image image(L"Texture1.jpg");
graphics.DrawImage(&image, 10, 5, image.GetWidth(), image.GetHeight());
Pen opaquePen(Color(255, 0, 0, 255), 15);
Pen semiTransPen(Color(128, 0, 0, 255), 15);
graphics.DrawLine(&opaquePen, 0, 20, 100, 20);
graphics.DrawLine(&semiTransPen, 0, 40, 100, 40);
graphics.SetCompositingQuality(CompositingQualityGammaCorrected);
graphics.DrawLine(&semiTransPen, 0, 60, 100, 60);
```



<span data-ttu-id="ca685-114">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="ca685-114">The following illustration shows the output of the preceding code.</span></span>

![Ilustración en la que se muestra una imagen superpuesta por tres líneas anchas: una opaca, una ligeramente transparente y una muy transparente](images/compqualline.png)

 

 



