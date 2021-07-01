---
title: Transformaciones (DirectComposition)
description: En este tema se describe la compatibilidad de Microsoft DirectComposition con transformaciones afín bidimensionales (2D) (lineales) y se describen los tipos de transformaciones que admite DirectComposition.
ms.assetid: a0f41cc6-e848-4831-8063-609e17d9b4c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991e1205422864efdec82bbd4067b9c7662aaf29
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118660"
---
# <a name="transforms-directcomposition"></a><span data-ttu-id="265ed-103">Transformaciones (DirectComposition)</span><span class="sxs-lookup"><span data-stu-id="265ed-103">Transforms (DirectComposition)</span></span>

> [!NOTE]
> <span data-ttu-id="265ed-104">Para las aplicaciones Windows 10, se recomienda usar las API Windows.UI.Composition en lugar de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="265ed-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="265ed-105">Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="265ed-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="265ed-106">En este tema se describe la compatibilidad de Microsoft DirectComposition con transformaciones afín bidimensionales (2D) (lineales) y se describen los tipos de transformaciones que admite DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="265ed-106">This topic discusses Microsoft DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span>

<span data-ttu-id="265ed-107">DirectComposition también admite transformaciones de perspectiva 3D, pero como requieren la creación de un mapa de bits intermedio, DirectComposition las considera efectos en lugar de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="265ed-107">DirectComposition also supports 3D perspective transforms, but because they require the creation of an intermediate bitmap, DirectComposition considers them to be effects rather than transforms.</span></span> <span data-ttu-id="265ed-108">Para obtener información sobre los efectos de transformación de perspectiva 3D, vea [Efectos](effects.md).</span><span class="sxs-lookup"><span data-stu-id="265ed-108">For information about 3D perspective transform effects, see [Effects](effects.md).</span></span>

