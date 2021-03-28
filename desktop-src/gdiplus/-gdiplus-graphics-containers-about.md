---
description: El estado de gráficos &\# 8212; la región de recorte, las transformaciones y la configuración de calidad &\# 8212; se almacenan en un objeto gráfico.
ms.assetid: 98b9fa12-02e7-42bf-9cbd-03ee696188f6
title: Contenedores de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8bf6469d0835137be1bb76b7727fd961bba16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549993"
---
# <a name="graphics-containers"></a><span data-ttu-id="26338-103">Contenedores de gráficos</span><span class="sxs-lookup"><span data-stu-id="26338-103">Graphics Containers</span></span>

<span data-ttu-id="26338-104">El estado de los gráficos (región de recorte, transformaciones y configuración de calidad) se almacena en un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="26338-104">Graphics state — clipping region, transformations, and quality settings — is stored in a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="26338-105">Windows GDI+ le permite reemplazar o aumentar temporalmente parte del estado en un objeto **gráfico** mediante un contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-105">Windows GDI+ allows you to temporarily replace or augment part of the state in a **Graphics** object by using a container.</span></span> <span data-ttu-id="26338-106">Para iniciar un contenedor, debe llamar al método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de un objeto **Graphics** y finalizar un contenedor llamando al método [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) .</span><span class="sxs-lookup"><span data-stu-id="26338-106">You start a container by calling the [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) method of a **Graphics** object, and you end a container by calling the [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) method.</span></span> <span data-ttu-id="26338-107">Entre los **gráficos:: BeginContainer** y **Graphics:: EndContainer**, cualquier cambio de estado que realice en el objeto de **gráficos** pertenece al contenedor y no sobrescribe el estado existente del objeto de **gráficos** .</span><span class="sxs-lookup"><span data-stu-id="26338-107">In between **Graphics::BeginContainer** and **Graphics::EndContainer**, any state changes you make to the **Graphics** object belong to the container and do not overwrite the existing state of the **Graphics** object.</span></span>

<span data-ttu-id="26338-108">En el ejemplo siguiente se crea un contenedor dentro de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="26338-108">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="26338-109">La transformación universal del objeto **Graphics** es una traducción de 200 unidades a la derecha y la transformación universal del contenedor es una unidad de traducción de 100 unidades.</span><span class="sxs-lookup"><span data-stu-id="26338-109">The world transformation of the **Graphics** object is a translation 200 units to the right, and the world transformation of the container is a translation 100 units down.</span></span>


```
myGraphics.TranslateTransform(200.0f, 0.0f);

myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.TranslateTransform(0.0f, 100.0f);
   myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
myGraphics.EndContainer(myGraphicsContainer);

myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50);
```



<span data-ttu-id="26338-110">Tenga en cuenta que en el ejemplo anterior, la instrucción `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` realizada entre las llamadas a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) genera un rectángulo diferente al de la misma instrucción realizada después de la llamada a **Graphics:: EndContainer**.</span><span class="sxs-lookup"><span data-stu-id="26338-110">Note that in the previous example, the statement `myGraphics.DrawRectangle(&myPen, 0, 0, 50, 50)` made in between the calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) produces a different rectangle than the same statement made after the call to **Graphics::EndContainer**.</span></span> <span data-ttu-id="26338-111">Solo la traducción horizontal se aplica a la llamada **DrawRectangle** realizada fuera del contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-111">Only the horizontal translation applies to the **DrawRectangle** call made outside of the container.</span></span> <span data-ttu-id="26338-112">Ambas transformaciones (la traslación horizontal de 200 unidades y la conversión vertical de las unidades 100) se aplican a la llamada de [**gráficos::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) realizada dentro del contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-112">Both transformations — the horizontal translation of 200 units and the vertical translation of 100 units — apply to the [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call made inside the container.</span></span> <span data-ttu-id="26338-113">En la ilustración siguiente se muestran los dos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="26338-113">The following illustration shows the two rectangles.</span></span>

![captura de pantalla de una ventana con dos rectángulos dibujados con un lápiz azul, uno situado encima del otro](images/aboutgdip05-art17.png)

<span data-ttu-id="26338-115">Los contenedores se pueden anidar dentro de contenedores.</span><span class="sxs-lookup"><span data-stu-id="26338-115">Containers can be nested within containers.</span></span> <span data-ttu-id="26338-116">En el ejemplo siguiente se crea un contenedor dentro de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y otro contenedor en el primer contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-116">The following example creates a container within a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and another container within the first container.</span></span> <span data-ttu-id="26338-117">La transformación universal del objeto **Graphics** es una traducción de 100 unidades en la dirección x y 80 unidades en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="26338-117">The world transformation of the **Graphics** object is a translation 100 units in the x direction and 80 units in the y direction.</span></span> <span data-ttu-id="26338-118">La transformación universal del primer contenedor es una rotación de 30 grados.</span><span class="sxs-lookup"><span data-stu-id="26338-118">The world transformation of the first container is a 30-degree rotation.</span></span> <span data-ttu-id="26338-119">La transformación universal del segundo contenedor es un escalado mediante un factor de 2 en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="26338-119">The world transformation of the second container is a scaling by a factor of 2 in the x direction.</span></span> <span data-ttu-id="26338-120">Se realiza una llamada al método [**Graphics::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) en el segundo contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-120">A call to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) method is made inside the second container.</span></span>


