---
description: La reasignación es el proceso de convertir los colores de una imagen según una tabla de reasignación de colores. La tabla de reasignación de colores es una matriz de estructuras ColorMap. Cada estructura ColorMap de la matriz tiene un miembro oldColor y un miembro newColor.
ms.assetid: 2b56ccd5-b9f3-4c5e-8a0b-4b3d1f2b7122
title: Uso de una tabla de reasignación de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1c07bc0a67a02ea07aeaa3931e661af5665e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154215"
---
# <a name="using-a-color-remap-table"></a><span data-ttu-id="372da-105">Uso de una tabla de reasignación de colores</span><span class="sxs-lookup"><span data-stu-id="372da-105">Using a Color Remap Table</span></span>

<span data-ttu-id="372da-106">La reasignación es el proceso de convertir los colores de una imagen según una tabla de reasignación de colores.</span><span class="sxs-lookup"><span data-stu-id="372da-106">Remapping is the process of converting the colors in an image according to a color remap table.</span></span> <span data-ttu-id="372da-107">La tabla de reasignación de colores es una matriz de estructuras [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="372da-107">The color remap table is an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="372da-108">Cada estructura **colormap** de la matriz tiene un miembro **oldColor** y un miembro **newColor** .</span><span class="sxs-lookup"><span data-stu-id="372da-108">Each **ColorMap** structure in the array has an **oldColor** member and a **newColor** member.</span></span>

<span data-ttu-id="372da-109">Cuando GDI+ dibuja una imagen, cada píxel de la imagen se compara con la matriz de colores antiguos.</span><span class="sxs-lookup"><span data-stu-id="372da-109">When GDI+ draws an image, each pixel of the image is compared to the array of old colors.</span></span> <span data-ttu-id="372da-110">Si el color de un píxel coincide con un color anterior, su color cambia al nuevo color correspondiente.</span><span class="sxs-lookup"><span data-stu-id="372da-110">If a pixel's color matches an old color, its color is changed to the corresponding new color.</span></span> <span data-ttu-id="372da-111">Los colores se cambian solo para la representación; los valores de color de la propia imagen (almacenados en un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) o de [**mapa de bits**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) ) no cambian.</span><span class="sxs-lookup"><span data-stu-id="372da-111">The colors are changed only for rendering — the color values of the image itself (stored in an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) or [**Bitmap**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object) are not changed.</span></span>

<span data-ttu-id="372da-112">Para dibujar una imagen reasignada, inicialice una matriz de estructuras [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="372da-112">To draw a remapped image, initialize an array of [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structures.</span></span> <span data-ttu-id="372da-113">Pase la dirección de esa matriz al método [**ImageAttributes:: SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) de un objeto [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) y, a continuación, pase la dirección del objeto **ImageAttributes** al método [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) Methods de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="372da-113">Pass the address of that array to the [**ImageAttributes::SetRemapTable**](/windows/win32/api/Gdiplusimageattributes/nf-gdiplusimageattributes-imageattributes-setremaptable) method of an [**ImageAttributes**](/windows/win32/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes) object, and then pass the address of the **ImageAttributes** object to the [DrawImage Methods](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) method of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

<span data-ttu-id="372da-114">En el ejemplo siguiente se crea un objeto de [**imagen**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) a partir del archivo RemapInput.bmp.</span><span class="sxs-lookup"><span data-stu-id="372da-114">The following example creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file RemapInput.bmp.</span></span> <span data-ttu-id="372da-115">El código crea una tabla de reasignación de colores formada por una única estructura [**colormap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) .</span><span class="sxs-lookup"><span data-stu-id="372da-115">The code creates a color remap table that consists of a single [**ColorMap**](/windows/win32/api/Gdipluscolormatrix/ns-gdipluscolormatrix-colormap) structure.</span></span> <span data-ttu-id="372da-116">El miembro **oldColor** de la estructura **colormap** es rojo y el miembro **newColor** es Blue.</span><span class="sxs-lookup"><span data-stu-id="372da-116">The **oldColor** member of the **ColorMap** structure is red, and the **newColor** member is blue.</span></span> <span data-ttu-id="372da-117">La imagen se dibuja una vez sin reasignar y una vez con reasignación.</span><span class="sxs-lookup"><span data-stu-id="372da-117">The image is drawn once without remapping and once with remapping.</span></span> <span data-ttu-id="372da-118">El proceso de reasignación cambia todos los píxeles rojos a azul.</span><span class="sxs-lookup"><span data-stu-id="372da-118">The remapping process changes all the red pixels to blue.</span></span>


```
Image            image(L"RemapInput.bmp");
ImageAttributes  imageAttributes;
UINT             width = image.GetWidth();
UINT             height = image.GetHeight();
ColorMap         colorMap[1];

colorMap[0].oldColor = Color(255, 255, 0, 0);  // opaque red
colorMap[0].newColor = Color(255, 0, 0, 255);  // opaque blue

imageAttributes.SetRemapTable(1, colorMap, ColorAdjustTypeBitmap);

graphics.DrawImage(&image, 10, 10, width, height);

graphics.DrawImage(
   &image, 
   Rect(150, 10, width, height),  // destination rectangle 
   0, 0,        // upper-left corner of source rectangle 
   width,       // width of source rectangle
   height,      // height of source rectangle
   UnitPixel,
   &imageAttributes);
```



<span data-ttu-id="372da-119">En la ilustración siguiente se muestra la imagen original de la izquierda y la imagen reasignada a la derecha.</span><span class="sxs-lookup"><span data-stu-id="372da-119">The following illustration shows the original image on the left and the remapped image on the right.</span></span>

![Ilustración en la que se muestran dos versiones de una imagen de multicolor: la región roja de la primera versión es azul en la segunda versión](images/colortrans7.png)

 

 



