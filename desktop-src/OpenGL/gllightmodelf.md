---
title: función glLightModelf (GL. h)
description: La función glLightModelf establece los parámetros del modelo de iluminación.
ms.assetid: 7002c157-514e-4102-93f7-21a0df97a5c2
keywords:
- glLightModelf (función) OpenGL
topic_type:
- apiref
api_name:
- glLightModelf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2c17f7dc82080544a9055805cf62726227c200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078894"
---
# <a name="gllightmodelf-function"></a><span data-ttu-id="9a7c6-104">glLightModelf función)</span><span class="sxs-lookup"><span data-stu-id="9a7c6-104">glLightModelf function</span></span>

<span data-ttu-id="9a7c6-105">La función **glLightModelf** establece los parámetros del modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-105">The **glLightModelf** function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7c6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a7c6-106">Syntax</span></span>


```C++
void WINAPI glLightModelf(
   GLenum  pname,
   GLfloat *param
);
```



## <a name="parameters"></a><span data-ttu-id="9a7c6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a7c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7c6-108">*PName*</span><span class="sxs-lookup"><span data-stu-id="9a7c6-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="9a7c6-109">Un parámetro de modelo de iluminación de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-109">A single-valued lighting model parameter.</span></span> <span data-ttu-id="9a7c6-110">Se aceptan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-110">The following values are accepted.</span></span>



| <span data-ttu-id="9a7c6-111">Value</span><span class="sxs-lookup"><span data-stu-id="9a7c6-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="9a7c6-112">Significado</span><span class="sxs-lookup"><span data-stu-id="9a7c6-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="9a7c6-113"><dt>**\_ \_ \_ visor local del modelo \_ de contabilidad solar**</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-113"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="9a7c6-114">El parámetro *param* es un valor de punto flotante único que especifica cómo se calculan los ángulos de reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-114">The *param* parameter is a single floating-point value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="9a7c6-115">Si *param* es 0 (o 0,0), los ángulos de reflexión especular toman la dirección de la vista para que sea paralela a y en la dirección del eje-*z* , independientemente de la ubicación del vértice en coordenadas de ojo.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-115">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="9a7c6-116">De lo contrario, las reflexiones especulares se calculan a partir del origen del sistema de coordenadas ocular.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-116">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="9a7c6-117">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-117">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="9a7c6-118"><dt>**modelo de la luz de contabilidad \_ \_ \_ dos \_ lados**</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-118"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="9a7c6-119">El parámetro *param* es un valor de punto flotante único que especifica si se realizan cálculos de iluminación de un lado o dos lados para los polígonos.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-119">The *param* parameter is a single floating-point value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="9a7c6-120">No tiene ningún efecto en los cálculos de iluminación de puntos, líneas o mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-120">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="9a7c6-121">Si *param* es 0 (o 0,0), se especifica una iluminación de un lado y solo se usan los parámetros de material frontal en la ecuación de iluminación.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-121">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="9a7c6-122">De lo contrario, se especifica la iluminación a dos caras.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-122">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="9a7c6-123">En este caso, los vértices de los polígonos hacia delante se iluminan con los parámetros del material de fondo y se invierten sus normales antes de que se evalúe la ecuación de iluminación.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-123">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="9a7c6-124">Los vértices de los polígonos frontales siempre se iluminan mediante los parámetros de material frontal, sin cambiar sus normales.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-124">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="9a7c6-125">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-125">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9a7c6-126">*param*</span><span class="sxs-lookup"><span data-stu-id="9a7c6-126">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="9a7c6-127">Valor en el que se establecerá el *parámetro* .</span><span class="sxs-lookup"><span data-stu-id="9a7c6-127">The value to which *param* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7c6-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a7c6-128">Return value</span></span>

<span data-ttu-id="9a7c6-129">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-129">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9a7c6-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9a7c6-130">Error codes</span></span>

<span data-ttu-id="9a7c6-131">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-131">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9a7c6-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a7c6-132">Name</span></span>                                                                                                  | <span data-ttu-id="9a7c6-133">Significado</span><span class="sxs-lookup"><span data-stu-id="9a7c6-133">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a7c6-134"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-134"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9a7c6-135">*PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-135">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="9a7c6-136"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9a7c6-137">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9a7c6-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9a7c6-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a7c6-138">Remarks</span></span>

