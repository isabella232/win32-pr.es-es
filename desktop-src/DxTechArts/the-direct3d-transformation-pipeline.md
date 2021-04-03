---
title: La canalización de transformación de Direct3D
description: En este artículo se proporciona una explicación técnica para que los desarrolladores de aplicaciones de Direct3D establezcan los parámetros de la canalización de transformación de Direct3D mediante la manipulación directa de las matrices de Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "103913942"
---
# <a name="the-direct3d-transformation-pipeline"></a><span data-ttu-id="be604-103">La canalización de transformación de Direct3D</span><span class="sxs-lookup"><span data-stu-id="be604-103">The Direct3D Transformation Pipeline</span></span>

<span data-ttu-id="be604-104">En este artículo se proporciona una explicación técnica para que los desarrolladores de aplicaciones de Direct3D establezcan los parámetros de la canalización de transformación de Direct3D mediante la manipulación directa de las matrices de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="be604-104">This article provides a technical explanation for Direct3D application developers on how to set the parameters of the Direct3D Transformation Pipeline by the direct manipulation of Direct3D matrices.</span></span>

-   [<span data-ttu-id="be604-105">Información general</span><span class="sxs-lookup"><span data-stu-id="be604-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="be604-106">La canalización de transformación</span><span class="sxs-lookup"><span data-stu-id="be604-106">The Transformation Pipeline</span></span>](#the-transformation-pipeline)
-   [<span data-ttu-id="be604-107">Sugerencias de uso</span><span class="sxs-lookup"><span data-stu-id="be604-107">Usage Tips</span></span>](#usage-tips)

## <a name="overview"></a><span data-ttu-id="be604-108">Información general</span><span class="sxs-lookup"><span data-stu-id="be604-108">Overview</span></span>

<span data-ttu-id="be604-109">Direct3D usa tres transformaciones para cambiar las coordenadas del modelo 3D por coordenadas de píxeles (espacio de pantalla).</span><span class="sxs-lookup"><span data-stu-id="be604-109">Direct3D uses three transformations to change your 3D model coordinates into pixel coordinates (screen space).</span></span> <span data-ttu-id="be604-110">Estas transformaciones son transformación universal, transformación de vista y transformación de proyección.</span><span class="sxs-lookup"><span data-stu-id="be604-110">These transformations are world transform, view transform, and projection transform.</span></span>

<span data-ttu-id="be604-111">Transformación universal controla cómo se transforman las coordenadas del modelo en coordenadas universales.</span><span class="sxs-lookup"><span data-stu-id="be604-111">World transform controls how model coordinates are transformed into world coordinates.</span></span> <span data-ttu-id="be604-112">La transformación universal puede incluir traducciones, giros y escalado, pero no se aplica a las luces.</span><span class="sxs-lookup"><span data-stu-id="be604-112">World transform can include translations, rotations, and scalings, but it does not apply to lights.</span></span> <span data-ttu-id="be604-113">Para obtener más información sobre cómo trabajar con las transformaciones del mundo, vea [universal Transform](/windows/desktop/direct3d9/world-transform).</span><span class="sxs-lookup"><span data-stu-id="be604-113">For more information on working with world transforms, see [World Transform](/windows/desktop/direct3d9/world-transform).</span></span>

<span data-ttu-id="be604-114">La transformación de vista controla la transición de coordenadas universales a "espacio de la cámara", que determina la posición de la cámara en el mundo.</span><span class="sxs-lookup"><span data-stu-id="be604-114">View transform controls the transition from world coordinates into "camera space," determining camera position in the world.</span></span> <span data-ttu-id="be604-115">Para obtener un ejemplo de cómo trabajar con transformaciones de vista, vea vista de la [transformación](/windows/desktop/direct3d9/view-transform).</span><span class="sxs-lookup"><span data-stu-id="be604-115">For an example of working with view transforms, see [View Transform](/windows/desktop/direct3d9/view-transform).</span></span>

<span data-ttu-id="be604-116">La transformación de proyección cambia la geometría del espacio de la cámara a "espacio de recorte" y aplica la distorsión de la perspectiva.</span><span class="sxs-lookup"><span data-stu-id="be604-116">Projection transform changes the geometry from camera space into "clip space" and applies perspective distortion.</span></span> <span data-ttu-id="be604-117">El término "espacio de recorte" se refiere al modo en que la geometría se recorta en el volumen de la vista durante esta transformación.</span><span class="sxs-lookup"><span data-stu-id="be604-117">The term "clip space" refers to how the geometry is clipped to the view volume during this transform.</span></span> <span data-ttu-id="be604-118">Para obtener un ejemplo de cómo trabajar con transformaciones de proyección, consulte [transformación de proyección](/windows/desktop/direct3d9/projection-transform).</span><span class="sxs-lookup"><span data-stu-id="be604-118">For an example of working with projection transforms, see [Projection Transform](/windows/desktop/direct3d9/projection-transform).</span></span>

<span data-ttu-id="be604-119">Por último, la geometría en el espacio de recorte se transforma en coordenadas de píxeles (espacio de pantalla).</span><span class="sxs-lookup"><span data-stu-id="be604-119">Finally, the geometry in clip space is transformed into pixel coordinates (screen space).</span></span> <span data-ttu-id="be604-120">Esta transformación se controla mediante la configuración de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="be604-120">This transformation is controlled by the viewport settings.</span></span>

<span data-ttu-id="be604-121">Los vértices de recorte y transformación deben tener lugar en el espacio homogéneo (simplemente Put, espacio en el que el sistema de coordenadas incluye un cuarto elemento), pero el resultado final de la mayoría de las aplicaciones deben ser coordenadas tridimensionales (3D) no homogéneas definidas en "espacio de pantalla".</span><span class="sxs-lookup"><span data-stu-id="be604-121">Clipping and transforming vertices must take place in homogenous space (simply put, space in which the coordinate system includes a fourth element), but the final result for most applications needs to be non-homogenous three-dimensional (3D) coordinates defined in "screen space."</span></span> <span data-ttu-id="be604-122">Esto significa que tanto los vértices de entrada como el volumen de recorte deben traducirse en un espacio homogéneo para realizar el recorte y, a continuación, convertirse en el espacio no homogéneo que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="be604-122">This means that both the input vertices and the clipping volume must be translated into homogenous space to perform the clipping and then translated back into non-homogenous space to be displayed.</span></span>

<span data-ttu-id="be604-123">Las tres transformaciones de Direct3D (mundo, vista y transformación de proyección) están definidas por matrices de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="be604-123">The three Direct3D transformations-world, view, and projection transform-are defined by Direct3D matrices.</span></span> <span data-ttu-id="be604-124">Una matriz de Direct3D es una matriz homogénea 4x4 definida por una estructura [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) .</span><span class="sxs-lookup"><span data-stu-id="be604-124">A Direct3D matrix is a 4x4 homogenous matrix defined by a [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) structure.</span></span> <span data-ttu-id="be604-125">Aunque las matrices de Direct3D no son objetos estándar, no se representan mediante una interfaz COM, puede crearlas y establecerlas tal y como lo haría con cualquier otro objeto de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="be604-125">Although Direct3D matrices are not standard objects-they are not represented by a COM interface-you can create and set them just as you would any other Direct3D object.</span></span> <span data-ttu-id="be604-126">Para obtener más información sobre las matrices de Direct3D, vea [transformaciones](/windows/desktop/direct3d9/transforms).</span><span class="sxs-lookup"><span data-stu-id="be604-126">For more information on Direct3D matrices, see [Transforms](/windows/desktop/direct3d9/transforms).</span></span>

## <a name="the-transformation-pipeline"></a><span data-ttu-id="be604-127">La canalización de transformación</span><span class="sxs-lookup"><span data-stu-id="be604-127">The Transformation Pipeline</span></span>

<span data-ttu-id="be604-128">Si el vértice de la coordenada del modelo viene dado por PM = (XM, YM, ZM, 1), las transformaciones que se muestran en la siguiente ilustración se aplican a las coordenadas de la pantalla de proceso PS = (XS, calendario, ZS, WS).</span><span class="sxs-lookup"><span data-stu-id="be604-128">If a vertex in the model coordinate is given by Pm = (Xm, Ym, Zm, 1), then the transformations shown in the following figure are applied to compute screen coordinates Ps = (Xs, Ys, Zs, Ws).</span></span>

![espacio de modelo para transformación de espacio de pantalla](images/d3dxfrm61.gif)

<span data-ttu-id="be604-130">Estas son las descripciones de las fases que se muestran en la ilustración anterior:</span><span class="sxs-lookup"><span data-stu-id="be604-130">Here are descriptions of the stages that are shown in the preceding figure:</span></span>

1.  <span data-ttu-id="be604-131">World Matrix Mworld transforma los vértices del espacio del modelo al espacio del mundo.</span><span class="sxs-lookup"><span data-stu-id="be604-131">World matrix Mworld transforms vertices from the model space to the world space.</span></span> <span data-ttu-id="be604-132">Esta matriz se establece mediante:</span><span class="sxs-lookup"><span data-stu-id="be604-132">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    <span data-ttu-id="be604-133">La implementación de Direct3D supone que la última columna de esta matriz es (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="be604-133">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="be604-134">No se devuelve ningún error si el usuario especifica una matriz con una última columna diferente, pero la iluminación y la niebla serán incorrectas.</span><span class="sxs-lookup"><span data-stu-id="be604-134">No error is returned if the user specifies a matrix with a different last column, but the lighting and fog will be incorrect.</span></span>

2.  <span data-ttu-id="be604-135">View Matrix MView transforma los vértices del espacio universal en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="be604-135">View matrix Mview transforms vertices from the world space to the camera space.</span></span> <span data-ttu-id="be604-136">Esta matriz se establece mediante:</span><span class="sxs-lookup"><span data-stu-id="be604-136">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    <span data-ttu-id="be604-137">La implementación de Direct3D supone que la última columna de esta matriz es (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="be604-137">Direct3D implementation assumes that the last column of this matrix is (0, 0, 0, 1).</span></span> <span data-ttu-id="be604-138">No se devuelve ningún error si el usuario especifica una matriz con una última columna distinta, pero la iluminación y la niebla serán incorrectas.</span><span class="sxs-lookup"><span data-stu-id="be604-138">No error is returned if the user specifies a matrix with different last column, but the lighting and fog will be incorrect.</span></span>

3.  <span data-ttu-id="be604-139">La matriz de proyección Mproj transforma los vértices del espacio de la cámara en el espacio de proyección.</span><span class="sxs-lookup"><span data-stu-id="be604-139">Projection matrix Mproj transforms vertices from the camera space to the projection space.</span></span> <span data-ttu-id="be604-140">Esta matriz se establece mediante:</span><span class="sxs-lookup"><span data-stu-id="be604-140">This matrix is set by:</span></span>

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    <span data-ttu-id="be604-141">La última columna de la matriz de proyección debe ser (0, 0, 1, 0) o (0, 0, a, 0) para los efectos de niebla e iluminación correctos. se prefiere el formato (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="be604-141">The last column of the projection matrix should be (0, 0, 1, 0), or (0, 0, a, 0) for correct fog and lighting effects; (0, 0, 1, 0) form is preferred.</span></span>

    <span data-ttu-id="be604-142">El volumen de recorte para todos los puntos XP = (XP, es, ZP, WP) en el espacio de proyección se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="be604-142">Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:</span></span>

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    <span data-ttu-id="be604-143">Se recortarán todos los puntos que no cumplan estas ecuaciones.</span><span class="sxs-lookup"><span data-stu-id="be604-143">All points that do not satisfy these equations will be clipped.</span></span>

    <span data-ttu-id="be604-144">Si un volumen de vista se define como:</span><span class="sxs-lookup"><span data-stu-id="be604-144">If a view volume is defined as:</span></span>

    -   <span data-ttu-id="be604-145">Ancho de la ventana de la pantalla en el espacio de la cámara en el plano de recorte cercano</span><span class="sxs-lookup"><span data-stu-id="be604-145">Sw-screen window width in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="be604-146">Alto de la ventana de la pantalla sh en el espacio de la cámara en el plano de recorte cercano</span><span class="sxs-lookup"><span data-stu-id="be604-146">Sh-screen window height in camera space in near clipping plane</span></span>
    -   <span data-ttu-id="be604-147">Zn: distancia al plano de recorte cercano a lo largo de los ejes Z del espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="be604-147">Zn-distance to the near clipping plane along Z axes in camera space</span></span>
    -   <span data-ttu-id="be604-148">ZF: distancia al plano de recorte lejano a lo largo de los ejes Z del espacio de la cámara</span><span class="sxs-lookup"><span data-stu-id="be604-148">Zf-distance to the far clipping plane along Z axes in camera space</span></span>

    <span data-ttu-id="be604-149">después, una matriz de proyección de perspectiva se podría escribir de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="be604-149">then a perspective projection matrix could be written as follows:</span></span>

    ![Muestra una matriz de proyección de perspectiva.](images/d3dxfrm62.gif)

    <span data-ttu-id="be604-151">donde mij son miembros de Mproj.</span><span class="sxs-lookup"><span data-stu-id="be604-151">where Mij are members of Mproj.</span></span>

    <span data-ttu-id="be604-152">Para la proyección ortogonal que tenemos:</span><span class="sxs-lookup"><span data-stu-id="be604-152">For the orthogonal projection we have:</span></span>

    ![proyección ortogonal](images/d3dxfrm63.gif)

    <span data-ttu-id="be604-154">Direct3D supone que la matriz de proyección de perspectiva tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="be604-154">Direct3D assumes that the perspective projection matrix has the form:</span></span>

    ![matriz de proyección de perspectiva](images/d3dxfrm64.gif)

    <span data-ttu-id="be604-156">Si la matriz de proyección de perspectiva no tiene este formato, habrá algunos artefactos.</span><span class="sxs-lookup"><span data-stu-id="be604-156">If the perspective projection matrix does not have this form, there will be some artifacts.</span></span> <span data-ttu-id="be604-157">Por ejemplo, la niebla de tabla no funcionará.</span><span class="sxs-lookup"><span data-stu-id="be604-157">For example, table fog will not work.</span></span>

4.  <span data-ttu-id="be604-158">Direct3D permite al usuario cambiar el volumen de la imagen de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="be604-158">Direct3D allows the user to change the clip volume as follows:</span></span>

    ![cambiar el volumen del clip](images/d3dxfrm65.gif)

    <span data-ttu-id="be604-160">Esto se puede volver a escribir de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="be604-160">This can be rewritten as:</span></span>

    ![cambiar el volumen de clip reescrito](images/d3dxfrm66.gif)

    <span data-ttu-id="be604-162">donde:</span><span class="sxs-lookup"><span data-stu-id="be604-162">where:</span></span>

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    <span data-ttu-id="be604-163">Esta transformación puede proporcionar mayor precisión y es equivalente a escalar y desplazar el volumen de recorte.</span><span class="sxs-lookup"><span data-stu-id="be604-163">This transformation can provide increased precision and is equivalent to scaling and shifting the clipping volume.</span></span>

    <span data-ttu-id="be604-164">La matriz de Mclip correspondiente es:</span><span class="sxs-lookup"><span data-stu-id="be604-164">The corresponding Mclip matrix is:</span></span>

    ![matriz mclip](images/d3dxfrm67.gif)

    <span data-ttu-id="be604-166">Un vértice se transforma por:</span><span class="sxs-lookup"><span data-stu-id="be604-166">A vertex is transformed by:</span></span>

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    <span data-ttu-id="be604-167">Si no desea escalar el volumen de clip, puede establecer los parámetros de la ventanilla en valores predeterminados:</span><span class="sxs-lookup"><span data-stu-id="be604-167">If you do not want to scale the clip volume, you can set viewport parameters to default values:</span></span>

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  <span data-ttu-id="be604-168">La fase de recorte es opcional si el usuario especifica la \_ marca D3DDP DONOTCLIP en una llamada DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="be604-168">The clipping stage is optional if the user specifies the D3DDP\_DONOTCLIP flag in a DrawPrimitive call.</span></span> <span data-ttu-id="be604-169">En este caso, se pueden combinar todas las matrices (incluido MVS).</span><span class="sxs-lookup"><span data-stu-id="be604-169">In this case, all matrices (including Mvs) can be combined.</span></span>
6.  <span data-ttu-id="be604-170">La matriz de escala de ventanilla MVS escala las coordenadas para que estén dentro de la ventana de ventanilla y voltea el eje Y de arriba a abajo:</span><span class="sxs-lookup"><span data-stu-id="be604-170">The viewport scale matrix Mvs scales coordinates to be within the viewport window and flips the Y axis from up to down:</span></span>

    ![matriz de escala de ventanilla MVS](images/d3dxfrm68.gif)

    <span data-ttu-id="be604-172">donde:</span><span class="sxs-lookup"><span data-stu-id="be604-172">where:</span></span>

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  <span data-ttu-id="be604-173">Por último, las coordenadas de pantalla se calculan y se pasan al rasterizador:</span><span class="sxs-lookup"><span data-stu-id="be604-173">Finally, screen coordinates are computed and passed to the rasterizer:</span></span>

    ![coordenadas de pantalla calculadas y pasadas al rasterizador](images/d3dxfrm69.gif)

## <a name="usage-tips"></a><span data-ttu-id="be604-175">Sugerencias de uso</span><span class="sxs-lookup"><span data-stu-id="be604-175">Usage Tips</span></span>

<span data-ttu-id="be604-176">A continuación se muestran algunas sugerencias sobre cómo usar la canalización de transformación de Direct3D:</span><span class="sxs-lookup"><span data-stu-id="be604-176">Here are some tips for how to use the Direct3D Transformation Pipeline:</span></span>

-   <span data-ttu-id="be604-177">La última columna del mundo y las matrices de la vista deben ser (0, 0, 0, 1) o la iluminación será incorrecta.</span><span class="sxs-lookup"><span data-stu-id="be604-177">The last column of the world and view matrices should be (0, 0, 0, 1), or the lighting will be incorrect.</span></span>
-   <span data-ttu-id="be604-178">Establezca los parámetros de la ventanilla para compilar una matriz de Mclip de identidad, a menos que comprenda exactamente lo que se necesita para.</span><span class="sxs-lookup"><span data-stu-id="be604-178">Set the viewport parameters to build an identity Mclip matrix, unless you understand exactly what it is needed for.</span></span>

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 