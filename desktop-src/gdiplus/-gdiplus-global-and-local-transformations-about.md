---
description: Una transformación global es una transformación que se aplica a todos los elementos dibujados por un objeto gráfico determinado.
ms.assetid: 9f744c2a-f1f3-4a7e-ab0c-37aa1df01623
title: Transformaciones globales y locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2682fef6a6236b9da7ec0ec1e5ab5484ad9f90d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561233"
---
# <a name="global-and-local-transformations"></a><span data-ttu-id="addd9-103">Transformaciones globales y locales</span><span class="sxs-lookup"><span data-stu-id="addd9-103">Global and Local Transformations</span></span>

<span data-ttu-id="addd9-104">Una transformación global es una transformación que se aplica a todos los elementos dibujados por un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) determinado.</span><span class="sxs-lookup"><span data-stu-id="addd9-104">A global transformation is a transformation that applies to every item drawn by a given [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="addd9-105">Para crear una transformación global, construya un objeto **Graphics** y, a continuación, llame a su método [**Graphics:: SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) .</span><span class="sxs-lookup"><span data-stu-id="addd9-105">To create a global transformation, construct a **Graphics** object, and then call its [**Graphics::SetTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settransform) method.</span></span> <span data-ttu-id="addd9-106">El método **Graphics:: SetTransform** manipula un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) que está asociado al objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="addd9-106">The **Graphics::SetTransform** method manipulates a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object that is associated with the **Graphics** object.</span></span> <span data-ttu-id="addd9-107">La transformación almacenada en ese objeto de **matriz** se denomina *transformación universal*.</span><span class="sxs-lookup"><span data-stu-id="addd9-107">The transformation stored in that **Matrix** object is called the *world transformation*.</span></span> <span data-ttu-id="addd9-108">La transformación universal puede ser una transformación afín simple o una secuencia compleja de transformaciones afines, pero independientemente de su complejidad, la transformación universal se almacena en un objeto de **matriz** único.</span><span class="sxs-lookup"><span data-stu-id="addd9-108">The world transformation can be a simple affine transformation or a complex sequence of affine transformations, but regardless of its complexity, the world transformation is stored in a single **Matrix** object.</span></span>

