---
title: función glTexGenfv (GL. h)
description: Controla la generación de coordenadas de textura. | función glTexGenfv (GL. h)
ms.assetid: d5454d6f-16bb-47d9-9c52-da2daf491224
keywords:
- glTexGenfv (función) OpenGL
topic_type:
- apiref
api_name:
- glTexGenfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d5394b6385246f296a472ce51f2727e2738845
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104553437"
---
# <a name="gltexgenfv-function"></a><span data-ttu-id="ac8d2-105">glTexGenfv función)</span><span class="sxs-lookup"><span data-stu-id="ac8d2-105">glTexGenfv function</span></span>

<span data-ttu-id="ac8d2-106">Controla la generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac8d2-107">Syntax</span></span>


```C++
void WINAPI glTexGenfv(
         GLenum  coord,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="ac8d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac8d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac8d2-109">*coords*</span><span class="sxs-lookup"><span data-stu-id="ac8d2-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="ac8d2-110">Coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-110">A texture coordinate.</span></span> <span data-ttu-id="ac8d2-111">Debe ser uno de los siguientes: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="ac8d2-112">**PName**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="ac8d2-113">Nombre simbólico de la función de generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="ac8d2-114">*params*</span><span class="sxs-lookup"><span data-stu-id="ac8d2-114">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="ac8d2-115">Matriz de floats que contiene los coeficientes para la función de generación de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-115">An array of floats that contains the coefficients for the corresponding texture generation function.</span></span>

``` syntax
GLfloat zPlane[] = { 0.0f, 0.0f, 1.0f, 0.0f };
```

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac8d2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac8d2-116">Return value</span></span>

<span data-ttu-id="ac8d2-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ac8d2-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ac8d2-118">Error codes</span></span>

<span data-ttu-id="ac8d2-119">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ac8d2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac8d2-120">Name</span></span>                                                                                                  | <span data-ttu-id="ac8d2-121">Significado</span><span class="sxs-lookup"><span data-stu-id="ac8d2-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac8d2-122"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ac8d2-123">no se aceptó el valor de *coords* o *PName* , o bien *PName* era el \_ \_ modo de generación de texturas GL \_ y *params* no era un valor definido.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="ac8d2-124"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ac8d2-125">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ac8d2-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="ac8d2-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac8d2-126">Remarks</span></span>

<span data-ttu-id="ac8d2-127">La función **glTexGen** selecciona una función de generación de coordenadas de textura o proporciona coeficientes para una de las funciones.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-127">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="ac8d2-128">El parámetro *coords* asigna un nombre a una de las coordenadas de textura (s, t, r, q) y debe ser uno de estos símbolos: GL \_ s, GL \_ t, GL \_ r o GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-128">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="ac8d2-129">El parámetro *PName* debe ser una de estas tres constantes simbólicas: GL \_ Texture, plano de \_ \_ \_ objeto \_ o \_ plano de ojo \_ de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-129">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="ac8d2-130">Si *PName* es \_ \_ plano de objeto GL o \_ plano de ojo de contabilidad \_ , *param* contiene coeficientes para la función de generación de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-130">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="ac8d2-131">Si la función de generación de textura \_ es \_ lineal del objeto GL, la función</span><span class="sxs-lookup"><span data-stu-id="ac8d2-131">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="ac8d2-132">! [Ecuación que muestra la función glTexGen cuando la función de generación de textura es GL_OBJECT_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="ac8d2-132">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="ac8d2-133">se usa, donde g es el valor calculado para la coordenada denominada en coordenadas; P1, P2, P3 y P4 son los cuatro valores que se proporcionan en params; y x?, y?, z? y w? son las coordenadas de objeto del vértice.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-133">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="ac8d2-134">Puede usar esta función para asignar texturas al terreno mediante el nivel de mar como un plano de referencia (definido por P1, P2, P3 y P4).</span><span class="sxs-lookup"><span data-stu-id="ac8d2-134">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="ac8d2-135">La \_ función de \_ generación de coordenadas lineales del objeto GL calcula la altitud de un vértice de terreno como su distancia desde el nivel de mar; esa altitud se usa para indexar la imagen de textura y asignar la nieve blanca en picos y hierba verdes en Foothills, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-135">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="ac8d2-136">Si la función de generación de textura es \_ lineal en el ojo de contabilidad \_ , la función</span><span class="sxs-lookup"><span data-stu-id="ac8d2-136">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="ac8d2-137">! [Ecuación que muestra la función glTexGen cuando la función de generación de textura es GL_EYE_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="ac8d2-137">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="ac8d2-138">se usa, donde</span><span class="sxs-lookup"><span data-stu-id="ac8d2-138">is used, where</span></span>

![Ecuación que muestra las coordenadas del ojo del vértice.](images/tex03.png)

<span data-ttu-id="ac8d2-140">y x?, y?, z? y w? ¿las coordenadas oculares del vértice, P1, P2, P3 y P4 son los valores proporcionados en *param* y M es la matriz MODELVIEW cuando se llama a **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-140">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="ac8d2-141">Si M está mal acondicionado o singular, las coordenadas de textura generadas por la función resultante pueden ser inexactas o indefinidas.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-141">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="ac8d2-142">Tenga en cuenta que los valores de *param* definen un plano de referencia en coordenadas de ojo.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-142">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="ac8d2-143">La matriz de MODELVIEW que se aplica a ellos puede no ser la misma en vigor cuando se transforman los vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-143">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="ac8d2-144">Esta función establece un campo de coordenadas de textura que puede generar líneas de contorno dinámico en el movimiento de objetos.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-144">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="ac8d2-145">Si *PName* es el \_ \_ mapa de esfera  de contabilidad y la \_ coordenadas es GL s o GL \_ T, se generan coordenadas de textura s y t como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-145">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="ac8d2-146">Permita que u sea el vector de unidad que apunta desde el origen al vértice del polígono (en coordenadas de ojo).</span><span class="sxs-lookup"><span data-stu-id="ac8d2-146">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="ac8d2-147">Deje que n sea la normal actual, después de la transformación a las coordenadas del ojo.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-147">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="ac8d2-148">Let f = (FX () AF () FZ) T es el vector de reflexión tal que</span><span class="sxs-lookup"><span data-stu-id="ac8d2-148">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Ecuación que muestra el vector de reflexión como una función de vector de unidad y normal actual.](images/tex05.png)

<span data-ttu-id="ac8d2-150">Por último, deje que</span><span class="sxs-lookup"><span data-stu-id="ac8d2-150">Finally, let</span></span>

![Ecuación que muestra m como función del vector de reflexión.](images/tex07.png)

<span data-ttu-id="ac8d2-152">Después, los valores asignados a las coordenadas de textura i y t son</span><span class="sxs-lookup"><span data-stu-id="ac8d2-152">Then the values assigned to the i and t texture coordinates are</span></span>

![Ecuación que muestra los valores asignados a las coordenadas de textura i y t.](images/tex06.png)

<span data-ttu-id="ac8d2-154">Puede habilitar o deshabilitar una función de generación de coordenada de textura mediante [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno de los nombres de coordenadas de textura simbólicos (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R o GL \_ Texture \_ gen \_ Q) como argumento.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-154">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="ac8d2-155">Cuando esta función está habilitada, la coordenada de textura especificada se calcula según la función de generación asociada a esa coordenada.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-155">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="ac8d2-156">Cuando esta función está deshabilitada, los vértices siguientes toman la coordenada de textura especificada del conjunto actual de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-156">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="ac8d2-157">Inicialmente, todas las funciones de generación de texturas se establecen en contabilidad \_ ocular \_ lineal y están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-157">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="ac8d2-158">Ambas ecuaciones de plano s son (1, 0, 0, 0); ambas ecuaciones de plano t son (0, 1, 0, 0); y todas las ecuaciones de r y q plano son (0, 0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="ac8d2-158">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="ac8d2-159">Las siguientes funciones recuperan información relacionada con glTexGen:</span><span class="sxs-lookup"><span data-stu-id="ac8d2-159">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="ac8d2-160">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-160">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="ac8d2-161">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ Texture \_ S</span><span class="sxs-lookup"><span data-stu-id="ac8d2-161">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="ac8d2-162">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="ac8d2-162">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="ac8d2-163">[**glIsEnabled**](glisenabled.md) con el argumento GL de \_ textura \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="ac8d2-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="ac8d2-164">[**glIsEnabled**](glisenabled.md) con argument GL \_ Texture \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="ac8d2-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="ac8d2-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac8d2-165">Requirements</span></span>



| <span data-ttu-id="ac8d2-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac8d2-166">Requirement</span></span> | <span data-ttu-id="ac8d2-167">Value</span><span class="sxs-lookup"><span data-stu-id="ac8d2-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8d2-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac8d2-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ac8d2-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac8d2-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac8d2-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac8d2-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ac8d2-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac8d2-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac8d2-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac8d2-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac8d2-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ac8d2-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac8d2-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac8d2-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac8d2-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac8d2-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac8d2-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac8d2-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac8d2-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac8d2-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-180">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-180">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-181">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-181">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-182">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-182">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-183">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-183">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-184">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-184">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-185">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="ac8d2-185">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-187">glTexParameter</span><span class="sxs-lookup"><span data-stu-id="ac8d2-187">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-188">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-188">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="ac8d2-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





