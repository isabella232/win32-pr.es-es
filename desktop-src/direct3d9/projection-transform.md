---
description: Puede pensar en la transformación proyección como el control de los elementos internos de la cámara. es análogo a elegir una lente para la cámara.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Transformación de proyección (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274733"
---
# <a name="projection-transform-direct3d-9"></a><span data-ttu-id="0ad8a-103">Transformación de proyección (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0ad8a-103">Projection Transform (Direct3D 9)</span></span>

<span data-ttu-id="0ad8a-104">Puede pensar en la transformación proyección como el control de los elementos internos de la cámara. es análogo a elegir una lente para la cámara.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-104">You can think of the projection transformation as controlling the camera's internals; it is analogous to choosing a lens for the camera.</span></span> <span data-ttu-id="0ad8a-105">Este es el más complicado de los tres tipos de transformación.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-105">This is the most complicated of the three transformation types.</span></span> <span data-ttu-id="0ad8a-106">Esta explicación de la transformación proyección se organiza en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-106">This discussion of the projection transformation is organized into the following topics.</span></span>

<span data-ttu-id="0ad8a-107">La matriz de proyección es normalmente una proyección de escala y perspectiva.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-107">The projection matrix is typically a scale and perspective projection.</span></span> <span data-ttu-id="0ad8a-108">La transformación proyección convierte el frustum de visualización en una forma Cuboid.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-108">The projection transformation converts the viewing frustum into a cuboid shape.</span></span> <span data-ttu-id="0ad8a-109">Dado que el extremo cercano del frustum de visualización es más pequeño que el extremo, tiene el efecto de expandir los objetos que están cerca de la cámara. así es cómo se aplica la perspectiva a la escena.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-109">Because the near end of the viewing frustum is smaller than the far end, this has the effect of expanding objects that are near to the camera; this is how perspective is applied to the scene.</span></span>

<span data-ttu-id="0ad8a-110">En [el frustum de visualización](viewports-and-clipping.md), la distancia entre la cámara y el origen del espacio de la transformación de visualización se define arbitrariamente como D, por lo que la matriz de proyección es similar a la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-110">In [the viewing frustum](viewports-and-clipping.md), the distance between the camera and the origin of the viewing transform space is defined arbitrarily as D, so the projection matrix looks like the following illustration.</span></span>

![Ilustración de la matriz de proyección](images/projmat1.png)

<span data-ttu-id="0ad8a-112">La matriz de visualización traduce la cámara al origen mediante la conversión de la dirección z por D. La matriz de traslación es similar a la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-112">The viewing matrix translates the camera to the origin by translating in the z direction by - D. The translation matrix is like the following illustration.</span></span>

![Ilustración de la matriz de traslación](images/projmat2.png)

<span data-ttu-id="0ad8a-114">La multiplicación de la matriz de traslación por la matriz de proyección (T \* P) proporciona la matriz de proyección compuesta, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-114">Multiplying the translation matrix by the projection matrix (T\*P) gives the composite projection matrix, as shown in the following illustration.</span></span>

![Ilustración de la matriz de proyección compuesta](images/projmat3.png)

<span data-ttu-id="0ad8a-116">La transformación perspectiva convierte un frustum de visualización en un nuevo espacio de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-116">The perspective transform converts a viewing frustum into a new coordinate space.</span></span> <span data-ttu-id="0ad8a-117">Observe que el frustum se convierte en CUBOID y que el origen se desplaza desde la esquina superior derecha de la escena hasta el centro, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-117">Notice that the frustum becomes cuboid and also that the origin moves from the upper-right corner of the scene to the center, as shown in the following diagram.</span></span>

![diagrama de cómo cambia la transformación de perspectiva el frustum de visualización en un nuevo espacio de coordenadas](images/cuboid.png)

<span data-ttu-id="0ad8a-119">En la transformación perspectiva, los límites de las direcciones x e y son-1 y 1.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-119">In the perspective transform, the limits of the x- and y-directions are -1 and 1.</span></span> <span data-ttu-id="0ad8a-120">Los límites de la dirección z son 0 para el plano frontal y 1 para el plano trasero.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-120">The limits of the z-direction are 0 for the front plane and 1 for the back plane.</span></span>

<span data-ttu-id="0ad8a-121">Esta matriz convierte y escala los objetos en función de una distancia especificada de la cámara al plano de recorte cercano, pero no tiene en cuenta el campo de vista (hipercampo) y los valores z que genera para los objetos de la distancia pueden ser prácticamente idénticos, lo que dificulta las comparaciones de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-121">This matrix translates and scales objects based on a specified distance from the camera to the near clipping plane, but it doesn't consider the field of view (fov), and the z-values that it produces for objects in the distance can be nearly identical, making depth comparisons difficult.</span></span> <span data-ttu-id="0ad8a-122">La siguiente matriz aborda estos problemas y ajusta los vértices para que tengan en cuenta la relación de aspecto de la ventanilla, lo que lo convierte en una buena opción para la proyección en perspectiva.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-122">The following matrix addresses these issues, and it adjusts vertices to account for the aspect ratio of the viewport, making it a good choice for the perspective projection.</span></span>

![Ilustración de una matriz para la proyección en perspectiva](images/prjmatx1.png)

<span data-ttu-id="0ad8a-124">En esta matriz, Zn es el valor z del plano de recorte cercano.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-124">In this matrix, Zₙ is the z-value of the near clipping plane.</span></span> <span data-ttu-id="0ad8a-125">Las variables w, h y Q tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-125">The variables w, h, and Q have the following meanings.</span></span> <span data-ttu-id="0ad8a-126">Tenga en cuenta que el campo de campo y el fovk representan los campos de vista<sub>horizontal y vertical</sub> de la ventanilla, en radianes.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-126">Note that fov<sub>w</sub> and fovₖ represent the viewport's horizontal and vertical fields of view, in radians.</span></span>

![ecuaciones de los significados de variables](images/prjmatx2.png)

<span data-ttu-id="0ad8a-128">En el caso de la aplicación, el uso de ángulos de campo de vista para definir los coeficientes de escalado x e y podría no ser tan práctico como usar las dimensiones horizontal y vertical de la ventanilla (en el espacio de la cámara).</span><span class="sxs-lookup"><span data-stu-id="0ad8a-128">For your application, using field-of-view angles to define the x- and y-scaling coefficients might not be as convenient as using the viewport's horizontal and vertical dimensions (in camera space).</span></span> <span data-ttu-id="0ad8a-129">A medida que la matemáticas funciona, las dos ecuaciones siguientes para w y h usan las dimensiones de la ventanilla y son equivalentes a las ecuaciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-129">As the math works out, the following two equations for w and h use the viewport's dimensions, and are equivalent to the preceding equations.</span></span>

![ecuaciones de los significados de las variables w y h](images/prjmatx3.png)

<span data-ttu-id="0ad8a-131">En estas fórmulas, Zn representa la posición del plano de recorte cercano y las variables V<sub>w</sub> y VH representan el ancho y el alto de la ventanilla, en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-131">In these formulas, Zₙ represents the position of the near clipping plane, and the V<sub>w</sub> and Vₕ variables represent the width and height of the viewport, in camera space.</span></span>

<span data-ttu-id="0ad8a-132">En el caso de una aplicación de C++, estas dos dimensiones se corresponden directamente con los miembros width y height de la estructura [**D3DVIEWPORT9**](d3dviewport9.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad8a-132">For a C++ application, these two dimensions correspond directly to the Width and Height members of the [**D3DVIEWPORT9**](d3dviewport9.md) structure.</span></span>

<span data-ttu-id="0ad8a-133">Sea cual sea la fórmula que decida usar, asegúrese de establecer Zn en un valor tan grande como sea posible, ya que los valores z muy cercanos a la cámara no varían en gran medida.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-133">Whatever formula you decide to use, be sure to set Zₙ to as large a value as possible, because z-values extremely close to the camera don't vary by much.</span></span> <span data-ttu-id="0ad8a-134">Esto realiza comparaciones de profundidad mediante el uso de búferes z de 16 bits, algo complicado.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-134">This makes depth comparisons using 16-bit z-buffers somewhat complicated.</span></span>

<span data-ttu-id="0ad8a-135">Al igual que con las transformaciones mundo y ver, se llama al método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para establecer la transformación de proyección.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-135">As with the world and view transformations, you call the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the projection transform.</span></span>

## <a name="setting-up-a-projection-matrix"></a><span data-ttu-id="0ad8a-136">Configuración de una matriz de proyección</span><span class="sxs-lookup"><span data-stu-id="0ad8a-136">Setting Up a Projection Matrix</span></span>

<span data-ttu-id="0ad8a-137">La siguiente función de ejemplo ProjectionMatrix establece los planos de recorte delantero y posterior, así como el campo horizontal y vertical de los ángulos de vista.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-137">The following ProjectionMatrix sample function sets the front and back clipping planes, as well as the horizontal and vertical field of view angles.</span></span> <span data-ttu-id="0ad8a-138">Los campos de la vista deben ser inferiores a PI radianes.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-138">The fields of view should be less than pi radians.</span></span>


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



<span data-ttu-id="0ad8a-139">Después de crear la matriz, establézcala con [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) que especifique la \_ proyección D3DTS.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-139">After creating the matrix, set it with [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) specifying D3DTS\_PROJECTION.</span></span>

<span data-ttu-id="0ad8a-140">La biblioteca de utilidades de D3DX proporciona las siguientes funciones para ayudarle a configurar la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-140">The D3DX utility library provides the following functions to help you set up your projection matrix.</span></span>

-   [<span data-ttu-id="0ad8a-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="0ad8a-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
-   [<span data-ttu-id="0ad8a-142">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="0ad8a-142">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
-   [<span data-ttu-id="0ad8a-143">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="0ad8a-143">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
-   [<span data-ttu-id="0ad8a-144">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="0ad8a-144">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
-   [<span data-ttu-id="0ad8a-145">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="0ad8a-145">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
-   [<span data-ttu-id="0ad8a-146">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="0ad8a-146">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a><span data-ttu-id="0ad8a-147">Matriz de proyección sencilla</span><span class="sxs-lookup"><span data-stu-id="0ad8a-147">A W-Friendly Projection Matrix</span></span>

<span data-ttu-id="0ad8a-148">Direct3D puede usar el componente w de un vértice transformado por las matrices World, View y proyecciones para realizar cálculos basados en la profundidad en el búfer de profundidad o en los efectos de niebla.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-148">Direct3D can use the w-component of a vertex that has been transformed by the world, view, and projection matrices to perform depth-based calculations in depth-buffer or fog effects.</span></span> <span data-ttu-id="0ad8a-149">Los cálculos como estos requieren que la matriz de proyección normalice w sea equivalente a la z de espacio universal.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-149">Computations such as these require that your projection matrix normalize w to be equivalent to world-space z.</span></span> <span data-ttu-id="0ad8a-150">En Resumen, si la matriz de proyección incluye un coeficiente (3, 4) que no es 1, debe escalar todos los coeficientes mediante el inverso del coeficiente (3, 4) para crear una matriz adecuada.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-150">In short, if your projection matrix includes a (3,4) coefficient that is not 1, you must scale all the coefficients by the inverse of the (3,4) coefficient to make a proper matrix.</span></span> <span data-ttu-id="0ad8a-151">Si no proporciona una matriz compatible, los efectos de niebla y el almacenamiento en búfer de profundidad no se aplican correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-151">If you don't provide a compliant matrix, fog effects and depth buffering are not applied correctly.</span></span>

<span data-ttu-id="0ad8a-152">En la ilustración siguiente se muestra una matriz de proyección no compatible y la misma matriz escalada para que se habilite la niebla relativa a la vista.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-152">The following illustration shows a noncompliant projection matrix, and the same matrix scaled so that eye-relative fog will be enabled.</span></span>

![ilustraciones de una matriz de proyección no compatible y una matriz con niebla relativa a la vista](images/eyerlmx.png)

<span data-ttu-id="0ad8a-154">En las matrices anteriores, se supone que todas las variables son distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-154">In the preceding matrices, all variables are assumed to be nonzero.</span></span> <span data-ttu-id="0ad8a-155">Para obtener más información sobre la niebla relativa a la vista, consulte la [profundidad relativa a la vista en relación con la base Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="0ad8a-155">For more information about eye-relative fog, see [Eye-Relative vs. Z-Based Depth](pixel-fog.md).</span></span> <span data-ttu-id="0ad8a-156">Para obtener información sobre el almacenamiento en búfer de profundidad basado en w, vea [búferes de profundidad (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="0ad8a-156">For information about w-based depth buffering, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="0ad8a-157">Direct3D usa la matriz de proyección establecida actualmente en los cálculos de profundidad basados en w.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-157">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="0ad8a-158">Como resultado, las aplicaciones deben establecer una matriz de proyección compatible para recibir las características basadas en w deseadas, incluso si no usan Direct3D para las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="0ad8a-158">As a result, applications must set a compliant projection matrix to receive the desired w-based features, even if they do not use Direct3D for transforms.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ad8a-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ad8a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad8a-160">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="0ad8a-160">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 