<span data-ttu-id="9a7c6-139">La función **glLightModelf** establece el parámetro del modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-139">The **glLightModelf** function sets lighting model parameter.</span></span> <span data-ttu-id="9a7c6-140">El parámetro *PName* nombra un parámetro y *param* proporciona el nuevo valor. el valor o los valores de los parámetros individuales de origen de la luz.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-140">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="9a7c6-141">En el modo RGBA, el color claro de un vértice es la suma de la intensidad de la emisión material, el producto de la reflectancia ambiente material y el modelo de iluminación intensidad de ambiente completo de la escena y la contribución de cada fuente de luz habilitada.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-141">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="9a7c6-142">Cada fuente de luz contribuye a la suma de tres términos: ambiente, difuso y especular.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-142">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="9a7c6-143">La contribución de origen de luz ambiente es el producto de la reflectancia ambiente material y la intensidad ambiente de la luz.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-143">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="9a7c6-144">La contribución de fuente de luz difusa es el producto de la reflectancia difusa del material, la intensidad difusa de la luz y el producto de punto del vértice normal con el vector normalizado del vértice al origen de la luz.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-144">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="9a7c6-145">La contribución de origen de la luz especular es el producto de la reflexión especular de material, la intensidad especular de la luz y el producto de punto de los vectores de vértice a ojo y de vértice a luz normalizados, elevados a la potencia del brillo del material.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-145">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="9a7c6-146">Las tres contribuciones de fuente luminosa se atenúan equitativamente en función de la distancia entre el vértice y el origen de la luz y en la dirección de la fuente de luz, el exponente y el ángulo límite de propagación.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-146">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="9a7c6-147">Todos los productos dot se sustituyen por cero si se evalúan como un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-147">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="9a7c6-148">El componente alfa del color claro resultante se establece en el valor alfa del reflejo difuso de material.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-148">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="9a7c6-149">En el modo de índice de color, el valor del índice claro de un vértice varía entre el ambiente y los valores especulares pasados a [**glMaterial**](glmaterial-functions.md) con los índices de color de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a7c6-149">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="9a7c6-150">Los coeficientes difusos y especulares, calculados con una ponderación de (. 30,. 59, .11) de los colores de la luz, el brillo del material y las mismas ecuaciones de reflexión y atenuación que en el caso RGBA, determinan la cantidad de ambiente más allá del que se encuentra el índice resultante.</span><span class="sxs-lookup"><span data-stu-id="9a7c6-150">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="9a7c6-151">Las siguientes funciones recuperan información relacionada con la función **glLightModelf** :</span><span class="sxs-lookup"><span data-stu-id="9a7c6-151">The following functions retrieve information related to the **glLightModelf** function:</span></span>

<span data-ttu-id="9a7c6-152">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ \_ visor local del modelo de contabilidad solar \_</span><span class="sxs-lookup"><span data-stu-id="9a7c6-152">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="9a7c6-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ del modelo \_ \_ de la vista de contabilidad</span><span class="sxs-lookup"><span data-stu-id="9a7c6-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="9a7c6-154">[**glIsEnabled**](glisenabled.md) con iluminación de GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="9a7c6-154">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7c6-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a7c6-155">Requirements</span></span>



| <span data-ttu-id="9a7c6-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a7c6-156">Requirement</span></span> | <span data-ttu-id="9a7c6-157">Value</span><span class="sxs-lookup"><span data-stu-id="9a7c6-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7c6-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a7c6-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7c6-159">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9a7c6-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9a7c6-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a7c6-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7c6-161">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9a7c6-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a7c6-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a7c6-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7c6-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9a7c6-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a7c6-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a7c6-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9a7c6-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a7c6-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a7c6-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7c6-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a7c6-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a7c6-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7c6-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9a7c6-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9a7c6-170">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9a7c6-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9a7c6-171">**glLight**</span><span class="sxs-lookup"><span data-stu-id="9a7c6-171">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="9a7c6-172">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="9a7c6-172">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