```
myGraphics.TranslateTransform(100.0f, 80.0f, MatrixOrderAppend);

container1 = myGraphics.BeginContainer();
   myGraphics.RotateTransform(30.0f, MatrixOrderAppend);

   container2 = myGraphics.BeginContainer();
      myGraphics.ScaleTransform(2.0f, 1.0f);
      myGraphics.DrawEllipse(&myPen, -30, -20, 60, 40);
   myGraphics.EndContainer(container2);

myGraphics.EndContainer(container1);
```



<span data-ttu-id="26338-121">En la ilustración siguiente se muestra la elipse.</span><span class="sxs-lookup"><span data-stu-id="26338-121">The following illustration shows the ellipse.</span></span>

![captura de pantalla de una ventana que contiene una elipse azul girada con su centro etiquetada como (100, 80)](images/aboutgdip05-art18.png)

<span data-ttu-id="26338-123">Tenga en cuenta que las tres transformaciones se aplican a la llamada de [**gráficos::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) realizada en el segundo contenedor (interior).</span><span class="sxs-lookup"><span data-stu-id="26338-123">Note that all three transformations apply to the [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) call made in the second (innermost) container.</span></span> <span data-ttu-id="26338-124">Tenga en cuenta también el orden de las transformaciones: primera escala, girar y después trasladar.</span><span class="sxs-lookup"><span data-stu-id="26338-124">Also note the order of the transformations: first scale, then rotate, then translate.</span></span> <span data-ttu-id="26338-125">La transformación más interna se aplica primero y la transformación más externa se aplica en último lugar.</span><span class="sxs-lookup"><span data-stu-id="26338-125">The innermost transformation is applied first, and the outermost transformation is applied last.</span></span>

<span data-ttu-id="26338-126">Cualquier propiedad de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se puede establecer dentro de un contenedor (entre las llamadas a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span><span class="sxs-lookup"><span data-stu-id="26338-126">Any property of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be set inside a container (in between calls to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) and [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)).</span></span> <span data-ttu-id="26338-127">Por ejemplo, se puede establecer una región de recorte dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-127">For example, a clipping region can be set inside a container.</span></span> <span data-ttu-id="26338-128">Cualquier dibujo realizado dentro del contenedor se restringe a la región de recorte de ese contenedor y también se restringe a las regiones de recorte de cualquier contenedor externo y la región de recorte del propio objeto de **gráficos** .</span><span class="sxs-lookup"><span data-stu-id="26338-128">Any drawing done inside the container will be restricted to the clipping region of that container and will also be restricted to the clipping regions of any outer containers and the clipping region of the **Graphics** object itself.</span></span>

<span data-ttu-id="26338-129">Las propiedades descritas hasta ahora, la transformación universal y la región de recorte, se combinan mediante contenedores anidados.</span><span class="sxs-lookup"><span data-stu-id="26338-129">The properties discussed so far — the world transformation and the clipping region — are combined by nested containers.</span></span> <span data-ttu-id="26338-130">Otras propiedades se reemplazan temporalmente por un contenedor anidado.</span><span class="sxs-lookup"><span data-stu-id="26338-130">Other properties are temporarily replaced by a nested container.</span></span> <span data-ttu-id="26338-131">Por ejemplo, si establece el modo de suavizado en SmoothingModeAntiAlias dentro de un contenedor, cualquier método de dibujo llamado dentro de ese contenedor usará el modo de suavizado antialias, pero los métodos de dibujo llamados después de [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) usarán el modo de suavizado que estaba antes de la llamada a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span><span class="sxs-lookup"><span data-stu-id="26338-131">For example, if you set the smoothing mode to SmoothingModeAntiAlias within a container, any drawing methods called inside that container will use the antialias smoothing mode, but drawing methods called after [**Graphics::EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) will use the smoothing mode that was in place before the call to [**Graphics::BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).</span></span>

