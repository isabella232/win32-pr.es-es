---
description: Una figura cerrada, como un rectángulo o una elipse, consta de un contorno y un interior.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pinceles y formas rellenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559918"
---
# <a name="brushes-and-filled-shapes"></a><span data-ttu-id="07ba0-103">Pinceles y formas rellenas</span><span class="sxs-lookup"><span data-stu-id="07ba0-103">Brushes and Filled Shapes</span></span>

<span data-ttu-id="07ba0-104">Una figura cerrada, como un rectángulo o una elipse, consta de un contorno y un interior.</span><span class="sxs-lookup"><span data-stu-id="07ba0-104">A closed figure such as a rectangle or an ellipse consists of an outline and an interior.</span></span> <span data-ttu-id="07ba0-105">El contorno se dibuja con un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y el interior se rellena con un objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="07ba0-105">The outline is drawn with a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object and the interior is filled with a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="07ba0-106">Windows GDI+ proporciona varias clases de pincel para rellenar los interiores de las figuras cerradas: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)y [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="07ba0-106">Windows GDI+ provides several brush classes for filling the interiors of closed figures: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush), and [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush).</span></span> <span data-ttu-id="07ba0-107">Todas estas clases heredan de la clase **Brush** .</span><span class="sxs-lookup"><span data-stu-id="07ba0-107">All these classes inherit from the **Brush** class.</span></span> <span data-ttu-id="07ba0-108">En la ilustración siguiente se muestra un rectángulo relleno con un pincel sólido y una elipse rellena con un pincel de trama.</span><span class="sxs-lookup"><span data-stu-id="07ba0-108">The following illustration shows a rectangle filled with a solid brush and an ellipse filled with a hatch brush.</span></span>

![Ilustración que muestra un rectángulo azul y una elipse magenta rellena con un patrón de trama azul](images/aboutgdip02-art17.png)

 

