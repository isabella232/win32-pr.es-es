---
title: función glTexGeni (GL. h)
description: Controla la generación de coordenadas de textura. | función glTexGeni (GL. h)
ms.assetid: beffcb24-c99b-4b2a-a9c3-2c2cc1afe5e5
keywords:
- glTexGeni (función) OpenGL
topic_type:
- apiref
api_name:
- glTexGeni
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20bb1121a8f125f06bf8e6e18f56c96fbeeb692d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104551617"
---
# <a name="gltexgeni-function"></a><span data-ttu-id="e35b2-105">glTexGeni función)</span><span class="sxs-lookup"><span data-stu-id="e35b2-105">glTexGeni function</span></span>

<span data-ttu-id="e35b2-106">Controla la generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e35b2-106">Controls the generation of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e35b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e35b2-107">Syntax</span></span>


```C++
void WINAPI glTexGeni(
   GLenum coord,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="e35b2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e35b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e35b2-109">*coords*</span><span class="sxs-lookup"><span data-stu-id="e35b2-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="e35b2-110">Coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="e35b2-110">A texture coordinate.</span></span> <span data-ttu-id="e35b2-111">Debe ser uno de los siguientes: GL \_ S, GL \_ T, GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="e35b2-111">Must be one of the following: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="e35b2-112">**PName**</span><span class="sxs-lookup"><span data-stu-id="e35b2-112">**pname**</span></span> 
</dt> <dd>

<span data-ttu-id="e35b2-113">Nombre simbólico de la función de generación de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e35b2-113">The symbolic name of the texture coordinate generation function.</span></span>

</dd> <dt>

<span data-ttu-id="e35b2-114">*param*</span><span class="sxs-lookup"><span data-stu-id="e35b2-114">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="e35b2-115">Parámetro de generación de textura con un solo valor, uno de los \_ objetos GL \_ linear, GL \_ ocular \_ lineal o el mapa de la \_ esfera GL \_ .</span><span class="sxs-lookup"><span data-stu-id="e35b2-115">A single valued texture generation parameter, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e35b2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e35b2-116">Return value</span></span>

<span data-ttu-id="e35b2-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e35b2-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e35b2-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e35b2-118">Error codes</span></span>

<span data-ttu-id="e35b2-119">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="e35b2-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e35b2-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e35b2-120">Name</span></span>                                                                                                  | <span data-ttu-id="e35b2-121">Significado</span><span class="sxs-lookup"><span data-stu-id="e35b2-121">Meaning</span></span>                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e35b2-122"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e35b2-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e35b2-123">no se aceptó el valor de *coords* o *PName* , o bien *PName* era el \_ \_ modo de generación de texturas GL \_ y *params* no era un valor definido.</span><span class="sxs-lookup"><span data-stu-id="e35b2-123">*coord* or *pname* was not an accepted defined value, or *pname* was GL\_TEXTURE\_GEN\_MODE and *params* was not an accepted defined value.</span></span><br/> |
| <dl> <span data-ttu-id="e35b2-124"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e35b2-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e35b2-125">*PName* era el \_ \_ modo gen \_ de textura GL, *params* era el mapa de la \_ esfera de contabilidad y la \_ de *coordenadas* era GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="e35b2-125">*pname* was GL\_TEXTURE\_GEN\_MODE, *params* was GL\_SPHERE\_MAP, and *coord* was either GL\_R or GL\_Q</span></span><br/>                                     |
| <dl> <span data-ttu-id="e35b2-126"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e35b2-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e35b2-127">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e35b2-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                 |



## <a name="remarks"></a><span data-ttu-id="e35b2-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e35b2-128">Remarks</span></span>

<span data-ttu-id="e35b2-129">La función **glTexGen** selecciona una función de generación de coordenadas de textura o proporciona coeficientes para una de las funciones.</span><span class="sxs-lookup"><span data-stu-id="e35b2-129">The **glTexGen** function selects a texture-coordinate generation function or supplies coefficients for one of the functions.</span></span> <span data-ttu-id="e35b2-130">El parámetro *coords* asigna un nombre a una de las coordenadas de textura (s, t, r, q) y debe ser uno de estos símbolos: GL \_ s, GL \_ t, GL \_ r o GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="e35b2-130">The *coord* parameter names one of the (s,t,r,q) texture coordinates, and it must be one of these symbols: GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span> <span data-ttu-id="e35b2-131">El parámetro *PName* debe ser una de estas tres constantes simbólicas: GL \_ Texture, plano de \_ \_ \_ objeto \_ o \_ plano de ojo \_ de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e35b2-131">The *pname* parameter must be one of three symbolic constants: GL\_TEXTURE\_GEN\_MODE, GL\_OBJECT\_PLANE, or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="e35b2-132">Si *PName* es \_ el modo de generación de texturas GL \_ \_ , *param* especifica un modo, uno de los \_ objetos GL \_ linear, GL \_ Eye \_ linear o GL \_ Sphere \_ map.</span><span class="sxs-lookup"><span data-stu-id="e35b2-132">If *pname* is GL\_TEXTURE\_GEN\_MODE, then *param* specifies a mode, one of GL\_OBJECT\_LINEAR, GL\_EYE\_LINEAR, or GL\_SPHERE\_MAP.</span></span> <span data-ttu-id="e35b2-133">Si *PName* es \_ \_ plano de objeto GL o \_ plano de ojo de contabilidad \_ , *param* contiene coeficientes para la función de generación de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e35b2-133">If *pname* is either GL\_OBJECT\_PLANE or GL\_EYE\_PLANE, *param* contains coefficients for the corresponding texture generation function.</span></span>

<span data-ttu-id="e35b2-134">Si la función de generación de textura \_ es \_ lineal del objeto GL, la función</span><span class="sxs-lookup"><span data-stu-id="e35b2-134">If the texture generation function is GL\_OBJECT\_LINEAR, the function</span></span>

<span data-ttu-id="e35b2-135">! [Ecuación que muestra la función glTexGen cuando la función de generación de textura es GL_OBJECT_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="e35b2-135">![Equation showing the glTexGen function when the texture generation function is GL_OBJECT_LINEAR.]</span></span>

<span data-ttu-id="e35b2-136">se usa, donde g es el valor calculado para la coordenada denominada en coordenadas; P1, P2, P3 y P4 son los cuatro valores que se proporcionan en params; y x?, y?, z? y w? son las coordenadas de objeto del vértice.</span><span class="sxs-lookup"><span data-stu-id="e35b2-136">is used, where g is the value computed for the coordinate named in coord; p1, p2, p3, and p4 are the four values supplied in params; and x?, y?, z?, and w? are the object coordinates of the vertex.</span></span> <span data-ttu-id="e35b2-137">Puede usar esta función para asignar texturas al terreno mediante el nivel de mar como un plano de referencia (definido por P1, P2, P3 y P4).</span><span class="sxs-lookup"><span data-stu-id="e35b2-137">You can use this function to texture-map terrain by using sea level as a reference plane (defined by p1, p2, p3, and p4).</span></span> <span data-ttu-id="e35b2-138">La \_ función de \_ generación de coordenadas lineales del objeto GL calcula la altitud de un vértice de terreno como su distancia desde el nivel de mar; esa altitud se usa para indexar la imagen de textura y asignar la nieve blanca en picos y hierba verdes en Foothills, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e35b2-138">The GL\_OBJECT\_LINEAR coordinate generation function computes the altitude of a terrain vertex as its distance from sea level; that altitude is used to index the texture image to map white snow onto peaks and green grass onto foothills, for example.</span></span>

<span data-ttu-id="e35b2-139">Si la función de generación de textura es \_ lineal en el ojo de contabilidad \_ , la función</span><span class="sxs-lookup"><span data-stu-id="e35b2-139">If the texture generation function is GL\_EYE\_LINEAR, the function</span></span>

<span data-ttu-id="e35b2-140">! [Ecuación que muestra la función glTexGen cuando la función de generación de textura es GL_EYE_LINEAR.]</span><span class="sxs-lookup"><span data-stu-id="e35b2-140">![Equation showing the glTexGen function when the texture generation function is GL_EYE_LINEAR.]</span></span>

<span data-ttu-id="e35b2-141">se usa, donde</span><span class="sxs-lookup"><span data-stu-id="e35b2-141">is used, where</span></span>

![Ecuación que muestra las coordenadas del ojo del vértice.](images/tex03.png)

<span data-ttu-id="e35b2-143">y x?, y?, z? y w? ¿las coordenadas oculares del vértice, P1, P2, P3 y P4 son los valores proporcionados en *param* y M es la matriz MODELVIEW cuando se llama a **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="e35b2-143">and x?, y?, z?, and w? are the eye coordinates of the vertex, p1, p2, p3, and p4 are the values supplied in *param*, and M is the modelview matrix when you call **glTexGen**.</span></span> <span data-ttu-id="e35b2-144">Si M está mal acondicionado o singular, las coordenadas de textura generadas por la función resultante pueden ser inexactas o indefinidas.</span><span class="sxs-lookup"><span data-stu-id="e35b2-144">If M is poorly conditioned or singular, texture coordinates generated by the resulting function can be inaccurate or undefined.</span></span>

<span data-ttu-id="e35b2-145">Tenga en cuenta que los valores de *param* definen un plano de referencia en coordenadas de ojo.</span><span class="sxs-lookup"><span data-stu-id="e35b2-145">Note that the values in *param* define a reference plane in eye coordinates.</span></span> <span data-ttu-id="e35b2-146">La matriz de MODELVIEW que se aplica a ellos puede no ser la misma en vigor cuando se transforman los vértices del polígono.</span><span class="sxs-lookup"><span data-stu-id="e35b2-146">The modelview matrix that is applied to them may not be the same one in effect when the polygon vertices are transformed.</span></span> <span data-ttu-id="e35b2-147">Esta función establece un campo de coordenadas de textura que puede generar líneas de contorno dinámico en el movimiento de objetos.</span><span class="sxs-lookup"><span data-stu-id="e35b2-147">This function establishes a field of texture coordinates that can produce dynamic contour lines on moving objects.</span></span>

<span data-ttu-id="e35b2-148">Si *PName* es el \_ \_ mapa de esfera  de contabilidad y la \_ coordenadas es GL s o GL \_ T, se generan coordenadas de textura s y t como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e35b2-148">If *pname* is GL\_SPHERE\_MAP and *coord* is either GL\_S or GL\_T, s and t texture coordinates are generated as follows.</span></span> <span data-ttu-id="e35b2-149">Permita que u sea el vector de unidad que apunta desde el origen al vértice del polígono (en coordenadas de ojo).</span><span class="sxs-lookup"><span data-stu-id="e35b2-149">Let u be the unit vector pointing from the origin to the polygon vertex (in eye coordinates).</span></span> <span data-ttu-id="e35b2-150">Deje que n sea la normal actual, después de la transformación a las coordenadas del ojo.</span><span class="sxs-lookup"><span data-stu-id="e35b2-150">Let n  be the current normal, after transformation to eye coordinates.</span></span> <span data-ttu-id="e35b2-151">Let f = (FX () AF () FZ) T es el vector de reflexión tal que</span><span class="sxs-lookup"><span data-stu-id="e35b2-151">Let f = (fx ( ) fy ( ) fz)T be the reflection vector such that</span></span>

![Ecuación que muestra el vector de reflexión como una función de vector de unidad y normal actual.](images/tex05.png)

<span data-ttu-id="e35b2-153">Por último, deje que</span><span class="sxs-lookup"><span data-stu-id="e35b2-153">Finally, let</span></span>

![Ecuación que muestra m como función del vector de reflexión.](images/tex07.png)

<span data-ttu-id="e35b2-155">Después, los valores asignados a las coordenadas de textura i y t son</span><span class="sxs-lookup"><span data-stu-id="e35b2-155">Then the values assigned to the i and t texture coordinates are</span></span>

![Ecuación que muestra los valores asignados a las coordenadas de textura i y t.](images/tex06.png)

<span data-ttu-id="e35b2-157">Puede habilitar o deshabilitar una función de generación de coordenada de textura mediante [**glEnable**](glenable.md) o [**glDisable**](gldisable.md) con uno de los nombres de coordenadas de textura simbólicos (GL \_ Texture \_ gen \_ S, GL \_ Texture \_ gen \_ T, GL \_ Texture \_ gen \_ R o GL \_ Texture \_ gen \_ Q) como argumento.</span><span class="sxs-lookup"><span data-stu-id="e35b2-157">You can enable or disable a texture-coordinate generation function by using [**glEnable**](glenable.md) or [**glDisable**](gldisable.md) with one of the symbolic texture-coordinate names (GL\_TEXTURE\_GEN\_S, GL\_TEXTURE\_GEN\_T, GL\_TEXTURE\_GEN\_R, or GL\_TEXTURE\_GEN\_Q) as the argument.</span></span> <span data-ttu-id="e35b2-158">Cuando esta función está habilitada, la coordenada de textura especificada se calcula según la función de generación asociada a esa coordenada.</span><span class="sxs-lookup"><span data-stu-id="e35b2-158">When this function is enabled, the specified texture coordinate is computed according to the generating function associated with that coordinate.</span></span> <span data-ttu-id="e35b2-159">Cuando esta función está deshabilitada, los vértices siguientes toman la coordenada de textura especificada del conjunto actual de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e35b2-159">When this function is disabled, subsequent vertices take the specified texture coordinate from the current set of texture coordinates.</span></span> <span data-ttu-id="e35b2-160">Inicialmente, todas las funciones de generación de texturas se establecen en contabilidad \_ ocular \_ lineal y están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="e35b2-160">Initially, all texture generation functions are set to GL\_EYE\_LINEAR and are disabled.</span></span> <span data-ttu-id="e35b2-161">Ambas ecuaciones de plano s son (1, 0, 0, 0); ambas ecuaciones de plano t son (0, 1, 0, 0); y todas las ecuaciones de r y q plano son (0, 0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="e35b2-161">Both s plane equations are (1,0,0,0); both t plane equations are (0,1,0,0); and all r and q plane equations are (0,0,0,0).</span></span>

<span data-ttu-id="e35b2-162">Las siguientes funciones recuperan información relacionada con glTexGen:</span><span class="sxs-lookup"><span data-stu-id="e35b2-162">The following functions retrieve information related to glTexGen:</span></span>

<dl>

[<span data-ttu-id="e35b2-163">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="e35b2-163">**glGetTexGen**</span></span>](glgettexgen.md)  
<span data-ttu-id="e35b2-164">[**glIsEnabled**](glisenabled.md) con el argumento \_ GL \_ Texture \_ S</span><span class="sxs-lookup"><span data-stu-id="e35b2-164">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_S</span></span>  
<span data-ttu-id="e35b2-165">[**glIsEnabled**](glisenabled.md) con el argumento GL \_ Texture \_ gen \_ T</span><span class="sxs-lookup"><span data-stu-id="e35b2-165">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_T</span></span>  
<span data-ttu-id="e35b2-166">[**glIsEnabled**](glisenabled.md) con el argumento GL de \_ textura \_ gen \_ R</span><span class="sxs-lookup"><span data-stu-id="e35b2-166">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_R</span></span>  
<span data-ttu-id="e35b2-167">[**glIsEnabled**](glisenabled.md) con argument GL \_ Texture \_ gen \_ Q</span><span class="sxs-lookup"><span data-stu-id="e35b2-167">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_GEN\_Q</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="e35b2-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e35b2-168">Requirements</span></span>



| <span data-ttu-id="e35b2-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="e35b2-169">Requirement</span></span> | <span data-ttu-id="e35b2-170">Value</span><span class="sxs-lookup"><span data-stu-id="e35b2-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e35b2-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e35b2-171">Minimum supported client</span></span><br/> | <span data-ttu-id="e35b2-172">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e35b2-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e35b2-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e35b2-173">Minimum supported server</span></span><br/> | <span data-ttu-id="e35b2-174">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e35b2-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e35b2-175">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e35b2-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="e35b2-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e35b2-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e35b2-177">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e35b2-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="e35b2-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e35b2-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e35b2-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e35b2-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e35b2-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e35b2-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e35b2-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="e35b2-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e35b2-182">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e35b2-182">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e35b2-183">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e35b2-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e35b2-184">**glCopyTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="e35b2-184">**glCopyTexImage2D**</span></span>](glcopyteximage2d.md)
</dt> <dt>

[<span data-ttu-id="e35b2-185">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="e35b2-185">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="e35b2-186">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="e35b2-186">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="e35b2-187">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e35b2-187">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="e35b2-188">glTexEnv</span><span class="sxs-lookup"><span data-stu-id="e35b2-188">glTexEnv</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="e35b2-189">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="e35b2-189">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="e35b2-190">glTexParameter</span><span class="sxs-lookup"><span data-stu-id="e35b2-190">glTexParameter</span></span>](gltexparameter-functions.md)
</dt> <dt>

[<span data-ttu-id="e35b2-191">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="e35b2-191">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="e35b2-192">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="e35b2-192">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> </dl>

 

 