<span data-ttu-id="26338-132">Para obtener otro ejemplo de cómo combinar las transformaciones del mundo de un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor, supongamos que desea dibujar un ojo y colocarlo en varias ubicaciones en una secuencia de caras.</span><span class="sxs-lookup"><span data-stu-id="26338-132">For another example of combining the world transformations of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and a container, suppose you want to draw an eye and place it at various locations on a sequence of faces.</span></span> <span data-ttu-id="26338-133">En el ejemplo siguiente se dibuja un ojo centrado en el origen del sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="26338-133">The following example draws an eye centered at the origin of the coordinate system.</span></span>


```
void DrawEye(Graphics* pGraphics)
{
   GraphicsContainer eyeContainer;
   
   eyeContainer = pGraphics->BeginContainer();

      Pen myBlackPen(Color(255, 0, 0, 0));
      SolidBrush myGreenBrush(Color(255, 0, 128, 0));
      SolidBrush myBlackBrush(Color(255, 0, 0, 0));

      GraphicsPath myTopPath;
      myTopPath.AddEllipse(-30, -50, 60, 60);

      GraphicsPath myBottomPath;
      myBottomPath.AddEllipse(-30, -10, 60, 60);

      Region myTopRegion(&myTopPath);
      Region myBottomRegion(&myBottomPath);

      // Draw the outline of the eye.
      // The outline of the eye consists of two ellipses.
      // The top ellipse is clipped by the bottom ellipse, and
      // the bottom ellipse is clipped by the top ellipse.
      pGraphics->SetClip(&myTopRegion);
      pGraphics->DrawPath(&myBlackPen, &myBottomPath);
      pGraphics->SetClip(&myBottomRegion);
      pGraphics->DrawPath(&myBlackPen, &myTopPath);

      // Fill the iris.
      // The iris is clipped by the bottom ellipse.
      pGraphics->FillEllipse(&myGreenBrush, -10, -15, 20, 22);

      // Fill the pupil.
      pGraphics->FillEllipse(&myBlackBrush, -3, -7, 6, 9);

   pGraphics->EndContainer(eyeContainer);
}
```



<span data-ttu-id="26338-134">En la ilustración siguiente se muestra el ojo y los ejes de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="26338-134">The following illustration shows the eye and the coordinate axes.</span></span>

![Ilustración en la que se muestra un ojo compuesto de tres puntos suspensivos: uno para el contorno, iris y Pupil](images/aboutgdip05-art19.png)

<span data-ttu-id="26338-136">La función DrawEye, definida en el ejemplo anterior, recibe la dirección de un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y crea inmediatamente un contenedor en ese objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="26338-136">The DrawEye function, defined in the previous example receives the address of a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and immediately creates a container within that **Graphics** object.</span></span> <span data-ttu-id="26338-137">Este contenedor aísla cualquier código que llame a la función DrawEye desde la configuración de propiedades realizada durante la ejecución de la función DrawEye.</span><span class="sxs-lookup"><span data-stu-id="26338-137">This container insulates any code that calls the DrawEye function from property settings made during the execution of the DrawEye function.</span></span> <span data-ttu-id="26338-138">Por ejemplo, el código de la función DrawEye establece la región de recorte del objeto **Graphics** , pero cuando DrawEye devuelve el control a la rutina que realiza la llamada, la región de recorte será como estaba antes de la llamada a DrawEye.</span><span class="sxs-lookup"><span data-stu-id="26338-138">For example, code in the DrawEye function sets the clipping region of the **Graphics** object, but when DrawEye returns control to the calling routine, the clipping region will be as it was before the call to DrawEye.</span></span>

<span data-ttu-id="26338-139">En el ejemplo siguiente se dibujan tres elipses (caras), cada una de ellas con un ojo.</span><span class="sxs-lookup"><span data-stu-id="26338-139">The following example draws three ellipses (faces), each with an eye inside.</span></span>


