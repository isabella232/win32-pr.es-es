---
description: El tema uso de una matriz de colores para establecer valores alfa en imágenes muestra un método no destructivo para cambiar los valores alfa de una imagen.
ms.assetid: 38c6254d-5191-4948-804a-1a4427aab7c6
title: Establecer los valores alfa de píxeles individuales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cd45bf32284ffc9a8cef13f368cff59e1e8a74f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541454"
---
# <a name="setting-the-alpha-values-of-individual-pixels"></a><span data-ttu-id="fa0ca-103">Establecer los valores alfa de píxeles individuales</span><span class="sxs-lookup"><span data-stu-id="fa0ca-103">Setting the Alpha Values of Individual Pixels</span></span>

<span data-ttu-id="fa0ca-104">El tema [uso de una matriz de colores para establecer valores alfa en imágenes](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) muestra un método no destructivo para cambiar los valores alfa de una imagen.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-104">The topic [Using a Color Matrix to Set Alpha Values in Images](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md) shows a nondestructive method for changing the alpha values of an image.</span></span> <span data-ttu-id="fa0ca-105">En el ejemplo de ese tema se representa una imagen de forma semitransparente, pero los datos de píxeles del mapa de bits no cambian.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-105">The example in that topic renders an image semitransparently, but the pixel data in the bitmap is not changed.</span></span> <span data-ttu-id="fa0ca-106">Los valores alfa solo se modifican durante la representación.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-106">The alpha values are altered only during rendering.</span></span>

<span data-ttu-id="fa0ca-107">En el ejemplo siguiente se muestra cómo cambiar los valores alfa de píxeles individuales.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-107">The following example shows how to change the alpha values of individual pixels.</span></span> <span data-ttu-id="fa0ca-108">En realidad, el código del ejemplo cambia la información alfa de un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="fa0ca-108">The code in the example actually changes the alpha information in a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="fa0ca-109">El enfoque es mucho más lento que el uso de una matriz de colores y un objeto [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) , pero proporciona control sobre los píxeles individuales del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-109">The approach is much slower than using a color matrix and an [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object but gives you control over the individual pixels in the bitmap.</span></span>


```
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
Color color, colorTemp;
for(INT iRow = 0; iRow < iHeight; iRow++)
{
   for(INT iColumn = 0; iColumn < iWidth; iColumn++)
   {
      bitmap.GetPixel(iColumn, iRow, &color);
      colorTemp.SetValue(color.MakeARGB(
         (BYTE)(255 * iColumn / iWidth), 
         color.GetRed(),
         color.GetGreen(),
         color.GetBlue()));
      bitmap.SetPixel(iColumn, iRow, colorTemp);
   }
}
// First draw a wide black line.
Pen pen(Color(255, 0, 0, 0), 25);
graphics.DrawLine(&pen, 10, 35, 200, 35);
// Now draw the modified bitmap.
graphics.DrawImage(&bitmap, 30, 0, iWidth, iHeight);
```



<span data-ttu-id="fa0ca-110">En la ilustración siguiente se muestra la imagen resultante.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-110">The following illustration shows the resulting image.</span></span>

![Ilustración en la que se muestra una imagen más opaca de izquierda a derecha, sobre un rectángulo negro](images/image3.png)

<span data-ttu-id="fa0ca-112">En el ejemplo de código anterior se usan bucles anidados para cambiar el valor alfa de cada píxel del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-112">The preceding code example uses nested loops to change the alpha value of each pixel in the bitmap.</span></span> <span data-ttu-id="fa0ca-113">Para cada píxel, [**Bitmap:: getPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) obtiene el color existente, [**color:: SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) crea un color temporal que contiene el nuevo valor alfa y [**Bitmap:: setPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) establece el nuevo color.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-113">For each pixel, [**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) gets the existing color, [**Color::SetValue**](/windows/desktop/api/Gdipluscolor/nf-gdipluscolor-color-setvalue) creates a temporary color that contains the new alpha value, and then [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) sets the new color.</span></span> <span data-ttu-id="fa0ca-114">El valor alfa se establece basándose en la columna del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-114">The alpha value is set based on the column of the bitmap.</span></span> <span data-ttu-id="fa0ca-115">En la primera columna, alfa se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-115">In the first column, alpha is set to 0.</span></span> <span data-ttu-id="fa0ca-116">En la última columna, alfa se establece en 255.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-116">In the last column, alpha is set to 255.</span></span> <span data-ttu-id="fa0ca-117">Por lo tanto, la imagen resultante pasa de ser completamente transparente (en el borde izquierdo) a totalmente opaca (en el borde derecho).</span><span class="sxs-lookup"><span data-stu-id="fa0ca-117">So the resulting image goes from fully transparent (on the left edge) to fully opaque (on the right edge).</span></span>

<span data-ttu-id="fa0ca-118">[**Bitmap:: getPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) y [**Bitmap:: setPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) proporcionan el control de los valores individuales de los píxeles.</span><span class="sxs-lookup"><span data-stu-id="fa0ca-118">[**Bitmap::GetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-getpixel) and [**Bitmap::SetPixel**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) give you control of the individual pixel values.</span></span> <span data-ttu-id="fa0ca-119">Sin embargo, el uso de **Bitmap:: getPixel** y **Bitmap:: setPixel** no es casi tan rápido como el uso de la clase [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y la estructura [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="fa0ca-119">However, using **Bitmap::GetPixel** and **Bitmap::SetPixel** is not nearly as fast as using the [**ImageAttributes**](/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class and the [**ColorMatrix**](/windows/desktop/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>

 

 