<span data-ttu-id="265ed-109">Este tema incluye las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="265ed-109">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="265ed-110">¿Qué es una transformación 2D de DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="265ed-110">What is a DirectComposition 2D transform?</span></span>](#what-is-a-directcomposition-2d-transform)
-   [<span data-ttu-id="265ed-111">El espacio de coordenadas 2D de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="265ed-111">The DirectComposition 2D coordinate space</span></span>](#the-directcomposition-2d-coordinate-space)
-   [<span data-ttu-id="265ed-112">Compatibilidad con transformaciones 2D afín</span><span class="sxs-lookup"><span data-stu-id="265ed-112">Support for affine 2D transforms</span></span>](#support-for-affine-2d-transforms)
-   [<span data-ttu-id="265ed-113">Transformaciones 2D de matriz</span><span class="sxs-lookup"><span data-stu-id="265ed-113">Matrix 2D transforms</span></span>](#matrix-2d-transforms)
-   [<span data-ttu-id="265ed-114">Transformar grupos</span><span class="sxs-lookup"><span data-stu-id="265ed-114">Transform Groups</span></span>](#transform-groups)
-   [<span data-ttu-id="265ed-115">Animación de transformación</span><span class="sxs-lookup"><span data-stu-id="265ed-115">Transform animation</span></span>](#transform-animation)
-   [<span data-ttu-id="265ed-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="265ed-116">Related topics</span></span>](#related-topics)

## <a name="what-is-a-directcomposition-2d-transform"></a><span data-ttu-id="265ed-117">¿Qué es una transformación 2D de DirectComposition?</span><span class="sxs-lookup"><span data-stu-id="265ed-117">What is a DirectComposition 2D transform?</span></span>

<span data-ttu-id="265ed-118">Una transformación 2D le permite modificar la posición, el tamaño o la naturaleza de un objeto visual en dos dimensiones moviendo el objeto visual a otra ubicación (traducción), lo hace más grande o más pequeño (escalado), lo convierte (rotación) o distorsiona su forma (sesgo).</span><span class="sxs-lookup"><span data-stu-id="265ed-118">A 2D transform enables you to alter the position, size, or nature of a visual in two dimensions by moving the visual to another location (translation), making it larger or smaller (scaling), turning it (rotation), or distorting its shape (skewing).</span></span>

<span data-ttu-id="265ed-119">Una transformación 2D se logra mediante la asignación de los puntos de un objeto visual de una posición a otra dentro del mismo espacio de coordenadas, o de un espacio de coordenadas a otro.</span><span class="sxs-lookup"><span data-stu-id="265ed-119">A 2D transform is achieved by mapping the points of a visual from one position to another within the same coordinate space, or from one coordinate space to another.</span></span> <span data-ttu-id="265ed-120">Esta asignación se describe mediante una tabla de valores denominada matriz de transformación, definida como una colección de tres filas con tres columnas de valores de punto flotante, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="265ed-120">This mapping is described by a table of values called a transformation matrix, defined as a collection of three rows with three columns of floating-point values as shown in the following table.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="265ed-121">M11Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="265ed-121">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="265ed-122">M21Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="265ed-122">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="265ed-123">M31OffsetX: 0,0</span><span class="sxs-lookup"><span data-stu-id="265ed-123">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="265ed-124">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="265ed-124">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="265ed-125">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="265ed-125">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="265ed-126">M32OffsetY: 0,0</span><span class="sxs-lookup"><span data-stu-id="265ed-126">M32OffsetY: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="265ed-127">0,0</span><span class="sxs-lookup"><span data-stu-id="265ed-127">0.0</span></span><br/>
        <span data-ttu-id="265ed-128">0,0</span><span class="sxs-lookup"><span data-stu-id="265ed-128">0.0</span></span><br/>
        <span data-ttu-id="265ed-129">1,0</span><span class="sxs-lookup"><span data-stu-id="265ed-129">1.0</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="265ed-130">La matriz de transformación para transformaciones 2D afínes es una matriz 3 por 2 que omite la tercera columna de la matriz de transformación anterior.</span><span class="sxs-lookup"><span data-stu-id="265ed-130">The transformation matrix for affine 2D transforms is a 3-by-2 matrix that omits the third column from the previous transformation matrix.</span></span> <span data-ttu-id="265ed-131">En la tabla siguiente se muestra el diseño de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="265ed-131">The following table shows the layout of this matrix.</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="265ed-132">M11Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="265ed-132">M11Default: 1.0</span></span><br/>
        <span data-ttu-id="265ed-133">M21Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="265ed-133">M21Default: 0.0</span></span><br/>
        <span data-ttu-id="265ed-134">M31OffsetX: 0,0</span><span class="sxs-lookup"><span data-stu-id="265ed-134">M31OffsetX: 0.0</span></span>
    :::column-end:::
    :::column:::
        <span data-ttu-id="265ed-135">M12Default: 0.0</span><span class="sxs-lookup"><span data-stu-id="265ed-135">M12Default: 0.0</span></span><br/>
        <span data-ttu-id="265ed-136">M22Default: 1.0</span><span class="sxs-lookup"><span data-stu-id="265ed-136">M22Default: 1.0</span></span><br/>
        <span data-ttu-id="265ed-137">M32OffsetY: 0,0</span><span class="sxs-lookup"><span data-stu-id="265ed-137">M32OffsetY: 0.0</span></span>
    :::column-end:::
:::row-end:::

> [!Note]  
> <span data-ttu-id="265ed-138">DirectComposition no realiza ningún procesamiento especial al aplicar transformaciones 2D al contenido estéreo.</span><span class="sxs-lookup"><span data-stu-id="265ed-138">DirectComposition does no special processing when applying 2D transforms to stereo content.</span></span> <span data-ttu-id="265ed-139">Esto significa que el contenido 3D puede aparecer distorsionado cuando se le aplica una transformación 2D.</span><span class="sxs-lookup"><span data-stu-id="265ed-139">This means the 3D content might appear distorted when a 2D transform is applied to it.</span></span>

 

## <a name="the-directcomposition-2d-coordinate-space"></a><span data-ttu-id="265ed-140">El espacio de coordenadas 2D de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="265ed-140">The DirectComposition 2D coordinate space</span></span>

<span data-ttu-id="265ed-141">DirectComposition usa un espacio de coordenadas 2D a la izquierda; Es decir, los valores positivos del eje X aumentan a la derecha y los valores positivos del eje Y aumentan hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="265ed-141">DirectComposition uses a left-handed 2D coordinate space; that is, positive x-axis values increase to the right and positive y-axis values increase downward.</span></span> <span data-ttu-id="265ed-142">Los objetos visuales se sitúan en relación con el origen, que es el punto en el que el eje X y el eje Y se intersecan (0, 0), como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="265ed-142">Visuals are positioned relative to the origin, which is the point where the x-axis and y-axis intersect (0, 0), as shown in the following illustration.</span></span>

![los ejes X e Y de un espacio de coordenadas con la mano izquierda](images/coordinatespace.png)

<span data-ttu-id="265ed-144">Al manipular valores en una matriz de transformación 3 por 2, puede girar, escalar, sesgar y traducir un objeto en dos dimensiones.</span><span class="sxs-lookup"><span data-stu-id="265ed-144">By manipulating values in a 3-by-2 transformation matrix, you can rotate, scale, skew, and translate an object in two dimensions.</span></span> <span data-ttu-id="265ed-145">Por ejemplo, si establece OffsetX en 100 y OffsetY en 200, mueva el objeto a la derecha 100 píxeles y 200 píxeles hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="265ed-145">For example, if you set OffsetX to 100 and OffsetY to 200, you move the object to the right 100 pixels and down 200 pixels.</span></span>

## <a name="support-for-affine-2d-transforms"></a><span data-ttu-id="265ed-146">Compatibilidad con transformaciones 2D afín</span><span class="sxs-lookup"><span data-stu-id="265ed-146">Support for affine 2D transforms</span></span>

<span data-ttu-id="265ed-147">En la tabla siguiente se describen los tipos de transformaciones 2D afín compatibles con DirectComposition y se enumeran las interfaces que puede usar para realizar los distintos tipos de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="265ed-147">The following table describes the types of affine 2D transforms supported by DirectComposition, and lists the interfaces that you can use to perform the various types of transformations.</span></span>



| <span data-ttu-id="265ed-148">Transformación o interfaz</span><span class="sxs-lookup"><span data-stu-id="265ed-148">Transform/interface</span></span>                                                                               | <span data-ttu-id="265ed-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="265ed-149">Description</span></span>                                                                                              | <span data-ttu-id="265ed-150">Ilustración</span><span class="sxs-lookup"><span data-stu-id="265ed-150">Illustration</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265ed-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="265ed-151">Rotate 2D [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)\[newline\]</span></span>          | <span data-ttu-id="265ed-152">girar un objeto visual por el ángulo especificado sobre el punto central especificado.</span><span class="sxs-lookup"><span data-stu-id="265ed-152">rotate a visual by the specified angle about the specified center point.</span></span>                                 | ![ilustración de un cuadrado girado 45 grados en el sentido de las agujas del reloj sobre el centro del cuadrado original](images/rotate.png)               |
| <span data-ttu-id="265ed-154">Escala de la nueva línea [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform) \[ en 2D\]</span><span class="sxs-lookup"><span data-stu-id="265ed-154">Scale 2D [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)\[newline\]</span></span>             | <span data-ttu-id="265ed-155">escalar un objeto visual por el factor especificado sobre el punto central especificado.</span><span class="sxs-lookup"><span data-stu-id="265ed-155">scale a visual by the specified factor about the specified center point.</span></span>                                 | ![ilustración de un cuadrado escalado al 130 por ciento](images/scale.png)                                                                  |
| <span data-ttu-id="265ed-157">Sesgo 2D [**idcompositionpositionwtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="265ed-157">Skew 2D [**idcompositionskewtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)\[newline\]</span></span>                | <span data-ttu-id="265ed-158">sesga un objeto visual por el ángulo especificado a lo largo del eje X y el eje Y, y alrededor del punto central especificado.</span><span class="sxs-lookup"><span data-stu-id="265ed-158">skew a visual by the specified angle along the x-axis and y-axis, and around the specified center point.</span></span> | ![ilustración de un cuadrado sesgado a 30 grados en sentido contrario a las agujas del reloj desde el eje Y](images/skew.png)                                   |
| <span data-ttu-id="265ed-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) \[ newline\]</span><span class="sxs-lookup"><span data-stu-id="265ed-160">Translate 2D [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)\[newline\]</span></span> | <span data-ttu-id="265ed-161">cambiar la posición de un objeto visual en la dirección de los ejes X e Y.</span><span class="sxs-lookup"><span data-stu-id="265ed-161">change the position of a visual in the direction of the x-axis and y-axis.</span></span>                               | ![ilustración de un cuadrado movido 20 unidades a lo largo del eje X positivo y 10 unidades a lo largo del eje Y positivo](images/translate.png) |



 

## <a name="matrix-2d-transforms"></a><span data-ttu-id="265ed-163">Transformaciones 2D de matriz</span><span class="sxs-lookup"><span data-stu-id="265ed-163">Matrix 2D transforms</span></span>

<span data-ttu-id="265ed-164">La [**interfaz IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) permite definir su propia matriz de transformación 2D afín 3 por 2 y aplicarla a un objeto visual.</span><span class="sxs-lookup"><span data-stu-id="265ed-164">The [**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform) interface enables you to define your own 3-by-2 affine 2D transform matrix and apply it to a visual.</span></span> <span data-ttu-id="265ed-165">Esta interfaz es útil si necesita aplicar un tipo de transformación 2D afín que no está disponible a través de las otras interfaces de transformación de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="265ed-165">This interface is useful if you need to apply a type of affine 2D transform that is not available through the other DirectComposition transform interfaces.</span></span> <span data-ttu-id="265ed-166">Para definir la matriz, rellene una estructura [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) y la pase al [**método IDCompositionMatrixTransform::SetMatrix.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix)</span><span class="sxs-lookup"><span data-stu-id="265ed-166">You define the matrix by filling a [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure and passing it to the [**IDCompositionMatrixTransform::SetMatrix**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrix) method.</span></span>

## <a name="transform-groups"></a><span data-ttu-id="265ed-167">Transformar grupos</span><span class="sxs-lookup"><span data-stu-id="265ed-167">Transform Groups</span></span>

<span data-ttu-id="265ed-168">Puede usar grupos de transformación para combinar varias transformaciones en una.</span><span class="sxs-lookup"><span data-stu-id="265ed-168">You can use transform groups to combine multiple transforms into one.</span></span> <span data-ttu-id="265ed-169">Un grupo de transformación define una colección de objetos de transformación cuyas matrices se multiplican juntas en el orden en que se especifican en la colección.</span><span class="sxs-lookup"><span data-stu-id="265ed-169">A transform group defines a collection of transform objects whose matrices are multiplied together in the order in which they are specified in the collection.</span></span> <span data-ttu-id="265ed-170">A continuación, la matriz de transformación resultante se aplica al objeto visual.</span><span class="sxs-lookup"><span data-stu-id="265ed-170">The resulting transform matrix is then applied to the visual.</span></span> <span data-ttu-id="265ed-171">Un grupo de transformación genera el mismo resultado que aplicar cada transformación por separado.</span><span class="sxs-lookup"><span data-stu-id="265ed-171">A transform group produces the same result as applying each transform separately.</span></span>

<span data-ttu-id="265ed-172">Tenga en cuenta que el orden de los objetos de transformación en un grupo de transformación es importante.</span><span class="sxs-lookup"><span data-stu-id="265ed-172">Keep in mind that the order of the transform objects in a transform group is important.</span></span> <span data-ttu-id="265ed-173">Por ejemplo, si un objeto visual se gira primero, luego se escala y, a continuación, se traduce, el resultado es diferente de si el objeto visual se traduce primero, luego gira y, a continuación, se escala.</span><span class="sxs-lookup"><span data-stu-id="265ed-173">For example, if a visual is first rotated, then scaled, and then translated, the result is different than if the visual is first translated, then rotated, and then scaled.</span></span> <span data-ttu-id="265ed-174">DirectComposition siempre aplica las transformaciones a un objeto visual en el orden en que se especifican en la colección.</span><span class="sxs-lookup"><span data-stu-id="265ed-174">DirectComposition always applies the transforms to a visual in the order in which they are specified in the collection.</span></span>

<span data-ttu-id="265ed-175">Para crear un grupo de transformación, cree primero los objetos de transformación que desea incluir en el grupo y, a continuación, pase una matriz de punteros de objeto de transformación al [**método IDCompositionDevice::CreateTransformGroup.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup)</span><span class="sxs-lookup"><span data-stu-id="265ed-175">To create a transform group, first create the transform objects that you want to include in the group, and then pass an array of transform object pointers to the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method.</span></span> <span data-ttu-id="265ed-176">Después de crear un grupo de transformación, no puede agregar ni quitar ningún objeto de transformación.</span><span class="sxs-lookup"><span data-stu-id="265ed-176">After you create a transform group, you cannot add or remove any transform objects.</span></span> <span data-ttu-id="265ed-177">Sin embargo, puede modificar las propiedades de los objetos de transformación individuales de la colección y los cambios se reflejarán en la matriz de transformación resultante.</span><span class="sxs-lookup"><span data-stu-id="265ed-177">However, you can modify the properties of the individual transform objects in the collection, and the changes will be reflected in the resulting transform matrix.</span></span>

## <a name="transform-animation"></a><span data-ttu-id="265ed-178">Animación de transformación</span><span class="sxs-lookup"><span data-stu-id="265ed-178">Transform animation</span></span>

<span data-ttu-id="265ed-179">Las propiedades de una transformación se pueden animar.</span><span class="sxs-lookup"><span data-stu-id="265ed-179">The properties of a transform can be animated.</span></span> <span data-ttu-id="265ed-180">Cuando se anima una propiedad, DirectComposition cambia el valor de la propiedad a lo largo del tiempo, en lugar de todos a la vez.</span><span class="sxs-lookup"><span data-stu-id="265ed-180">When a property is animated, DirectComposition changes the value of the property over time, rather than all at once.</span></span> <span data-ttu-id="265ed-181">Esto es especialmente útil al crear transiciones.</span><span class="sxs-lookup"><span data-stu-id="265ed-181">This is particularly useful when creating transitions.</span></span> <span data-ttu-id="265ed-182">Para obtener más información, vea [Animation](animation.md).</span><span class="sxs-lookup"><span data-stu-id="265ed-182">For more information, see [Animation](animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="265ed-183">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="265ed-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="265ed-184">Conceptos de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="265ed-184">DirectComposition Concepts</span></span>](directcomposition-concepts.md)
</dt> </dl>

 

 