-   [<span data-ttu-id="07ba0-110">Pinceles sólidos</span><span class="sxs-lookup"><span data-stu-id="07ba0-110">Solid Brushes</span></span>](#solid-brushes)
-   [<span data-ttu-id="07ba0-111">Pinceles de trama</span><span class="sxs-lookup"><span data-stu-id="07ba0-111">Hatch Brushes</span></span>](#hatch-brushes)
-   [<span data-ttu-id="07ba0-112">Pinceles de textura</span><span class="sxs-lookup"><span data-stu-id="07ba0-112">Texture Brushes</span></span>](#texture-brushes)
-   [<span data-ttu-id="07ba0-113">Pinceles de degradado</span><span class="sxs-lookup"><span data-stu-id="07ba0-113">Gradient Brushes</span></span>](#gradient-brushes)

## <a name="solid-brushes"></a><span data-ttu-id="07ba0-114">Pinceles sólidos</span><span class="sxs-lookup"><span data-stu-id="07ba0-114">Solid Brushes</span></span>

<span data-ttu-id="07ba0-115">Para rellenar una forma cerrada, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="07ba0-115">To fill a closed shape, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span> <span data-ttu-id="07ba0-116">El objeto **Graphics** proporciona métodos, como [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) y [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), y el objeto **Brush** almacena atributos del relleno, como el color y el patrón.</span><span class="sxs-lookup"><span data-stu-id="07ba0-116">The **Graphics** object provides methods, such as [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) and [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), and the **Brush** object stores attributes of the fill, such as color and pattern.</span></span> <span data-ttu-id="07ba0-117">La dirección del objeto **Brush** se pasa como uno de los argumentos al método Fill.</span><span class="sxs-lookup"><span data-stu-id="07ba0-117">The address of the **Brush** object is passed as one of the arguments to the fill method.</span></span> <span data-ttu-id="07ba0-118">En el ejemplo siguiente se rellena una elipse con un color rojo sólido.</span><span class="sxs-lookup"><span data-stu-id="07ba0-118">The following example fills an ellipse with a solid red color.</span></span>


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



<span data-ttu-id="07ba0-119">Tenga en cuenta que en el ejemplo anterior, el pincel es de tipo [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), que hereda de [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span><span class="sxs-lookup"><span data-stu-id="07ba0-119">Note that in the preceding example, the brush is of type [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), which inherits from [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).</span></span>

## <a name="hatch-brushes"></a><span data-ttu-id="07ba0-120">Pinceles de trama</span><span class="sxs-lookup"><span data-stu-id="07ba0-120">Hatch Brushes</span></span>

<span data-ttu-id="07ba0-121">Al rellenar una forma con un pincel de trama, se especifica un color de primer plano, un color de fondo y un estilo de trama.</span><span class="sxs-lookup"><span data-stu-id="07ba0-121">When you fill a shape with a hatch brush, you specify a foreground color, a background color, and a hatch style.</span></span> <span data-ttu-id="07ba0-122">El color de primer plano es el color del sombreado.</span><span class="sxs-lookup"><span data-stu-id="07ba0-122">The foreground color is the color of the hatching.</span></span>


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



<span data-ttu-id="07ba0-123">GDI+ proporciona más de 50 estilos de trama, que se especifican en [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span><span class="sxs-lookup"><span data-stu-id="07ba0-123">GDI+ provides more than 50 hatch styles, specified in [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle).</span></span> <span data-ttu-id="07ba0-124">Los tres estilos que se muestran en la siguiente ilustración son horizontal, ForwardDiagonal y Cross.</span><span class="sxs-lookup"><span data-stu-id="07ba0-124">The three styles shown in the following illustration are Horizontal, ForwardDiagonal, and Cross.</span></span>

![Ilustración que muestra tres elipses de color verde azulado, cada una con un estilo de trama diferente](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a><span data-ttu-id="07ba0-126">Pinceles de textura</span><span class="sxs-lookup"><span data-stu-id="07ba0-126">Texture Brushes</span></span>

<span data-ttu-id="07ba0-127">Con un pincel de textura, puede rellenar una forma con un patrón almacenado en un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="07ba0-127">With a texture brush, you can fill a shape with a pattern stored in a bitmap.</span></span> <span data-ttu-id="07ba0-128">Por ejemplo, supongamos que la siguiente imagen se almacena en un archivo de disco denominado MyTexture.bmp.</span><span class="sxs-lookup"><span data-stu-id="07ba0-128">For example, suppose the following picture is stored in a disk file named MyTexture.bmp.</span></span>

![captura de pantalla de un cuadrado pequeño relleno con varios colores](images/aboutgdip02-art19.png)

<span data-ttu-id="07ba0-130&quot;>En el ejemplo siguiente se rellena una elipse repitiendo la imagen almacenada en MyTexture.bmp.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;07ba0-130&quot;>The following example fills an ellipse by repeating the picture stored in MyTexture.bmp.</span></span>


```
Image myImage(L&quot;MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



<span data-ttu-id="07ba0-131">En la ilustración siguiente se muestra la elipse rellenada.</span><span class="sxs-lookup"><span data-stu-id="07ba0-131">The following illustration shows the filled ellipse.</span></span>

![Ilustración en la que se muestra una elipse rellena con el patrón definido previamente](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a><span data-ttu-id="07ba0-133">Pinceles de degradado</span><span class="sxs-lookup"><span data-stu-id="07ba0-133">Gradient Brushes</span></span>

<span data-ttu-id="07ba0-134">Puede usar un pincel de degradado para rellenar una forma con un color que cambie gradualmente de una parte de la forma a otra.</span><span class="sxs-lookup"><span data-stu-id="07ba0-134">You can use a gradient brush to fill a shape with a color that changes gradually from one part of the shape to another.</span></span> <span data-ttu-id="07ba0-135">Por ejemplo, un pincel de degradado horizontal cambiará el color a medida que se desplaza desde el lado izquierdo de una figura a la derecha.</span><span class="sxs-lookup"><span data-stu-id="07ba0-135">For example, a horizontal gradient brush will change color as you move from the left side of a figure to the right side.</span></span> <span data-ttu-id="07ba0-136">En el ejemplo siguiente se rellena una elipse con un pincel de degradado horizontal que cambia de azul a verde a medida que se desplaza desde el lado izquierdo de la elipse hasta el lado derecho.</span><span class="sxs-lookup"><span data-stu-id="07ba0-136">The following example fills an ellipse with a horizontal gradient brush that changes from blue to green as you move from the left side of the ellipse to the right side.</span></span>


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



<span data-ttu-id="07ba0-137">En la ilustración siguiente se muestra la elipse rellenada.</span><span class="sxs-lookup"><span data-stu-id="07ba0-137">The following illustration shows the filled ellipse.</span></span>

![Ilustración que muestra una elipse con un relleno de degradado: Blue de la derecha a la izquierda](images/aboutgdip02-art21.png)

<span data-ttu-id="07ba0-139">Un pincel de degradado de trazado puede configurarse para cambiar el color a medida que se desplaza desde el centro de una figura hacia el límite.</span><span class="sxs-lookup"><span data-stu-id="07ba0-139">A path gradient brush can be configured to change color as you move from the center of a figure toward the boundary.</span></span>

![Ilustration de una elipse azul oscuro en el centro, sombreando el azul claro en el borde](images/aboutgdip02-art22.png)

<span data-ttu-id="07ba0-141">Los pinceles de degradado de trazado son bastante flexibles.</span><span class="sxs-lookup"><span data-stu-id="07ba0-141">Path gradient brushes are quite flexible.</span></span> <span data-ttu-id="07ba0-142">El pincel de degradado que se usa para rellenar el triángulo de la siguiente ilustración cambia gradualmente de rojo en el centro a cada uno de tres colores diferentes en los vértices.</span><span class="sxs-lookup"><span data-stu-id="07ba0-142">The gradient brush used to fill the triangle in the following illustration changes gradually from red at the center to each of three different colors at the vertices.</span></span>

![Ilustración de un triángulo que está en rojo en el centro y sombreado a un color diferente en cada vértice](images/aboutgdip02-art23.png)

 

 



