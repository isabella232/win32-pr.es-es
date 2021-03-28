---
description: La clase Bitmap (que hereda de la clase Image) y la clase ImageAttributes proporcionan funcionalidad para obtener y establecer valores de píxeles.
ms.assetid: e3d67431-6098-4b2a-8910-5695a8473216
title: Uso una matriz de colores para establecer valores alfa en imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81180b1f09b11e37b322e37106dab1879a00bbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541438"
---
# <a name="using-a-color-matrix-to-set-alpha-values-in-images"></a><span data-ttu-id="ed965-103">Uso una matriz de colores para establecer valores alfa en imágenes</span><span class="sxs-lookup"><span data-stu-id="ed965-103">Using a Color Matrix to Set Alpha Values in Images</span></span>

<span data-ttu-id="ed965-104">La clase [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) (que hereda de la clase [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) ) y la clase [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) proporcionan funcionalidad para obtener y establecer valores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ed965-104">The [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class (which inherits from the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class) and the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class provide functionality for getting and setting pixel values.</span></span> <span data-ttu-id="ed965-105">Puede usar la clase **ImageAttributes** para modificar los valores alfa de una imagen completa, o puede llamar al método [**Bitmap:: setPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) de la clase **Bitmap** para modificar los valores individuales de los píxeles.</span><span class="sxs-lookup"><span data-stu-id="ed965-105">You can use the **ImageAttributes** class to modify the alpha values for an entire image, or you can call the [**Bitmap::SetPixel**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-bitmap-setpixel) method of the **Bitmap** class to modify individual pixel values.</span></span> <span data-ttu-id="ed965-106">Para obtener más información sobre cómo establecer valores de píxeles individuales, vea [establecer los valores alfa de píxeles individuales](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span><span class="sxs-lookup"><span data-stu-id="ed965-106">For more information on setting individual pixel values, see [Setting the Alpha Values of Individual Pixels](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md).</span></span>

<span data-ttu-id="ed965-107">En el ejemplo siguiente se dibuja una línea negra ancha y, a continuación, se muestra una imagen opaca que cubre parte de esa línea.</span><span class="sxs-lookup"><span data-stu-id="ed965-107">The following example draws a wide black line and then displays an opaque image that covers part of that line.</span></span>


```
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw an image that covers part of the black line.
graphics.DrawImage(&bitmap,
   Rect(30, 0, bitmap.GetWidth(), bitmap.GetHeight()));
```



<span data-ttu-id="ed965-108">En la ilustración siguiente se muestra la imagen resultante, que se dibuja en (30, 0).</span><span class="sxs-lookup"><span data-stu-id="ed965-108">The following illustration shows the resulting image, which is drawn at (30, 0).</span></span> <span data-ttu-id="ed965-109">Tenga en cuenta que la línea de color negro ancho no se muestra a través de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ed965-109">Note that the wide black line doesn't show through the image.</span></span>

![Ilustración en la que se muestra una imagen opaca que se superpone a un rectángulo fino, ancho y negro](images/image1.png)

<span data-ttu-id="ed965-111">La clase [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) tiene muchas propiedades que se pueden utilizar para modificar imágenes durante la representación.</span><span class="sxs-lookup"><span data-stu-id="ed965-111">The [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) class has many properties that you can use to modify images during rendering.</span></span> <span data-ttu-id="ed965-112">En el ejemplo siguiente, se usa un objeto **ImageAttributes** para establecer todos los valores alfa en el 80 por ciento de lo que eran.</span><span class="sxs-lookup"><span data-stu-id="ed965-112">In the following example, an **ImageAttributes** object is used to set all the alpha values to 80 percent of what they were.</span></span> <span data-ttu-id="ed965-113">Esto se hace inicializando una matriz de colores y estableciendo el valor de escala alfa en la matriz en 0,8.</span><span class="sxs-lookup"><span data-stu-id="ed965-113">This is done by initializing a color matrix and setting the alpha scaling value in the matrix to 0.8.</span></span> <span data-ttu-id="ed965-114">La dirección de la matriz de colores se pasa al método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) del objeto **ImageAttributes** y la dirección del objeto **ImageAttributes** se pasa al método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ed965-114">The address of the color matrix is passed to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object, and the address of the **ImageAttributes** object is passed to the [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstrect_)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
// Create a Bitmap object and load it with the texture image.
Bitmap bitmap(L"Texture1.jpg");
Pen pen(Color(255, 0, 0, 0), 25);
// Initialize the color matrix.
// Notice the value 0.8 in row 4, column 4.
ColorMatrix colorMatrix = {1.0f, 0.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.8f, 0.0f,
                           0.0f, 0.0f, 0.0f, 0.0f, 1.0f};
// Create an ImageAttributes object and set its color matrix.
ImageAttributes imageAtt;
imageAtt.SetColorMatrix(&colorMatrix, ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
// First draw a wide black line.
graphics.DrawLine(&pen, Point(10, 35), Point(200, 35));
// Now draw the semitransparent bitmap image.
INT iWidth = bitmap.GetWidth();
INT iHeight = bitmap.GetHeight();
graphics.DrawImage(
   &bitmap, 
   Rect(30, 0, iWidth, iHeight),  // Destination rectangle
   0,                             // Source rectangle X 
   0,                             // Source rectangle Y
   iWidth,                        // Source rectangle width
   iHeight,                       // Source rectangle height
   UnitPixel, 
   &imageAtt);
```



<span data-ttu-id="ed965-115">Durante la representación, los valores alfa del mapa de bits se convierten al 80 por ciento de lo que eran.</span><span class="sxs-lookup"><span data-stu-id="ed965-115">During rendering, the alpha values in the bitmap are converted to 80 percent of what they were.</span></span> <span data-ttu-id="ed965-116">Esto da como resultado una imagen que se combina con el fondo.</span><span class="sxs-lookup"><span data-stu-id="ed965-116">This results in an image that is blended with the background.</span></span> <span data-ttu-id="ed965-117">Como se muestra en la siguiente ilustración, la imagen de mapa de bits es transparente; puede ver la línea negra sólida a través de ella.</span><span class="sxs-lookup"><span data-stu-id="ed965-117">As the following illustration shows, the bitmap image looks transparent; you can see the solid black line through it.</span></span>

![Ilustración similar a la anterior, pero la imagen es transparente para SEM](images/image2.png)

<span data-ttu-id="ed965-119">Cuando la imagen está sobre la parte blanca del fondo, la imagen se ha mezclado con el color blanco.</span><span class="sxs-lookup"><span data-stu-id="ed965-119">Where the image is over the white portion of the background, the image has been blended with the color white.</span></span> <span data-ttu-id="ed965-120">Cuando la imagen cruza la línea negra, la imagen se combina con el color negro.</span><span class="sxs-lookup"><span data-stu-id="ed965-120">Where the image crosses the black line, the image is blended with the color black.</span></span>

 

 



