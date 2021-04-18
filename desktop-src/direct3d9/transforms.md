---
description: La parte de Direct3D que envía la geometría a través de la canalización de geometría de función fija es el motor de transformación.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformaciones (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423148"
---
# <a name="transforms-direct3d-9"></a><span data-ttu-id="7d811-103">Transformaciones (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7d811-103">Transforms (Direct3D 9)</span></span>

<span data-ttu-id="7d811-104">La parte de Direct3D que envía la geometría a través de la canalización de geometría de función fija es el motor de transformación.</span><span class="sxs-lookup"><span data-stu-id="7d811-104">The part of Direct3D that pushes geometry through the fixed function geometry pipeline is the transform engine.</span></span> <span data-ttu-id="7d811-105">Busca el modelo y el visor en el mundo, proyecta los vértices para su presentación en la pantalla y recorta los vértices en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="7d811-105">It locates the model and viewer in the world, projects vertices for display on the screen, and clips vertices to the viewport.</span></span> <span data-ttu-id="7d811-106">El motor de transformación también realiza cálculos de iluminación para determinar los componentes difusos y especulares en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="7d811-106">The transform engine also performs lighting computations to determine diffuse and specular components at each vertex.</span></span>

<span data-ttu-id="7d811-107">La canalización de geometría toma los vértices como entrada.</span><span class="sxs-lookup"><span data-stu-id="7d811-107">The geometry pipeline takes vertices as input.</span></span> <span data-ttu-id="7d811-108">El motor de transformación aplica las transformaciones mundo, vista y proyección a los vértices, recorta el resultado y pasa todo al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="7d811-108">The transform engine applies the world, view, and projection transforms to the vertices, clips the result, and passes everything to the rasterizer.</span></span>

<span data-ttu-id="7d811-109">En el encabezado de la canalización, los vértices de un modelo se declaran en relación con un sistema de coordenadas local.</span><span class="sxs-lookup"><span data-stu-id="7d811-109">At the head of the pipeline, a model's vertices are declared relative to a local coordinate system.</span></span> <span data-ttu-id="7d811-110">Se trata de un origen local y una orientación.</span><span class="sxs-lookup"><span data-stu-id="7d811-110">This is a local origin and an orientation.</span></span> <span data-ttu-id="7d811-111">Esta orientación de las coordenadas se denomina a menudo espacio de modelo y las coordenadas individuales se denominan coordenadas del modelo.</span><span class="sxs-lookup"><span data-stu-id="7d811-111">This orientation of coordinates is often referred to as model space, and individual coordinates are called model coordinates.</span></span>

<span data-ttu-id="7d811-112">La primera fase de la canalización de geometría transforma los vértices de un modelo de su sistema de coordenadas local en un sistema de coordenadas que usan todos los objetos de una escena.</span><span class="sxs-lookup"><span data-stu-id="7d811-112">The first stage of the geometry pipeline transforms a model's vertices from their local coordinate system to a coordinate system that is used by all the objects in a scene.</span></span> <span data-ttu-id="7d811-113">El proceso de reorientar los vértices se denomina transformación universal.</span><span class="sxs-lookup"><span data-stu-id="7d811-113">The process of reorienting the vertices is called the world transform.</span></span> <span data-ttu-id="7d811-114">Esta nueva orientación se conoce comúnmente como espacio universal y cada vértice en el espacio universal se declara mediante coordenadas universales.</span><span class="sxs-lookup"><span data-stu-id="7d811-114">This new orientation is commonly referred to as world space, and each vertex in world space is declared using world coordinates.</span></span>

<span data-ttu-id="7d811-115">En la fase siguiente, los vértices que describen el mundo 3D están orientados con respecto a una cámara.</span><span class="sxs-lookup"><span data-stu-id="7d811-115">In the next stage, the vertices that describe your 3D world are oriented with respect to a camera.</span></span> <span data-ttu-id="7d811-116">Es decir, la aplicación elige un punto de vista para la escena y las coordenadas del espacio universal se reubican y giran alrededor de la vista de la cámara, lo que convierte el espacio universal en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="7d811-116">That is, your application chooses a point-of-view for the scene, and world space coordinates are relocated and rotated around the camera's view, turning world space into camera space.</span></span> <span data-ttu-id="7d811-117">Esta es la transformación de la vista.</span><span class="sxs-lookup"><span data-stu-id="7d811-117">This is the view transform.</span></span>

<span data-ttu-id="7d811-118">La siguiente fase es la transformación de proyección.</span><span class="sxs-lookup"><span data-stu-id="7d811-118">The next stage is the projection transform.</span></span> <span data-ttu-id="7d811-119">En esta parte de la canalización, los objetos normalmente se escalan con relación a su distancia desde el visor para dar la sensación de profundidad a una escena. los objetos de cierre se realizan para que aparezcan más grandes que los objetos lejanos, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7d811-119">In this part of the pipeline, objects are usually scaled with relation to their distance from the viewer in order to give the illusion of depth to a scene; close objects are made to appear larger than distant objects, and so on.</span></span> <span data-ttu-id="7d811-120">Para simplificar, en esta documentación se hace referencia al espacio en el que los vértices existen después de la transformación de proyección como espacio de proyección.</span><span class="sxs-lookup"><span data-stu-id="7d811-120">For simplicity, this documentation refers to the space in which vertices exist after the projection transform as projection space.</span></span> <span data-ttu-id="7d811-121">Algunos libros de gráficos pueden hacer referencia al espacio de proyección como espacio homogéneo posterior a la perspectiva.</span><span class="sxs-lookup"><span data-stu-id="7d811-121">Some graphics books might refer to projection space as post-perspective homogeneous space.</span></span> <span data-ttu-id="7d811-122">No todas las transformaciones de proyección escalan el tamaño de los objetos en una escena.</span><span class="sxs-lookup"><span data-stu-id="7d811-122">Not all projection transforms scale the size of objects in a scene.</span></span> <span data-ttu-id="7d811-123">Una proyección como esta se denomina a veces una proyección afín o ortogonal.</span><span class="sxs-lookup"><span data-stu-id="7d811-123">A projection such as this is sometimes called an affine or orthogonal projection.</span></span>

<span data-ttu-id="7d811-124">En la parte final de la canalización, se quitan los vértices que no serán visibles en la pantalla, de modo que el rasterizador no dedique tiempo a calcular los colores y el sombreado para algo que nunca se verá.</span><span class="sxs-lookup"><span data-stu-id="7d811-124">In the final part of the pipeline, any vertices that will not be visible on the screen are removed, so that the rasterizer doesn't take the time to calculate the colors and shading for something that will never be seen.</span></span> <span data-ttu-id="7d811-125">Este proceso se denomina recorte.</span><span class="sxs-lookup"><span data-stu-id="7d811-125">This process is called clipping.</span></span> <span data-ttu-id="7d811-126">Después del recorte, los vértices restantes se escalan según los parámetros de la ventanilla y se convierten en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="7d811-126">After clipping, the remaining vertices are scaled according to the viewport parameters and converted into screen coordinates.</span></span> <span data-ttu-id="7d811-127">Los vértices resultantes, que se muestran en la pantalla cuando se rasteriza la escena, existen en el espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="7d811-127">The resulting vertices, seen on the screen when the scene is rasterized, exist in screen space.</span></span>

<span data-ttu-id="7d811-128">Las transformaciones se usan para convertir la geometría de objeto de un espacio de coordenadas a otro.</span><span class="sxs-lookup"><span data-stu-id="7d811-128">Transforms are used to convert object geometry from one coordinate space to another.</span></span> <span data-ttu-id="7d811-129">Direct3D usa matrices para realizar transformaciones 3D.</span><span class="sxs-lookup"><span data-stu-id="7d811-129">Direct3D uses matrices to perform 3D transforms.</span></span> <span data-ttu-id="7d811-130">En esta sección se explica cómo las matrices crean transformaciones 3D, se describen algunos usos comunes de las transformaciones y se detalla cómo se pueden combinar matrices para generar una sola matriz que abarque varias transformaciones.</span><span class="sxs-lookup"><span data-stu-id="7d811-130">This section explains how matrices create 3D transforms, describes some common uses for transforms, and details how you can combine matrices to produce a single matrix that encompasses multiple transforms.</span></span>

-   <span data-ttu-id="7d811-131">[Universal Transform (Direct3D 9)](world-transform.md) : conversión del espacio de modelo al espacio universal</span><span class="sxs-lookup"><span data-stu-id="7d811-131">[World Transform (Direct3D 9)](world-transform.md) - convert from model space to world space</span></span>
-   <span data-ttu-id="7d811-132">[Transformación de vista (Direct3D 9)](view-transform.md) : conversión del espacio universal al espacio de vista</span><span class="sxs-lookup"><span data-stu-id="7d811-132">[View Transform (Direct3D 9)](view-transform.md) - convert from world space to view space</span></span>
-   <span data-ttu-id="7d811-133">[Transformación de proyección (Direct3D 9)](projection-transform.md) : conversión del espacio de vista al espacio de proyección</span><span class="sxs-lookup"><span data-stu-id="7d811-133">[Projection Transform (Direct3D 9)](projection-transform.md) - convert from view space to projection space</span></span>

## <a name="matrix-transforms"></a><span data-ttu-id="7d811-134">Transformaciones de matriz</span><span class="sxs-lookup"><span data-stu-id="7d811-134">Matrix Transforms</span></span>

<span data-ttu-id="7d811-135">En las aplicaciones que funcionan con gráficos 3D, puede usar transformaciones geométricas para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7d811-135">In applications that work with 3D graphics, you can use geometrical transforms to do the following:</span></span>

-   <span data-ttu-id="7d811-136">Expresar la ubicación de un objeto con respecto a otro objeto.</span><span class="sxs-lookup"><span data-stu-id="7d811-136">Express the location of an object relative to another object.</span></span>
-   <span data-ttu-id="7d811-137">Rotar y ajustar el tamaño de los objetos.</span><span class="sxs-lookup"><span data-stu-id="7d811-137">Rotate and size objects.</span></span>
-   <span data-ttu-id="7d811-138">Cambiar las posiciones, las direcciones y las perspectivas de visualización.</span><span class="sxs-lookup"><span data-stu-id="7d811-138">Change viewing positions, directions, and perspectives.</span></span>

<span data-ttu-id="7d811-139">Puede transformar cualquier punto (x, y, z) en otro punto (x ', y ', z ') mediante una matriz 4x4, tal como se muestra en la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="7d811-139">You can transform any point (x,y,z) into another point (x', y', z') by using a 4x4 matrix, as shown in the following equation.</span></span>

![ecuación de transformar cualquier punto en otro punto](images/matmult.png)

<span data-ttu-id="7d811-141">Realice las ecuaciones siguientes en (x, y, z) y en la matriz para generar el punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="7d811-141">Perform the following equations on (x, y, z) and the matrix to produce the point (x', y', z').</span></span>

![ecuaciones para el nuevo punto](images/matexpnd.png)

<span data-ttu-id="7d811-143">Las transformaciones más comunes son traducción, rotación y escalado.</span><span class="sxs-lookup"><span data-stu-id="7d811-143">The most common transforms are translation, rotation, and scaling.</span></span> <span data-ttu-id="7d811-144">Puede combinar las matrices que producen estos efectos en una sola matriz para calcular varias transformaciones a la vez.</span><span class="sxs-lookup"><span data-stu-id="7d811-144">You can combine the matrices that produce these effects into a single matrix to calculate several transforms at once.</span></span> <span data-ttu-id="7d811-145">Por ejemplo, puede crear una matriz única para traducir y girar una serie de puntos.</span><span class="sxs-lookup"><span data-stu-id="7d811-145">For example, you can build a single matrix to translate and rotate a series of points.</span></span>

<span data-ttu-id="7d811-146">Las matrices se escriben en orden de fila y columna.</span><span class="sxs-lookup"><span data-stu-id="7d811-146">Matrices are written in row-column order.</span></span> <span data-ttu-id="7d811-147">Una matriz que escala uniformemente los vértices a lo largo de cada eje, conocido como escala uniforme, se representa mediante la siguiente matriz mediante notación matemática.</span><span class="sxs-lookup"><span data-stu-id="7d811-147">A matrix that evenly scales vertices along each axis, known as uniform scaling, is represented by the following matrix using mathematical notation.</span></span>

![ecuación de una matriz para el escalado uniforme](images/matrix.png)

<span data-ttu-id="7d811-149">En C++, Direct3D declara las matrices como una matriz bidimensional mediante la estructura [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="7d811-149">In C++, Direct3D declares matrices as a two-dimensional array, using the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="7d811-150">En el ejemplo siguiente se muestra cómo inicializar una estructura **D3DMATRIX** para que actúe como una matriz de escalado uniforme.</span><span class="sxs-lookup"><span data-stu-id="7d811-150">The following example shows how to initialize a **D3DMATRIX** structure to act as a uniform scaling matrix.</span></span>


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a><span data-ttu-id="7d811-151">Translate</span><span class="sxs-lookup"><span data-stu-id="7d811-151">Translate</span></span>

<span data-ttu-id="7d811-152">La ecuación siguiente traduce el punto (x, y, z) a un nuevo punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="7d811-152">The following equation translates the point (x, y, z) to a new point (x', y', z').</span></span>

![ecuación de una matriz de traslación para un nuevo punto](images/transl8.png)

<span data-ttu-id="7d811-154">Puede crear manualmente una matriz de traducción en C++.</span><span class="sxs-lookup"><span data-stu-id="7d811-154">You can manually create a translation matrix in C++.</span></span> <span data-ttu-id="7d811-155">En el ejemplo siguiente se muestra el código fuente de una función que crea una matriz para traducir los vértices.</span><span class="sxs-lookup"><span data-stu-id="7d811-155">The following example shows the source code for a function that creates a matrix to translate vertices.</span></span>


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



<span data-ttu-id="7d811-156">Para mayor comodidad, la biblioteca de utilidades de D3DX proporciona la función [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .</span><span class="sxs-lookup"><span data-stu-id="7d811-156">For convenience, the D3DX utility library supplies the [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) function.</span></span>

## <a name="scale"></a><span data-ttu-id="7d811-157">Escala</span><span class="sxs-lookup"><span data-stu-id="7d811-157">Scale</span></span>

<span data-ttu-id="7d811-158">La ecuación siguiente escala el punto (x, y, z) mediante valores arbitrarios en las direcciones x-, y-y z-a un punto nuevo (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="7d811-158">The following equation scales the point (x, y, z) by arbitrary values in the x-, y-, and z-directions to a new point (x', y', z').</span></span>

![ecuación de una matriz de escala para un nuevo punto](images/matscale.png)

## <a name="rotate"></a><span data-ttu-id="7d811-160">Girar</span><span class="sxs-lookup"><span data-stu-id="7d811-160">Rotate</span></span>

<span data-ttu-id="7d811-161">Las transformaciones que se describen aquí son para los sistemas de coordenadas de la mano izquierda y, por tanto, pueden ser diferentes de las matrices de transformación que se han encontrado en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="7d811-161">The transforms described here are for left-handed coordinate systems, and so may be different from transform matrices that you have seen elsewhere.</span></span>

<span data-ttu-id="7d811-162">La siguiente ecuación gira el punto (x, y, z) alrededor del eje x, lo que produce un nuevo punto (x ', y ', z ').</span><span class="sxs-lookup"><span data-stu-id="7d811-162">The following equation rotates the point (x, y, z) around the x-axis, producing a new point (x', y', z').</span></span>

![ecuación de una matriz de rotación x para un nuevo punto](images/matxrot.png)

<span data-ttu-id="7d811-164">La siguiente ecuación gira el punto alrededor del eje y.</span><span class="sxs-lookup"><span data-stu-id="7d811-164">The following equation rotates the point around the y-axis.</span></span>

![ecuación de una matriz de rotación y para un nuevo punto](images/matyrot.png)

<span data-ttu-id="7d811-166">La siguiente ecuación gira el punto alrededor del eje z.</span><span class="sxs-lookup"><span data-stu-id="7d811-166">The following equation rotates the point around the z-axis.</span></span>

![ecuación de una matriz de rotación z para un nuevo punto](images/matzrot.png)

<span data-ttu-id="7d811-168">En estas matrices de ejemplo, la letra griega Theta representa el ángulo de rotación, en radianes.</span><span class="sxs-lookup"><span data-stu-id="7d811-168">In these example matrices, the Greek letter theta stands for the angle of rotation, in radians.</span></span> <span data-ttu-id="7d811-169">Los ángulos se miden en el sentido de las agujas del reloj al mirar el eje de giro hacia el origen.</span><span class="sxs-lookup"><span data-stu-id="7d811-169">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

<span data-ttu-id="7d811-170">En una aplicación de C++, use las funciones [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)y [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) que proporciona la biblioteca de utilidades de D3DX para crear matrices de rotación.</span><span class="sxs-lookup"><span data-stu-id="7d811-170">In a C++ application, use the [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md), and [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) functions supplied by the D3DX utility library to create rotation matrices.</span></span> <span data-ttu-id="7d811-171">A continuación se encuentra el código de la función **D3DXMatrixRotationX** .</span><span class="sxs-lookup"><span data-stu-id="7d811-171">The following is the code for the **D3DXMatrixRotationX** function.</span></span>


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a><span data-ttu-id="7d811-172">Concatenación de matrices</span><span class="sxs-lookup"><span data-stu-id="7d811-172">Concatenating Matrices</span></span>

<span data-ttu-id="7d811-173">Una ventaja de usar matrices es que se pueden combinar los efectos de dos o más matrices multiplicándolos.</span><span class="sxs-lookup"><span data-stu-id="7d811-173">One advantage of using matrices is that you can combine the effects of two or more matrices by multiplying them.</span></span> <span data-ttu-id="7d811-174">Esto significa que, para girar un modelo y, a continuación, convertirlo en una ubicación, no es necesario aplicar dos matrices.</span><span class="sxs-lookup"><span data-stu-id="7d811-174">This means that, to rotate a model and then translate it to some location, you don't need to apply two matrices.</span></span> <span data-ttu-id="7d811-175">En su lugar, se multiplican las matrices de traslación y rotación para producir una matriz compuesta que contiene todos sus efectos.</span><span class="sxs-lookup"><span data-stu-id="7d811-175">Instead, you multiply the rotation and translation matrices to produce a composite matrix that contains all their effects.</span></span> <span data-ttu-id="7d811-176">Este proceso, denominado concatenación de matriz, se puede escribir con la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="7d811-176">This process, called matrix concatenation, can be written with the following equation.</span></span>

![ecuación de concatenación de matriz](images/matrxcat.png)

<span data-ttu-id="7d811-178">En esta ecuación, C es la matriz compuesta que se está creando y M ₁ a MN son las matrices individuales.</span><span class="sxs-lookup"><span data-stu-id="7d811-178">In this equation, C is the composite matrix being created, and M₁ through Mₙ are the individual matrices.</span></span> <span data-ttu-id="7d811-179">En la mayoría de los casos, solo se concatenan dos o tres matrices, pero no hay ningún límite.</span><span class="sxs-lookup"><span data-stu-id="7d811-179">In most cases, only two or three matrices are concatenated, but there is no limit.</span></span>

<span data-ttu-id="7d811-180">Use la función [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) para realizar la multiplicación de matrices.</span><span class="sxs-lookup"><span data-stu-id="7d811-180">Use the [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) function to perform matrix multiplication.</span></span>

<span data-ttu-id="7d811-181">El orden en el que se realiza la multiplicación de matrices es fundamental.</span><span class="sxs-lookup"><span data-stu-id="7d811-181">The order in which the matrix multiplication is performed is crucial.</span></span> <span data-ttu-id="7d811-182">La fórmula anterior refleja la regla de izquierda a derecha de la concatenación de matrices.</span><span class="sxs-lookup"><span data-stu-id="7d811-182">The preceding formula reflects the left-to-right rule of matrix concatenation.</span></span> <span data-ttu-id="7d811-183">Es decir, los efectos visibles de las matrices que se usan para crear una matriz compuesta se producen en orden de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="7d811-183">That is, the visible effects of the matrices that you use to create a composite matrix occur in left-to-right order.</span></span> <span data-ttu-id="7d811-184">En el ejemplo siguiente se muestra una matriz universal típica.</span><span class="sxs-lookup"><span data-stu-id="7d811-184">A typical world matrix is shown in the following example.</span></span> <span data-ttu-id="7d811-185">Imagine que va a crear la matriz mundial para un típica volando Saucer.</span><span class="sxs-lookup"><span data-stu-id="7d811-185">Imagine that you are creating the world matrix for a stereotypical flying saucer.</span></span> <span data-ttu-id="7d811-186">Probablemente quiera girar el Saucer volando en torno a su centro, el eje y del espacio del modelo, y convertirlo en otra ubicación de la escena.</span><span class="sxs-lookup"><span data-stu-id="7d811-186">You would probably want to spin the flying saucer around its center - the y-axis of model space - and translate it to some other location in your scene.</span></span> <span data-ttu-id="7d811-187">Para lograr este efecto, primero se crea una matriz de rotación y, a continuación, se multiplica por una matriz de traslación, tal como se muestra en la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="7d811-187">To accomplish this effect, you first create a rotation matrix, and then multiply it by a translation matrix, as shown in the following equation.</span></span>

![ecuación de giro basada en una matriz de rotación y una matriz de traslación](images/wrldexpl.png)

<span data-ttu-id="7d811-189">En esta fórmula, R<sub>y</sub> es una matriz de rotación sobre el eje y, y T<sub>w</sub> es una traducción a alguna posición en coordenadas universales.</span><span class="sxs-lookup"><span data-stu-id="7d811-189">In this formula, R<sub>y</sub> is a matrix for rotation about the y-axis, and T<sub>w</sub> is a translation to some position in world coordinates.</span></span>

<span data-ttu-id="7d811-190">El orden en que se multiplican las matrices es importante porque, a diferencia de la multiplicación de dos valores escalares, la multiplicación de matrices no es conmutativa.</span><span class="sxs-lookup"><span data-stu-id="7d811-190">The order in which you multiply the matrices is important because, unlike multiplying two scalar values, matrix multiplication is not commutative.</span></span> <span data-ttu-id="7d811-191">La multiplicación de las matrices en el orden opuesto tiene el efecto visual de traducir el Saucer volando a su posición de espacio mundial y, a continuación, girarlo alrededor del origen mundial.</span><span class="sxs-lookup"><span data-stu-id="7d811-191">Multiplying the matrices in the opposite order has the visual effect of translating the flying saucer to its world space position, and then rotating it around the world origin.</span></span>

<span data-ttu-id="7d811-192">Independientemente del tipo de matriz que cree, recuerde la regla de izquierda a derecha para asegurarse de que se obtienen los efectos esperados.</span><span class="sxs-lookup"><span data-stu-id="7d811-192">No matter what type of matrix you are creating, remember the left-to-right rule to ensure that you achieve the expected effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d811-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d811-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d811-194">Introducción</span><span class="sxs-lookup"><span data-stu-id="7d811-194">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