```
// Draw an ellipse with center at (100, 100).
myGraphics.TranslateTransform(100.0f, 100.0f);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Draw the eye at the center of the ellipse.
DrawEye(&myGraphics);

// Draw an ellipse with center at 200, 100.
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Rotate the eye 40 degrees, and draw it 30 units above
// the center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.RotateTransform(-40.0f);
   myGraphics.TranslateTransform(0.0f, -30.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);

// Draw a ellipse with center at (300.0f, 100.0f).
myGraphics.TranslateTransform(100.0f, 0.0f, MatrixOrderAppend);
myGraphics.DrawEllipse(&myBlackPen, -40, -60, 80, 120);

// Stretch and rotate the eye, and draw it at the 
// center of the ellipse.
myGraphicsContainer = myGraphics.BeginContainer();
   myGraphics.ScaleTransform(2.0f, 1.5f);
   myGraphics.RotateTransform(45.0f, MatrixOrderAppend);
   DrawEye(&myGraphics);
myGraphics.EndContainer(myGraphicsContainer);
```



<span data-ttu-id="26338-140">En la ilustración siguiente se muestran los tres puntos suspensivos.</span><span class="sxs-lookup"><span data-stu-id="26338-140">The following illustration shows the three ellipses.</span></span>

![captura de pantalla de una ventana con tres elipses, cada una de las cuales contiene un ojo con un tamaño y una rotación diferentes](images/aboutgdip05-art20.png)

<span data-ttu-id="26338-142">En el ejemplo anterior, todas las elipses se dibujan con la llamada `DrawEllipse(&myBlackPen, -40, -60, 80, 120)` , que dibuja una elipse centrada en el origen del sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="26338-142">In the previous example, all ellipses are drawn with the call `DrawEllipse(&myBlackPen, -40, -60, 80, 120)`, which draws an ellipse centered at the origin of the coordinate system.</span></span> <span data-ttu-id="26338-143">Las elipses se desplazan de la esquina superior izquierda del área cliente estableciendo la transformación universal del objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="26338-143">The ellipses are moved away from the upper-left corner of the client area by setting the world transformation of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="26338-144">La instrucción hace que la primera elipse se Centre en (100, 100).</span><span class="sxs-lookup"><span data-stu-id="26338-144">The statement causes the first ellipse to be centered at (100, 100).</span></span> <span data-ttu-id="26338-145">La instrucción hace que el centro de la segunda elipse sea 100 unidades a la derecha del centro de la primera elipse.</span><span class="sxs-lookup"><span data-stu-id="26338-145">The statement causes the center of the second ellipse to be 100 units to the right of the center of the first ellipse.</span></span> <span data-ttu-id="26338-146">Del mismo modo, el centro de la tercera elipse es 100 unidades a la derecha del centro de la segunda elipse.</span><span class="sxs-lookup"><span data-stu-id="26338-146">Likewise, the center of the third ellipse is 100 units to the right of the center of the second ellipse.</span></span>

<span data-ttu-id="26338-147">Los contenedores del ejemplo anterior se usan para transformar el ojo en relación con el centro de una elipse determinada.</span><span class="sxs-lookup"><span data-stu-id="26338-147">The containers in the previous example are used to transform the eye relative to the center of a given ellipse.</span></span> <span data-ttu-id="26338-148">El primer ojo se dibuja en el centro de la elipse sin transformación, por lo que la llamada a DrawEye no está dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-148">The first eye is drawn at the center of the ellipse with no transformation, so the DrawEye call is not inside a container.</span></span> <span data-ttu-id="26338-149">El segundo ojo gira 40 grados y se dibujan 30 unidades por encima del centro de la elipse, por lo que se llama a la función DrawEye y a los métodos que establecen la transformación dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-149">The second eye is rotated 40 degrees and drawn 30 units above the center of the ellipse, so the DrawEye function and the methods that set the transformation are called inside a container.</span></span> <span data-ttu-id="26338-150">El tercer ojo se estira y gira y se dibuja en el centro de la elipse.</span><span class="sxs-lookup"><span data-stu-id="26338-150">The third eye is stretched and rotated and drawn at the center of the ellipse.</span></span> <span data-ttu-id="26338-151">Al igual que en el segundo ojo, se llama a la función DrawEye y a los métodos que establecen la transformación dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="26338-151">As with the second eye, the DrawEye function and the methods that set the transformation are called inside a container.</span></span>

 

 
