---
description: Windows GDI+ proporciona las clases Image y Bitmap para almacenar y manipular imágenes.
ms.assetid: fcd7f3d9-8bad-44f8-8c9c-c2f5df4a7241
title: Uso de una matriz de colores para transformar un color único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db56d0a64c36c08a5415d76e3fb184158d473268
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557670"
---
# <a name="using-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="a437d-103">Uso de una matriz de colores para transformar un color único</span><span class="sxs-lookup"><span data-stu-id="a437d-103">Using a Color Matrix to Transform a Single Color</span></span>

<span data-ttu-id="a437d-104">Windows GDI+ proporciona las clases [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) y [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para almacenar y manipular imágenes.</span><span class="sxs-lookup"><span data-stu-id="a437d-104">Windows GDI+ provides the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) classes for storing and manipulating images.</span></span> <span data-ttu-id="a437d-105">Los objetos **Image** y **Bitmap** almacenan el color de cada píxel como un número de 32 bits: 8 bits para rojo, verde, azul y alfa.</span><span class="sxs-lookup"><span data-stu-id="a437d-105">**Image** and **Bitmap** objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="a437d-106">Cada uno de los cuatro componentes es un número del 0 al 255, con 0 que no representa ninguna intensidad y 255 que representa intensidad total.</span><span class="sxs-lookup"><span data-stu-id="a437d-106">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="a437d-107">El componente alfa especifica la transparencia del color: 0 es totalmente transparente y 255 es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="a437d-107">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>

<span data-ttu-id="a437d-108">Un vector de color es una tupla de 4 de la forma (rojo, verde, azul, alfa).</span><span class="sxs-lookup"><span data-stu-id="a437d-108">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="a437d-109">Por ejemplo, el vector de color (0, 255, 0, 255) representa un color opaco que no tiene rojo o azul, pero tiene una intensidad de color verde.</span><span class="sxs-lookup"><span data-stu-id="a437d-109">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>

<span data-ttu-id="a437d-110">Otra Convención para representar colores utiliza el número 1 para la intensidad máxima y el número 0 para la intensidad mínima.</span><span class="sxs-lookup"><span data-stu-id="a437d-110">Another convention for representing colors uses the number 1 for maximum intensity and the number 0 for minimum intensity.</span></span> <span data-ttu-id="a437d-111">Con esa Convención, el color descrito en el párrafo anterior se representaría mediante el vector (0, 1, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a437d-111">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="a437d-112">GDI+ utiliza la Convención de 1 como intensidad completa cuando realiza transformaciones de color.</span><span class="sxs-lookup"><span data-stu-id="a437d-112">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>

<span data-ttu-id="a437d-113">Puede aplicar transformaciones lineales (giro, escala y similares) a vectores de color multiplicando por una matriz de 4 x 4.</span><span class="sxs-lookup"><span data-stu-id="a437d-113">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying by a 4 ×4 matrix.</span></span> <span data-ttu-id="a437d-114">Sin embargo, no puede usar una matriz de 4 × 4 para realizar una traducción (no lineal).</span><span class="sxs-lookup"><span data-stu-id="a437d-114">However, you cannot use a 4 ×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="a437d-115">Si agrega una quinta coordenada ficticia (por ejemplo, el número 1) a cada uno de los vectores de color, puede utilizar una matriz de 5 × 5 para aplicar cualquier combinación de transformaciones lineales y traducciones.</span><span class="sxs-lookup"><span data-stu-id="a437d-115">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5 ×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="a437d-116">Una transformación formada por una transformación lineal seguida de una traducción se denomina transformación afín.</span><span class="sxs-lookup"><span data-stu-id="a437d-116">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span> <span data-ttu-id="a437d-117">Una matriz de 5 × 5 que representa una transformación afín se denomina matriz homogénea para una transformación de 4 espacios.</span><span class="sxs-lookup"><span data-stu-id="a437d-117">A 5 ×5 matrix that represents an affine transformation is called a homogeneous matrix for a 4-space transformation.</span></span> <span data-ttu-id="a437d-118">El elemento de la quinta fila y la quinta columna de una matriz homogénea 5 × 5 deben ser 1 y todas las demás entradas de la quinta columna deben ser 0.</span><span class="sxs-lookup"><span data-stu-id="a437d-118">The element in the fifth row and fifth column of a 5 ×5 homogeneous matrix must be 1, and all of the other entries in the fifth column must be 0.</span></span>

<span data-ttu-id="a437d-119">Por ejemplo, supongamos que desea empezar con el color (0,2, 0,0, 0,4, 1,0) y aplicar las transformaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a437d-119">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>

1.  <span data-ttu-id="a437d-120">Doble del componente rojo</span><span class="sxs-lookup"><span data-stu-id="a437d-120">Double the red component</span></span>
2.  <span data-ttu-id="a437d-121">Agregar 0,2 a los componentes rojo, verde y azul</span><span class="sxs-lookup"><span data-stu-id="a437d-121">Add 0.2 to the red, green, and blue components</span></span>

<span data-ttu-id="a437d-122">La multiplicación de matrices siguiente realizará el par de transformaciones en el orden mostrado.</span><span class="sxs-lookup"><span data-stu-id="a437d-122">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>

![Ilustración en la que se muestra una matriz 5x1 de números multiplicada por una matriz 5x5 para crear una nueva matriz 5x1](images/recoloring01.png)

<span data-ttu-id="a437d-124">Los elementos de una matriz de colores se indexan (de base cero) por fila y después por columna.</span><span class="sxs-lookup"><span data-stu-id="a437d-124">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="a437d-125">Por ejemplo, la entrada de la quinta fila y la tercera columna de la matriz M se indican mediante M \[ 4 \] \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="a437d-125">For example, the entry in the fifth row and third column of matrix M is denoted by M\[4\]\[2\].</span></span>

<span data-ttu-id="a437d-126">La matriz de identidad 5 × 5 (que se muestra en la ilustración siguiente) tiene un 1 en la diagonal y 0s en cualquier otro lugar.</span><span class="sxs-lookup"><span data-stu-id="a437d-126">The 5 ×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="a437d-127">Si multiplica un vector de color por la matriz de identidad, el vector de color no cambia.</span><span class="sxs-lookup"><span data-stu-id="a437d-127">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="a437d-128">Una manera cómoda de formar la matriz de una transformación de color es comenzar con la matriz de identidad y hacer un pequeño cambio que genere la transformación deseada.</span><span class="sxs-lookup"><span data-stu-id="a437d-128">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>

![Ilustración que muestra una matriz de identidad 5x5; 1S en la parte superior izquierda a la diagonal inferior derecha y 0s en cualquier otro lugar](images/recoloring02.png)

<span data-ttu-id="a437d-130">Para obtener una explicación más detallada de las matrices y las transformaciones, vea [sistemas de coordenadas y transformaciones](-gdiplus-coordinate-systems-and-transformations-about.md).</span><span class="sxs-lookup"><span data-stu-id="a437d-130">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](-gdiplus-coordinate-systems-and-transformations-about.md).</span></span>

