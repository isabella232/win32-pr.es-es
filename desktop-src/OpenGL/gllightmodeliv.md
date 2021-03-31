---
title: función glLightModeliv (GL. h)
description: La función glLightModeliv establece los parámetros del modelo de iluminación.
ms.assetid: 5998bb7e-d97a-47a0-b612-e6b0046aa5d2
keywords:
- glLightModeliv (función) OpenGL
topic_type:
- apiref
api_name:
- glLightModeliv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de61d53d3f4ceb9805ca5560c864379b18c65b3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803487"
---
# <a name="gllightmodeliv-function"></a><span data-ttu-id="5110d-104">glLightModeliv función)</span><span class="sxs-lookup"><span data-stu-id="5110d-104">glLightModeliv function</span></span>

<span data-ttu-id="5110d-105">La función [**glLightModeliv**](gllightiv.md) establece los parámetros del modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="5110d-105">The [**glLightModeliv**](gllightiv.md) function sets lighting model parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5110d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5110d-106">Syntax</span></span>


```C++
void WINAPI glLightModeliv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="5110d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5110d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5110d-108">*PName*</span><span class="sxs-lookup"><span data-stu-id="5110d-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="5110d-109">Parámetro de modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="5110d-109">A lighting model parameter.</span></span> <span data-ttu-id="5110d-110">Se aceptan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="5110d-110">The following values are accepted.</span></span>



| <span data-ttu-id="5110d-111">Value</span><span class="sxs-lookup"><span data-stu-id="5110d-111">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="5110d-112">Significado</span><span class="sxs-lookup"><span data-stu-id="5110d-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span><dl> <span data-ttu-id="5110d-113"><dt>**\_ambiente de \_ modelo de luz de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-113"><dt>**GL\_LIGHT\_MODEL\_AMBIENT**</dt></span></span> </dl>                 | <span data-ttu-id="5110d-114">El parámetro *params* contiene cuatro valores enteros que especifican la intensidad RGBA ambiente de toda la escena.</span><span class="sxs-lookup"><span data-stu-id="5110d-114">The *params* parameter contains four integer values that specify the ambient RGBA intensity of the entire scene.</span></span> <span data-ttu-id="5110d-115">Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="5110d-115">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="5110d-116">Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="5110d-116">Floating-point values are mapped directly.</span></span> <span data-ttu-id="5110d-117">Ninguno de los valores enteros ni de punto flotante está fijado.</span><span class="sxs-lookup"><span data-stu-id="5110d-117">Neither integer nor floating-point values are clamped.</span></span> <span data-ttu-id="5110d-118">La intensidad de la escena ambiente predeterminada es (0,2, 0,2, 0,2, 1,0).</span><span class="sxs-lookup"><span data-stu-id="5110d-118">The default ambient scene intensity is (0.2, 0.2, 0.2, 1.0).</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| <span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span><dl> <span data-ttu-id="5110d-119"><dt>**\_ \_ \_ visor local del modelo \_ de contabilidad solar**</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-119"><dt>**GL\_LIGHT\_MODEL\_LOCAL\_VIEWER**</dt></span></span> </dl> | <span data-ttu-id="5110d-120">El parámetro *params* es un valor entero único que especifica cómo se calculan los ángulos de reflexión especular.</span><span class="sxs-lookup"><span data-stu-id="5110d-120">The *params* parameter is a single integer value that specifies how specular reflection angles are computed.</span></span> <span data-ttu-id="5110d-121">Si *param* es 0 (o 0,0), los ángulos de reflexión especular toman la dirección de la vista para que sea paralela a y en la dirección del eje-*z* , independientemente de la ubicación del vértice en coordenadas de ojo.</span><span class="sxs-lookup"><span data-stu-id="5110d-121">If *param* is 0 (or 0.0), specular reflection angles take the view direction to be parallel to and in the direction of the -*z* axis, regardless of the location of the vertex in eye coordinates.</span></span> <span data-ttu-id="5110d-122">De lo contrario, las reflexiones especulares se calculan a partir del origen del sistema de coordenadas ocular.</span><span class="sxs-lookup"><span data-stu-id="5110d-122">Otherwise, specular reflections are computed from the origin of the eye coordinate system.</span></span> <span data-ttu-id="5110d-123">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="5110d-123">The default is 0.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span><dl> <span data-ttu-id="5110d-124"><dt>**modelo de la luz de contabilidad \_ \_ \_ dos \_ lados**</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-124"><dt>**GL\_LIGHT\_MODEL\_TWO\_SIDE**</dt></span></span> </dl>             | <span data-ttu-id="5110d-125">El parámetro *params* es un valor entero único que especifica si se realizan cálculos de iluminación de un lado o dos lados para los polígonos.</span><span class="sxs-lookup"><span data-stu-id="5110d-125">The *params* parameter is a single integer value that specifies whether one-sided or two-sided lighting calculations are done for polygons.</span></span> <span data-ttu-id="5110d-126">No tiene ningún efecto en los cálculos de iluminación de puntos, líneas o mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="5110d-126">It has no effect on the lighting calculations for points, lines, or bitmaps.</span></span> <span data-ttu-id="5110d-127">Si *param* es 0 (o 0,0), se especifica una iluminación de un lado y solo se usan los parámetros de material frontal en la ecuación de iluminación.</span><span class="sxs-lookup"><span data-stu-id="5110d-127">If *param* is 0 (or 0.0), one-sided lighting is specified, and only the front material parameters are used in the lighting equation.</span></span> <span data-ttu-id="5110d-128">De lo contrario, se especifica la iluminación a dos caras.</span><span class="sxs-lookup"><span data-stu-id="5110d-128">Otherwise, two-sided lighting is specified.</span></span> <br/> <span data-ttu-id="5110d-129">En este caso, los vértices de los polígonos hacia delante se iluminan con los parámetros del material de fondo y se invierten sus normales antes de que se evalúe la ecuación de iluminación.</span><span class="sxs-lookup"><span data-stu-id="5110d-129">In this case, vertices of back-facing polygons are lighted using the back material parameters, and have their normals reversed before the lighting equation is evaluated.</span></span> <span data-ttu-id="5110d-130">Los vértices de los polígonos frontales siempre se iluminan mediante los parámetros de material frontal, sin cambiar sus normales.</span><span class="sxs-lookup"><span data-stu-id="5110d-130">Vertices of front-facing polygons are always lighted using the front material parameters, with no change to their normals.</span></span> <span data-ttu-id="5110d-131">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="5110d-131">The default is 0.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5110d-132">*params*</span><span class="sxs-lookup"><span data-stu-id="5110d-132">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="5110d-133">Puntero al valor o valores en los que se establecerán los *parámetros* .</span><span class="sxs-lookup"><span data-stu-id="5110d-133">A pointer to the value or values to which *params* will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5110d-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5110d-134">Return value</span></span>

<span data-ttu-id="5110d-135">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5110d-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5110d-136">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5110d-136">Error codes</span></span>

<span data-ttu-id="5110d-137">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="5110d-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5110d-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="5110d-138">Name</span></span>                                                                                                  | <span data-ttu-id="5110d-139">Significado</span><span class="sxs-lookup"><span data-stu-id="5110d-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5110d-140"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5110d-141">*PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="5110d-141">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="5110d-142"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5110d-143">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5110d-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5110d-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5110d-144">Remarks</span></span>

<span data-ttu-id="5110d-145">La función **glLightModeliv** establece el parámetro del modelo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="5110d-145">The **glLightModeliv** function sets lighting model parameter.</span></span> <span data-ttu-id="5110d-146">El parámetro *PName* nombra un parámetro y *param* proporciona el nuevo valor. el valor o los valores de los parámetros individuales de origen de la luz.</span><span class="sxs-lookup"><span data-stu-id="5110d-146">The *pname* parameter names a parameter and *param* gives the new value.the value or values of individual light source parameters.</span></span>

<span data-ttu-id="5110d-147">En el modo RGBA, el color claro de un vértice es la suma de la intensidad de la emisión material, el producto de la reflectancia ambiente material y el modelo de iluminación intensidad de ambiente completo de la escena y la contribución de cada fuente de luz habilitada.</span><span class="sxs-lookup"><span data-stu-id="5110d-147">In RGBA mode, the lighted color of a vertex is the sum of the material emission intensity, the product of the material ambient reflectance and the lighting model full-scene ambient intensity, and the contribution of each enabled light source.</span></span> <span data-ttu-id="5110d-148">Cada fuente de luz contribuye a la suma de tres términos: ambiente, difuso y especular.</span><span class="sxs-lookup"><span data-stu-id="5110d-148">Each light source contributes the sum of three terms: ambient, diffuse, and specular.</span></span>

-   <span data-ttu-id="5110d-149">La contribución de origen de luz ambiente es el producto de la reflectancia ambiente material y la intensidad ambiente de la luz.</span><span class="sxs-lookup"><span data-stu-id="5110d-149">The ambient light source contribution is the product of the material ambient reflectance and the light's ambient intensity.</span></span>
-   <span data-ttu-id="5110d-150">La contribución de fuente de luz difusa es el producto de la reflectancia difusa del material, la intensidad difusa de la luz y el producto de punto del vértice normal con el vector normalizado del vértice al origen de la luz.</span><span class="sxs-lookup"><span data-stu-id="5110d-150">The diffuse light source contribution is the product of the material diffuse reflectance, the light's diffuse intensity, and the dot product of the vertex's normal with the normalized vector from the vertex to the light source.</span></span>
-   <span data-ttu-id="5110d-151">La contribución de origen de la luz especular es el producto de la reflexión especular de material, la intensidad especular de la luz y el producto de punto de los vectores de vértice a ojo y de vértice a luz normalizados, elevados a la potencia del brillo del material.</span><span class="sxs-lookup"><span data-stu-id="5110d-151">The specular light source contribution is the product of the material specular reflectance, the light's specular intensity, and the dot product of the normalized vertex-to-eye and vertex-to-light vectors, raised to the power of the shininess of the material.</span></span>

<span data-ttu-id="5110d-152">Las tres contribuciones de fuente luminosa se atenúan equitativamente en función de la distancia entre el vértice y el origen de la luz y en la dirección de la fuente de luz, el exponente y el ángulo límite de propagación.</span><span class="sxs-lookup"><span data-stu-id="5110d-152">All three light source contributions are attenuated equally based on the distance from the vertex to the light source and on light source direction, spread exponent, and spread cutoff angle.</span></span> <span data-ttu-id="5110d-153">Todos los productos dot se sustituyen por cero si se evalúan como un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="5110d-153">All dot products are replaced with zero if they evaluate to a negative value.</span></span>

<span data-ttu-id="5110d-154">El componente alfa del color claro resultante se establece en el valor alfa del reflejo difuso de material.</span><span class="sxs-lookup"><span data-stu-id="5110d-154">The alpha component of the resulting lighted color is set to the alpha value of the material diffuse reflectance.</span></span>

<span data-ttu-id="5110d-155">En el modo de índice de color, el valor del índice claro de un vértice varía entre el ambiente y los valores especulares pasados a [**glMaterial**](glmaterial-functions.md) con los índices de color de GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5110d-155">In color-index mode, the value of the lighted index of a vertex ranges from the ambient to the specular values passed to [**glMaterial**](glmaterial-functions.md) using GL\_COLOR\_INDEXES.</span></span> <span data-ttu-id="5110d-156">Los coeficientes difusos y especulares, calculados con una ponderación de (. 30,. 59, .11) de los colores de la luz, el brillo del material y las mismas ecuaciones de reflexión y atenuación que en el caso RGBA, determinan la cantidad de ambiente más allá del que se encuentra el índice resultante.</span><span class="sxs-lookup"><span data-stu-id="5110d-156">Diffuse and specular coefficients, computed with a (.30, .59, .11) weighting of the light's colors, the shininess of the material, and the same reflection and attenuation equations as in the RGBA case, determine how much above ambient the resulting index is.</span></span>

<span data-ttu-id="5110d-157">Las siguientes funciones recuperan información relacionada con la función **glLightModeliv** :</span><span class="sxs-lookup"><span data-stu-id="5110d-157">The following functions retrieve information related to the **glLightModeliv** function:</span></span>

<span data-ttu-id="5110d-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ \_ visor local del modelo de contabilidad solar \_</span><span class="sxs-lookup"><span data-stu-id="5110d-158">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_LOCAL\_VIEWER</span></span>

<span data-ttu-id="5110d-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ del modelo \_ \_ de la vista de contabilidad</span><span class="sxs-lookup"><span data-stu-id="5110d-159">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIGHT\_MODEL\_TWO\_SIDE</span></span>

<span data-ttu-id="5110d-160">[**glIsEnabled**](glisenabled.md) con iluminación de GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="5110d-160">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="5110d-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5110d-161">Requirements</span></span>



| <span data-ttu-id="5110d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="5110d-162">Requirement</span></span> | <span data-ttu-id="5110d-163">Value</span><span class="sxs-lookup"><span data-stu-id="5110d-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5110d-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5110d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="5110d-165">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5110d-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5110d-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5110d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="5110d-167">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5110d-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5110d-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5110d-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="5110d-169"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-169"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5110d-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5110d-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="5110d-171"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-171"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5110d-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5110d-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5110d-173"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5110d-173"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5110d-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="5110d-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5110d-175">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5110d-175">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5110d-176">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5110d-176">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5110d-177">**glLight**</span><span class="sxs-lookup"><span data-stu-id="5110d-177">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="5110d-178">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5110d-178">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





