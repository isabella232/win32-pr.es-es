---
title: Aplicación de transformaciones en Direct2D
description: Aplicación de transformaciones en Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791655"
---
# <a name="applying-transforms-in-direct2d"></a><span data-ttu-id="81adf-103">Aplicación de transformaciones en Direct2D</span><span class="sxs-lookup"><span data-stu-id="81adf-103">Applying Transforms in Direct2D</span></span>

<span data-ttu-id="81adf-104">En el [dibujo con Direct2D](drawing-with-direct2d.md), vimos que el método [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) dibuja una elipse que se alinea con los ejes x e y.</span><span class="sxs-lookup"><span data-stu-id="81adf-104">In [Drawing with Direct2D](drawing-with-direct2d.md), we saw that the [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws an ellipse that is aligned to the x- and y-axes.</span></span> <span data-ttu-id="81adf-105">Pero supongamos que desea dibujar una elipse inclinada en un ángulo.</span><span class="sxs-lookup"><span data-stu-id="81adf-105">But suppose that you want to draw an ellipse tilted at an angle?</span></span>

![imagen que muestra una elipse inclinada.](images/graphics16.png)

<span data-ttu-id="81adf-107">Mediante el uso de transformaciones, puede modificar una forma de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="81adf-107">By using transforms, you can alter a shape in the following ways.</span></span>

-   <span data-ttu-id="81adf-108">Giro alrededor de un punto.</span><span class="sxs-lookup"><span data-stu-id="81adf-108">Rotation around a point.</span></span>
-   <span data-ttu-id="81adf-109">Ajustar la escala.</span><span class="sxs-lookup"><span data-stu-id="81adf-109">Scaling.</span></span>
-   <span data-ttu-id="81adf-110">Translation (desplazamiento en la dirección X o Y).</span><span class="sxs-lookup"><span data-stu-id="81adf-110">Translation (displacement in the X or Y direction).</span></span>
-   <span data-ttu-id="81adf-111">Sesgado (también conocido como *recorte*).</span><span class="sxs-lookup"><span data-stu-id="81adf-111">Skew (also known as *shear*).</span></span>

<span data-ttu-id="81adf-112">Una transformación es una operación matemática que asigna un conjunto de puntos a un nuevo conjunto de puntos.</span><span class="sxs-lookup"><span data-stu-id="81adf-112">A transform is a mathematical operation that maps a set of points to a new set of points.</span></span> <span data-ttu-id="81adf-113">Por ejemplo, en el diagrama siguiente se muestra un triángulo girado alrededor del punto P3.</span><span class="sxs-lookup"><span data-stu-id="81adf-113">For example, the following diagram shows a triangle rotated around the point P3.</span></span> <span data-ttu-id="81adf-114">Una vez aplicado el giro, el punto P1 se asigna a P1 ', el punto P2 se asigna a P2 ' y el punto P3 se asigna a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="81adf-114">After the rotation is applied, the point P1 is mapped to P1', the point P2 is mapped to P2', and the point P3 maps to itself.</span></span>

![diagrama que muestra la rotación alrededor de un punto.](images/graphics17.png)

<span data-ttu-id="81adf-116">Las transformaciones se implementan mediante matrices.</span><span class="sxs-lookup"><span data-stu-id="81adf-116">Transforms are implemented by using matrices.</span></span> <span data-ttu-id="81adf-117">Sin embargo, no es necesario comprender las matemáticas de las matrices para poder utilizarlas.</span><span class="sxs-lookup"><span data-stu-id="81adf-117">However, you do not have to understand the mathematics of matrices in order to use them.</span></span> <span data-ttu-id="81adf-118">Si desea obtener más información sobre las matemáticas, consulte [Apéndice: transformaciones de matriz](appendix--matrix-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="81adf-118">If you want to learn more about the math, see [Appendix: Matrix Transforms](appendix--matrix-transforms.md).</span></span>

<span data-ttu-id="81adf-119">Para aplicar una transformación en Direct2D, llame al método [**ID2D1RenderTarget:: SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="81adf-119">To apply a transform in Direct2D, call the [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) method.</span></span> <span data-ttu-id="81adf-120">Este método toma una estructura [**D2D1 de \_ matriz \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) que define la transformación.</span><span class="sxs-lookup"><span data-stu-id="81adf-120">This method takes a [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure that defines the transformation.</span></span> <span data-ttu-id="81adf-121">Puede inicializar esta estructura llamando a métodos en la clase [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="81adf-121">You can initialize this structure by calling methods on the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="81adf-122">Esta clase contiene métodos estáticos que devuelven una matriz para cada tipo de transformación:</span><span class="sxs-lookup"><span data-stu-id="81adf-122">This class contains static methods that return a matrix for each kind of transform:</span></span>

-   [<span data-ttu-id="81adf-123">**Matrix3x2F:: Rotation**</span><span class="sxs-lookup"><span data-stu-id="81adf-123">**Matrix3x2F::Rotation**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   <span data-ttu-id="81adf-124">[**Matrix3x2F:: scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span><span class="sxs-lookup"><span data-stu-id="81adf-124">[**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))</span></span>
-   <span data-ttu-id="81adf-125">[**Matrix3x2F:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span><span class="sxs-lookup"><span data-stu-id="81adf-125">[**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))</span></span>
-   [<span data-ttu-id="81adf-126">**Matrix3x2F:: Skew**</span><span class="sxs-lookup"><span data-stu-id="81adf-126">**Matrix3x2F::Skew**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

<span data-ttu-id="81adf-127">Por ejemplo, el código siguiente aplica una rotación de 20 grados alrededor del punto (100, 100).</span><span class="sxs-lookup"><span data-stu-id="81adf-127">For example, the following code applies a 20-degree rotation around the point (100, 100).</span></span>


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

<span data-ttu-id="81adf-128">La transformación se aplica a todas las operaciones de dibujo posteriores hasta que vuelva a llamar a [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) .</span><span class="sxs-lookup"><span data-stu-id="81adf-128">The transform is applied to all later drawing operations until you call [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) again.</span></span> <span data-ttu-id="81adf-129">Para quitar la transformación actual, llame a **SetTransform** con la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="81adf-129">To remove the current transform, call **SetTransform** with the identity matrix.</span></span> <span data-ttu-id="81adf-130">Para crear la matriz de identidad, llame a la función [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) .</span><span class="sxs-lookup"><span data-stu-id="81adf-130">To create the identity matrix, call the [**Matrix3x2F::Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) function.</span></span>


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a><span data-ttu-id="81adf-131">Mano del reloj de dibujo</span><span class="sxs-lookup"><span data-stu-id="81adf-131">Drawing Clock Hands</span></span>

<span data-ttu-id="81adf-132">Vamos a colocar las transformaciones para usarlas convirtiendo el programa de círculo en un reloj analógico.</span><span class="sxs-lookup"><span data-stu-id="81adf-132">Let's put transforms to use by converting our Circle program into an analog clock.</span></span> <span data-ttu-id="81adf-133">Podemos hacer esto agregando líneas para las manos.</span><span class="sxs-lookup"><span data-stu-id="81adf-133">We can do this by adding lines for the hands.</span></span>

![captura de pantalla del programa de reloj analógico.](images/graphics18.png)

<span data-ttu-id="81adf-135">En lugar de calcular las coordenadas de las líneas, podemos calcular el ángulo y luego aplicar una transformación de giro.</span><span class="sxs-lookup"><span data-stu-id="81adf-135">Instead of calculating the coordinates for the lines, we can calculate the angle and then apply a rotation transform.</span></span> <span data-ttu-id="81adf-136">En el código siguiente se muestra una función que dibuja una mano del reloj.</span><span class="sxs-lookup"><span data-stu-id="81adf-136">The following code shows a function that draws one clock hand.</span></span> <span data-ttu-id="81adf-137">El parámetro *fAngle* proporciona el ángulo de la mano, en grados.</span><span class="sxs-lookup"><span data-stu-id="81adf-137">The *fAngle* parameter gives the angle of the hand, in degrees.</span></span>

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

<span data-ttu-id="81adf-138">Este código dibuja una línea vertical, empezando desde el centro de la esfera del reloj hasta el punto de *conexión* del punto.</span><span class="sxs-lookup"><span data-stu-id="81adf-138">This code draws a vertical line, starting from the center of the clock face and ending at the point *endPoint*.</span></span> <span data-ttu-id="81adf-139">La línea se gira alrededor del centro de la elipse aplicando una transformación de giro.</span><span class="sxs-lookup"><span data-stu-id="81adf-139">The line is rotated around the center of the ellipse by applying a rotation transform.</span></span> <span data-ttu-id="81adf-140">El punto central de la rotación es el centro de la elipse que forma la esfera del reloj.</span><span class="sxs-lookup"><span data-stu-id="81adf-140">The center point for the rotation is the center of ellipse that forms the clock face.</span></span>

![diagrama que muestra el giro de la mano del reloj.](images/graphics19.png)

<span data-ttu-id="81adf-142">En el código siguiente se muestra cómo se dibuja toda la esfera del reloj.</span><span class="sxs-lookup"><span data-stu-id="81adf-142">The following code shows how the whole clock face is drawn.</span></span>

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

<span data-ttu-id="81adf-143">Puede descargar el proyecto de Visual Studio completo desde el [ejemplo de reloj de Direct2D](direct2d-clock-sample.md).</span><span class="sxs-lookup"><span data-stu-id="81adf-143">You can download the complete Visual Studio project from [Direct2D Clock Sample](direct2d-clock-sample.md).</span></span> <span data-ttu-id="81adf-144">(Solo para diversión, la versión de descarga agrega un Gradiant radial a la esfera del reloj).</span><span class="sxs-lookup"><span data-stu-id="81adf-144">(Just for fun, the download version adds a radial gradiant to the clock face.)</span></span>

## <a name="combining-transforms"></a><span data-ttu-id="81adf-145">Combinar transformaciones</span><span class="sxs-lookup"><span data-stu-id="81adf-145">Combining Transforms</span></span>

<span data-ttu-id="81adf-146">Las cuatro transformaciones básicas se pueden combinar multiplicando dos o más matrices.</span><span class="sxs-lookup"><span data-stu-id="81adf-146">The four basic transforms can be combined by multiplying two or more matrices.</span></span> <span data-ttu-id="81adf-147">Por ejemplo, el código siguiente combina una rotación con una traducción.</span><span class="sxs-lookup"><span data-stu-id="81adf-147">For example, the following code combines a rotation with a translation.</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="81adf-148">La clase [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) proporciona el [**operador \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para la multiplicación de matrices.</span><span class="sxs-lookup"><span data-stu-id="81adf-148">The [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class provides [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for matrix multiplication.</span></span> <span data-ttu-id="81adf-149">Es importante el orden en el que se multiplican las matrices.</span><span class="sxs-lookup"><span data-stu-id="81adf-149">The order in which you multiply the matrices is important.</span></span> <span data-ttu-id="81adf-150">Establecer una transformación (M × N) significa "aplicar M primero, seguido de N".</span><span class="sxs-lookup"><span data-stu-id="81adf-150">Setting a transform (M × N) means "Apply M first, followed by N."</span></span> <span data-ttu-id="81adf-151">Por ejemplo, este es el giro seguido de la traducción:</span><span class="sxs-lookup"><span data-stu-id="81adf-151">For example, here is rotation followed by translation:</span></span>

![diagrama que muestra el giro seguido de la traslación.](images/graphics20.png)

<span data-ttu-id="81adf-153">Este es el código de esta transformación:</span><span class="sxs-lookup"><span data-stu-id="81adf-153">Here is the code for this transform:</span></span>

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

<span data-ttu-id="81adf-154">Ahora Compare la transformación con una transformación en el orden inverso, la traducción seguida de la rotación.</span><span class="sxs-lookup"><span data-stu-id="81adf-154">Now compare that transform with a transform in the reverse order, translation followed by rotation.</span></span>

![diagrama que muestra la traslación seguido de la rotación.](images/graphics21.png)

<span data-ttu-id="81adf-156">La rotación se realiza alrededor del centro del rectángulo original.</span><span class="sxs-lookup"><span data-stu-id="81adf-156">The rotation is performed around the center of the original rectangle.</span></span> <span data-ttu-id="81adf-157">Este es el código de esta transformación.</span><span class="sxs-lookup"><span data-stu-id="81adf-157">Here is the code for this transform.</span></span>

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

<span data-ttu-id="81adf-158">Como puede ver, las matrices son las mismas, pero el orden de las operaciones ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="81adf-158">As you can see, the matrices are the same, but the order of operations has changed.</span></span> <span data-ttu-id="81adf-159">Esto sucede porque la multiplicación de matrices no es conmutativa: M × N ≠ N × M.</span><span class="sxs-lookup"><span data-stu-id="81adf-159">This happens because matrix multiplication is not commutative: M × N ≠ N × M.</span></span>

## <a name="next"></a><span data-ttu-id="81adf-160">Siguientes</span><span class="sxs-lookup"><span data-stu-id="81adf-160">Next</span></span>

[<span data-ttu-id="81adf-161">Apéndice: transformaciones de matriz</span><span class="sxs-lookup"><span data-stu-id="81adf-161">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)