<span data-ttu-id="a437d-131">En el siguiente ejemplo se toma una imagen de un color (0,2, 0,0, 0,4, 1,0) y se aplica la transformación descrita en los párrafos anteriores.</span><span class="sxs-lookup"><span data-stu-id="a437d-131">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>


```
Image            image(L"InputColor.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();

ColorMatrix colorMatrix = {
   2.0f, 0.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
   0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
   0.2f, 0.2f, 0.2f, 0.0f, 1.0f};
   
imageAttributes.SetColorMatrix(
   &colorMatrix, 
   ColorMatrixFlagsDefault,
   ColorAdjustTypeBitmap);
   
graphics.DrawImage(&image, 10, 10);

graphics.DrawImage(
   &image, 
   Rect(120, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="a437d-132">En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen transformada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="a437d-132">The following illustration shows the original image on the left and the transformed image on the right.</span></span>

![<span data-ttu-id="a437d-133">Ilustración que muestra un rectángulo relleno con un color sólido oscuro y, a continuación, un relleno con un color sólido más claro</span><span class="sxs-lookup"><span data-stu-id="a437d-133">illustration showing a rectangle filled by a dark solid color and then one filled by a lighter solid color</span></span> ](images/colortrans1.png)

<span data-ttu-id="a437d-134">En el código del ejemplo anterior se usan los pasos siguientes para realizar el recoloreado:</span><span class="sxs-lookup"><span data-stu-id="a437d-134">The code in the preceding example uses the following steps to perform the recoloring:</span></span>

1.  <span data-ttu-id="a437d-135">Inicialice una estructura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) .</span><span class="sxs-lookup"><span data-stu-id="a437d-135">Initialize a [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure.</span></span>
2.  <span data-ttu-id="a437d-136">Cree un objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y pase la dirección de la estructura [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) al método [**ImageAttributes:: SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) del objeto **ImageAttributes** .</span><span class="sxs-lookup"><span data-stu-id="a437d-136">Create an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object and pass the address of the [**ColorMatrix**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormatrix) structure to the [**ImageAttributes::SetColorMatrix**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setcolormatrix) method of the **ImageAttributes** object.</span></span>
3.  <span data-ttu-id="a437d-137">Pase la dirección del objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) al método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methods de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a437d-137">Pass the address of the [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

 

 