<span data-ttu-id="addd9-109">La clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona varios métodos para crear una transformación universal compuesta: [**Graphics:: MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics:: ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform)y [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span><span class="sxs-lookup"><span data-stu-id="addd9-109">The [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class provides several methods for building up a composite world transformation: [**Graphics::MultiplyTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-multiplytransform), [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform), [**Graphics::ScaleTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-scaletransform), and [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform).</span></span> <span data-ttu-id="addd9-110">En el ejemplo siguiente se dibuja una elipse dos veces: una vez antes de crear una transformación universal y otra después de.</span><span class="sxs-lookup"><span data-stu-id="addd9-110">The following example draws an ellipse twice: once before creating a world transformation and once after.</span></span> <span data-ttu-id="addd9-111">La transformación se escala primero mediante un factor de 0,5 en la dirección y, a continuación, convierte 50 unidades en la dirección x y, a continuación, gira 30 grados.</span><span class="sxs-lookup"><span data-stu-id="addd9-111">The transformation first scales by a factor of 0.5 in the y direction, then translates 50 units in the x direction, and then rotates 30 degrees.</span></span>


```
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
myGraphics.ScaleTransform(1.0f, 0.5f);
myGraphics.TranslateTransform(50.0f, 0.0f, MatrixOrderAppend);
myGraphics.RotateTransform(30.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myPen, 0, 0, 100, 50);
```



<span data-ttu-id="addd9-112">En la ilustración siguiente se muestra la elipse original y la elipse transformada.</span><span class="sxs-lookup"><span data-stu-id="addd9-112">The following illustration shows the original ellipse and the transformed ellipse.</span></span>

![captura de pantalla de una ventana que contiene dos puntos suspensivos superpuestos; uno es más estrecho y girado](images/aboutgdip05-art14.png)

> [!Note]  
> <span data-ttu-id="addd9-114">En el ejemplo anterior, la elipse gira sobre el origen del sistema de coordenadas, que se encuentra en la esquina superior izquierda del área cliente.</span><span class="sxs-lookup"><span data-stu-id="addd9-114">In the previous example, the ellipse is rotated about the origin of the coordinate system, which is at the upper–left corner of the client area.</span></span> <span data-ttu-id="addd9-115">Esto genera un resultado diferente que la rotación de la elipse sobre su propio centro.</span><span class="sxs-lookup"><span data-stu-id="addd9-115">This produces a different result than rotating the ellipse about its own center.</span></span>

 

<span data-ttu-id="addd9-116">Una transformación local es una transformación que se aplica a un elemento específico que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="addd9-116">A local transformation is a transformation that applies to a specific item to be drawn.</span></span> <span data-ttu-id="addd9-117">Por ejemplo, un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) tiene un método [**GraphicsPath:: transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) que le permite transformar los puntos de datos de esa ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="addd9-117">For example, a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object has a [**GraphicsPath::Transform**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-transform) method that allows you to transform the data points of that path.</span></span> <span data-ttu-id="addd9-118">En el ejemplo siguiente se dibuja un rectángulo sin transformación y un trazado con una transformación de giro.</span><span class="sxs-lookup"><span data-stu-id="addd9-118">The following example draws a rectangle with no transformation and a path with a rotation transformation.</span></span> <span data-ttu-id="addd9-119">(Suponga que no hay una transformación universal).</span><span class="sxs-lookup"><span data-stu-id="addd9-119">(Assume that there is no world transformation.)</span></span>


```
 
Matrix myMatrix;
myMatrix.Rotate(45.0f);
myGraphicsPath.Transform(&myMatrix);
myGraphics.DrawRectangle(&myPen, 10, 10, 100, 50);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="addd9-120">Puede combinar la transformación universal con transformaciones locales para lograr una variedad de resultados.</span><span class="sxs-lookup"><span data-stu-id="addd9-120">You can combine the world transformation with local transformations to achieve a variety of results.</span></span> <span data-ttu-id="addd9-121">Por ejemplo, puede usar la transformación universal para revisar el sistema de coordenadas y usar transformaciones locales para girar y escalar objetos dibujados en el nuevo sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="addd9-121">For example, you can use the world transformation to revise the coordinate system and use local transformations to rotate and scale objects drawn on the new coordinate system.</span></span>

<span data-ttu-id="addd9-122">Supongamos que desea un sistema de coordenadas que tenga su origen de 200 píxeles desde el borde izquierdo del área cliente y 150 píxeles desde la parte superior del área cliente.</span><span class="sxs-lookup"><span data-stu-id="addd9-122">Suppose you want a coordinate system that has its origin 200 pixels from the left edge of the client area and 150 pixels from the top of the client area.</span></span> <span data-ttu-id="addd9-123">Además, supongamos que desea que la unidad de medida sea el píxel, con el eje x que apunta hacia la derecha y el eje y que señala hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="addd9-123">Furthermore, assume that you want the unit of measure to be the pixel, with the x-axis pointing to the right and the y-axis pointing up.</span></span> <span data-ttu-id="addd9-124">El sistema de coordenadas predeterminado tiene el eje y apunta hacia abajo, por lo que debe realizar una reflexión en el eje horizontal.</span><span class="sxs-lookup"><span data-stu-id="addd9-124">The default coordinate system has the y-axis pointing down, so you need to perform a reflection across the horizontal axis.</span></span> <span data-ttu-id="addd9-125">En la ilustración siguiente se muestra la matriz de este tipo de reflexión.</span><span class="sxs-lookup"><span data-stu-id="addd9-125">The following illustration shows the matrix of such a reflection.</span></span>

![Ilustración en la que se muestra una matriz de tres por tres](images/aboutgdip05-art15.png)

<span data-ttu-id="addd9-127">A continuación, supongamos que necesita realizar una traducción de 200 unidades a la derecha y las unidades de 150.</span><span class="sxs-lookup"><span data-stu-id="addd9-127">Next, assume you need to perform a translation 200 units to the right and 150 units down.</span></span>

<span data-ttu-id="addd9-128">En el ejemplo siguiente se establece el sistema de coordenadas que se acaba de describir estableciendo la transformación universal de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="addd9-128">The following example establishes the coordinate system just described by setting the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>


```
Matrix myMatrix(1.0f, 0.0f, 0.0f, -1.0f, 0.0f, 0.0f);
myGraphics.SetTransform(&myMatrix);
myGraphics.TranslateTransform(200.0f, 150.0f, MatrixOrderAppend);
```



<span data-ttu-id="addd9-129">El código siguiente (colocado después del código en el ejemplo anterior) crea una ruta de acceso que consta de un único rectángulo con la esquina inferior izquierda en el origen del nuevo sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="addd9-129">The following code (placed after the code in the preceding example) creates a path that consists of a single rectangle with its lower-left corner at the origin of the new coordinate system.</span></span> <span data-ttu-id="addd9-130">El rectángulo se rellena una vez sin transformación local y una vez con una transformación local.</span><span class="sxs-lookup"><span data-stu-id="addd9-130">The rectangle is filled once with no local transformation and once with a local transformation.</span></span> <span data-ttu-id="addd9-131">La transformación local se compone de un escalado horizontal mediante un factor de 2 seguido de una rotación de 30 grados.</span><span class="sxs-lookup"><span data-stu-id="addd9-131">The local transformation consists of a horizontal scaling by a factor of 2 followed by a 30-degree rotation.</span></span>


```
// Create the path.
GraphicsPath myGraphicsPath;
Rect myRect(0, 0, 60, 60);
myGraphicsPath.AddRectangle(myRect);

// Fill the path on the new coordinate system.
// No local transformation
myGraphics.FillPath(&mySolidBrush1, &myGraphicsPath);

// Transform the path.
Matrix myPathMatrix;
myPathMatrix.Scale(2, 1);
myPathMatrix.Rotate(30, MatrixOrderAppend);
myGraphicsPath.Transform(&myPathMatrix);

// Fill the transformed path on the new coordinate system.
myGraphics.FillPath(&mySolidBrush2, &myGraphicsPath);
```



<span data-ttu-id="addd9-132">En la ilustración siguiente se muestra el nuevo sistema de coordenadas y los dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="addd9-132">The following illustration shows the new coordinate system and the two rectangles.</span></span>

![captura de pantalla de un eje x e y, y un cuadrado azul superpuesto con un rectagle semitransparente girado en torno a la esquina inferior izquierda](images/aboutgdip05-art16.png)

 

 



