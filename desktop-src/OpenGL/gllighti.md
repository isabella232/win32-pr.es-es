---
title: función glLighti (GL. h)
description: La función glLighti devuelve los valores de los parámetros de origen de la luz.
ms.assetid: 4fa5e604-d45d-412e-a08c-c38e0836596f
keywords:
- glLighti (función) OpenGL
topic_type:
- apiref
api_name:
- glLighti
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52225c4db8eaa31c17d12a25590b918cf94b4c3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905328"
---
# <a name="gllighti-function"></a><span data-ttu-id="71987-104">glLighti función)</span><span class="sxs-lookup"><span data-stu-id="71987-104">glLighti function</span></span>

<span data-ttu-id="71987-105">La función **glLighti** devuelve los valores de los parámetros de origen de la luz.</span><span class="sxs-lookup"><span data-stu-id="71987-105">The **glLighti** function returns light source parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="71987-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71987-106">Syntax</span></span>


```C++
void WINAPI glLighti(
   GLenum light,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="71987-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71987-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71987-108">*light*</span><span class="sxs-lookup"><span data-stu-id="71987-108">*light*</span></span> 
</dt> <dd>

<span data-ttu-id="71987-109">Identificador de una luz.</span><span class="sxs-lookup"><span data-stu-id="71987-109">The identifier of a light.</span></span> <span data-ttu-id="71987-110">El número de posibles luces depende de la implementación, pero se admiten al menos ocho luces.</span><span class="sxs-lookup"><span data-stu-id="71987-110">The number of possible lights depends on the implementation, but at least eight lights are supported.</span></span> <span data-ttu-id="71987-111">Se identifican por nombres simbólicos con el formato GL \_ Light *i* , donde *i* es un valor: 0 a las \_ \_ luces Max de GL-1.</span><span class="sxs-lookup"><span data-stu-id="71987-111">They are identified by symbolic names of the form GL\_LIGHT *i* where *i* is a value: 0 to GL\_MAX\_LIGHTS - 1.</span></span>

</dd> <dt>

<span data-ttu-id="71987-112">*PName*</span><span class="sxs-lookup"><span data-stu-id="71987-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="71987-113">Parámetro de origen de la luz de un solo valor para *Light*.</span><span class="sxs-lookup"><span data-stu-id="71987-113">A single-valued light source parameter for *light*.</span></span> <span data-ttu-id="71987-114">Se aceptan los siguientes nombres simbólicos.</span><span class="sxs-lookup"><span data-stu-id="71987-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="71987-115">Value</span><span class="sxs-lookup"><span data-stu-id="71987-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="71987-116">Significado</span><span class="sxs-lookup"><span data-stu-id="71987-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span><dl> <span data-ttu-id="71987-117"><dt>**exponente de la zona de contabilidad \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71987-117"><dt>**GL\_SPOT\_EXPONENT**</dt></span></span> </dl>                                                                                                                                                                             | <span data-ttu-id="71987-118">El parámetro *param* es un valor entero único que especifica la distribución de la intensidad de la luz.</span><span class="sxs-lookup"><span data-stu-id="71987-118">The *param* parameter is a single integer value that specifies the intensity distribution of the light.</span></span> <span data-ttu-id="71987-119">Los valores enteros y de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="71987-119">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="71987-120">Solo se aceptan los valores del intervalo comprendido entre \[ 0 y 128 \] .</span><span class="sxs-lookup"><span data-stu-id="71987-120">Only values in the range \[0, 128\] are accepted.</span></span> <br/> <span data-ttu-id="71987-121">La intensidad de la luz efectiva se atenúa por el coseno del ángulo entre la dirección de la luz y la dirección de la luz hasta el vértice que se ilumina, elevado a la potencia del exponente del punto.</span><span class="sxs-lookup"><span data-stu-id="71987-121">Effective light intensity is attenuated by the cosine of the angle between the direction of the light and the direction from the light to the vertex being lighted, raised to the power of the spot exponent.</span></span> <span data-ttu-id="71987-122">Por lo tanto, los exponentes más altos producen una fuente de luz más enfocada, independientemente del ángulo de corte puntual.</span><span class="sxs-lookup"><span data-stu-id="71987-122">Thus, higher spot exponents result in a more focused light source, regardless of the spot cutoff angle.</span></span> <span data-ttu-id="71987-123">El exponente de color predeterminado es 0, lo que da lugar a una distribución ligera uniforme.</span><span class="sxs-lookup"><span data-stu-id="71987-123">The default spot exponent is 0, resulting in uniform light distribution.</span></span><br/> |
| <span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span><dl> <span data-ttu-id="71987-124"><dt>**límite de la zona de contabilidad \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71987-124"><dt>**GL\_SPOT\_CUTOFF**</dt></span></span> </dl>                                                                                                                                                                                   | <span data-ttu-id="71987-125">El parámetro *param* es un valor entero único que especifica el ángulo de propagación máximo de una fuente de luz.</span><span class="sxs-lookup"><span data-stu-id="71987-125">The *param* parameter is a single integer value that specifies the maximum spread angle of a light source.</span></span> <span data-ttu-id="71987-126">Los valores enteros y de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="71987-126">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="71987-127">Solo se aceptan los valores del intervalo \[ 0, 90 \] y el valor especial 180.</span><span class="sxs-lookup"><span data-stu-id="71987-127">Only values in the range \[0, 90\], and the special value 180, are accepted.</span></span> <br/> <span data-ttu-id="71987-128">Si el ángulo entre la dirección de la luz y la dirección desde la luz hasta el vértice que se ilumina es mayor que el ángulo límite de la zona, la luz se enmascara completamente.</span><span class="sxs-lookup"><span data-stu-id="71987-128">If the angle between the direction of the light and the direction from the light to the vertex being lighted is greater than the spot cutoff angle, then the light is completely masked.</span></span> <span data-ttu-id="71987-129">De lo contrario, su intensidad se controla mediante el exponente puntual y los factores de atenuación.</span><span class="sxs-lookup"><span data-stu-id="71987-129">Otherwise, its intensity is controlled by the spot exponent and the attenuation factors.</span></span> <span data-ttu-id="71987-130">El límite de la luz predeterminada es 180, lo que da lugar a una distribución ligera uniforme.</span><span class="sxs-lookup"><span data-stu-id="71987-130">The default spot cutoff is 180, resulting in uniform light distribution.</span></span><br/>       |
| <span id="GL_CONSTANT_ATTENUATION__GL_LINEAR_ATTENUATION__GL_QUADRATIC_ATTENUATION"></span><span id="gl_constant_attenuation__gl_linear_attenuation__gl_quadratic_attenuation"></span><dl> <span data-ttu-id="71987-131"><dt>**\_ \_ atenuación de constantes de contabilidad \_ , \_ atenuación lineal de contabilidad, \_ atenuación cuadrática de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71987-131"><dt>**GL\_CONSTANT\_ATTENUATION, GL\_LINEAR\_ATTENUATION, GL\_QUADRATIC\_ATTENUATION**</dt></span></span> </dl> | <span data-ttu-id="71987-132">El parámetro *param* es un valor entero único que especifica uno de los tres factores de atenuación de luz.</span><span class="sxs-lookup"><span data-stu-id="71987-132">The *param* parameter is a single integer value that specifies one of the three light attenuation factors.</span></span> <span data-ttu-id="71987-133">Los valores enteros y de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="71987-133">Integer and floating-point values are mapped directly.</span></span> <span data-ttu-id="71987-134">Solo se aceptan valores no negativos.</span><span class="sxs-lookup"><span data-stu-id="71987-134">Only nonnegative values are accepted.</span></span> <br/> <span data-ttu-id="71987-135">Si la luz es posicional, en lugar de direccional, su intensidad se atenúa por el recíproco de la suma de: el factor constante, el factor lineal multiplicado por la distancia entre la luz y el vértice que se está iluminando, y el factor cuadrático multiplicado por el cuadrado de la misma distancia.</span><span class="sxs-lookup"><span data-stu-id="71987-135">If the light is positional, rather than directional, its intensity is attenuated by the reciprocal of the sum of: the constant factor, the linear factor multiplied by the distance between the light and the vertex being lighted, and the quadratic factor multiplied by the square of the same distance.</span></span> <span data-ttu-id="71987-136">Los factores de atenuación predeterminados son (1, 0, 0), lo que da lugar a no atenuación.</span><span class="sxs-lookup"><span data-stu-id="71987-136">The default attenuation factors are (1,0,0), resulting in no attenuation.</span></span><br/>                   |



 

</dd> <dt>

<span data-ttu-id="71987-137">*param*</span><span class="sxs-lookup"><span data-stu-id="71987-137">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="71987-138">Especifica el valor en el que se establecerá el parámetro *PName* de *luz* de origen de luz.</span><span class="sxs-lookup"><span data-stu-id="71987-138">Specifies the value that parameter *pname* of light source *light* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71987-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71987-139">Return value</span></span>

<span data-ttu-id="71987-140">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="71987-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71987-141">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="71987-141">Error codes</span></span>

<span data-ttu-id="71987-142">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="71987-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="71987-143">Nombre</span><span class="sxs-lookup"><span data-stu-id="71987-143">Name</span></span>                                                                                                  | <span data-ttu-id="71987-144">Significado</span><span class="sxs-lookup"><span data-stu-id="71987-144">Meaning</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71987-145"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71987-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="71987-146">*Light* o *PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="71987-146">*light* or *pname* was not an accepted value.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="71987-147"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71987-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="71987-148">Se especificó un valor de exponente puntual fuera del intervalo \[ 0, 128 \] o el límite de la zona se especificó fuera del intervalo comprendido entre \[ 0 y 90 \] (excepto el valor especial 180), o bien se especificó un factor de atenuación negativo.</span><span class="sxs-lookup"><span data-stu-id="71987-148">A spot exponent value was specified outside the range \[0, 128\], or spot cutoff was specified outside the range \[0, 90\] (except for the special value 180), or a negative attenuation factor was specified.</span></span><br/> |
| <dl> <span data-ttu-id="71987-149"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="71987-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="71987-150">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="71987-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="71987-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71987-151">Remarks</span></span>

<span data-ttu-id="71987-152">La función **glLighti** establece el valor o los valores de los parámetros individuales de origen de la luz.</span><span class="sxs-lookup"><span data-stu-id="71987-152">The **glLighti** function sets the value or values of individual light source parameters.</span></span> <span data-ttu-id="71987-153">El parámetro de *luz* asigna un nombre a la luz y es un nombre simbólico con el formato GL \_ Light *i*, donde 0 = *i* < las luces de contab \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="71987-153">The *light* parameter names the light and is a symbolic name of the form GL\_LIGHT *i*, where 0 = *i* < GL\_MAX\_LIGHTS.</span></span>

<span data-ttu-id="71987-154">El parámetro *PName* especifica uno de los parámetros de origen de la luz, de nuevo por nombre simbólico.</span><span class="sxs-lookup"><span data-stu-id="71987-154">The *pname* parameter specifies one of the light source parameters, again by symbolic name.</span></span> <span data-ttu-id="71987-155">El parámetro *param* es un valor único o un puntero a una matriz que contiene los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="71987-155">The *param* parameter is either a single value or a pointer to an array that contains the new values.</span></span>

<span data-ttu-id="71987-156">El cálculo de iluminación está habilitado y deshabilitado mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con iluminación de contabilidad de argumentos \_ .</span><span class="sxs-lookup"><span data-stu-id="71987-156">Lighting calculation is enabled and disabled using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_LIGHTING.</span></span> <span data-ttu-id="71987-157">Cuando está habilitada la iluminación, las fuentes de luz que están habilitadas contribuyen al cálculo de iluminación.</span><span class="sxs-lookup"><span data-stu-id="71987-157">When lighting is enabled, light sources that are enabled contribute to the lighting calculation.</span></span> <span data-ttu-id="71987-158">La fuente de luz *i* está habilitada y deshabilitada mediante **glEnable** y **glDisable** con el argumento GL \_ Light *i*.</span><span class="sxs-lookup"><span data-stu-id="71987-158">Light source *i* is enabled and disabled using **glEnable** and **glDisable** with argument GL\_LIGHT *i*.</span></span>

<span data-ttu-id="71987-159">Siempre es el caso de GL \_ Light *i* = GL \_ LIGHT0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="71987-159">It is always the case that GL\_LIGHT *i* = GL\_LIGHT0 + *i*.</span></span>

<span data-ttu-id="71987-160">Las siguientes funciones recuperan información relacionada con la función **glLighti** :</span><span class="sxs-lookup"><span data-stu-id="71987-160">The following functions retrieve information related to the **glLighti** function:</span></span>

[<span data-ttu-id="71987-161">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="71987-161">**glGetLight**</span></span>](glgetlight.md)

<span data-ttu-id="71987-162">[**glIsEnabled**](glisenabled.md) con iluminación de GL de argumento \_</span><span class="sxs-lookup"><span data-stu-id="71987-162">[**glIsEnabled**](glisenabled.md) with argument GL\_LIGHTING</span></span>

## <a name="requirements"></a><span data-ttu-id="71987-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71987-163">Requirements</span></span>



| <span data-ttu-id="71987-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="71987-164">Requirement</span></span> | <span data-ttu-id="71987-165">Value</span><span class="sxs-lookup"><span data-stu-id="71987-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71987-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71987-166">Minimum supported client</span></span><br/> | <span data-ttu-id="71987-167">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71987-167">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="71987-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71987-168">Minimum supported server</span></span><br/> | <span data-ttu-id="71987-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71987-169">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71987-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71987-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="71987-171"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="71987-171"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="71987-172">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71987-172">Library</span></span><br/>                  | <dl> <span data-ttu-id="71987-173"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71987-173"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="71987-174">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71987-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71987-175"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71987-175"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71987-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="71987-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71987-177">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="71987-177">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="71987-178">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="71987-178">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="71987-179">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="71987-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="71987-180">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="71987-180">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="71987-181">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="71987-181">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





