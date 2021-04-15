---
title: Función glFogiv (Gl.h)
description: La función glFogiv especifica los parámetros de niebla. | función glFogiv (GL. h)
ms.assetid: 8d920ddc-6155-412d-af10-585932cb149f
keywords:
- glFogiv (función) OpenGL
topic_type:
- apiref
api_name:
- glFogiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fa4fefece05529cf5ff3906f19c5ad6e444249
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547614"
---
# <a name="glfogiv-function"></a><span data-ttu-id="fbc46-105">glFogiv función)</span><span class="sxs-lookup"><span data-stu-id="fbc46-105">glFogiv function</span></span>

<span data-ttu-id="fbc46-106">La función **glFogfv** especifica los parámetros de niebla.</span><span class="sxs-lookup"><span data-stu-id="fbc46-106">The **glFogfv** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbc46-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbc46-107">Syntax</span></span>


```C++
void WINAPI glFogiv(
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="fbc46-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbc46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbc46-109">*PName*</span><span class="sxs-lookup"><span data-stu-id="fbc46-109">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="fbc46-110">Especifica un parámetro de niebla.</span><span class="sxs-lookup"><span data-stu-id="fbc46-110">Specifies a fog parameter.</span></span>

<span data-ttu-id="fbc46-111">Acepta uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fbc46-111">Accepts one of the following values.</span></span>



| <span data-ttu-id="fbc46-112">Value</span><span class="sxs-lookup"><span data-stu-id="fbc46-112">Value</span></span>                                                                                                                                                             | <span data-ttu-id="fbc46-113">Significado</span><span class="sxs-lookup"><span data-stu-id="fbc46-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="fbc46-114"><dt>**\_modo de niebla de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-114"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="fbc46-115">El parámetro *params* es un valor entero único que especifica la ecuación que se va a utilizar para calcular el factor de mezcla de niebla, *f*.</span><span class="sxs-lookup"><span data-stu-id="fbc46-115">The *params* parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="fbc46-116">Se aceptan tres constantes simbólicas: GL \_ lineal, GL \_ EXP y GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="fbc46-116">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="fbc46-117">Las ecuaciones correspondientes a estas constantes simbólicas se definen en la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="fbc46-117">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="fbc46-118">El modo de niebla predeterminado es GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="fbc46-118">The default fog mode is GL\_EXP.</span></span><br/>                                                                                      |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="fbc46-119"><dt>**\_densidad de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-119"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="fbc46-120">El parámetro *params* es un valor entero único que especifica la *densidad*, la densidad de niebla utilizada en ambas ecuaciones de niebla exponencial.</span><span class="sxs-lookup"><span data-stu-id="fbc46-120">The *params* parameter is a single integer value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="fbc46-121">Solo se aceptan las densidades no negativas.</span><span class="sxs-lookup"><span data-stu-id="fbc46-121">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="fbc46-122">La densidad de niebla predeterminada es 1,0.</span><span class="sxs-lookup"><span data-stu-id="fbc46-122">The default fog density is 1.0.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="fbc46-123"><dt>**\_Inicio de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-123"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="fbc46-124">El parámetro *params* es un valor entero único que especifica *Start*, la distancia cercana utilizada en la ecuación de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="fbc46-124">The *params* parameter is a single integer value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="fbc46-125">El valor predeterminado cerca de la distancia es 0,0.</span><span class="sxs-lookup"><span data-stu-id="fbc46-125">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="fbc46-126"><dt>**finalización de la niebla de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-126"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="fbc46-127">El parámetro *params* es un valor entero único que especifica *End*, la distancia lejana utilizada en la ecuación de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="fbc46-127">The *params* parameter is a single integer value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="fbc46-128">La distancia predeterminada es 1,0.</span><span class="sxs-lookup"><span data-stu-id="fbc46-128">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="fbc46-129"><dt>**\_Índice de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-129"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="fbc46-130">El parámetro *params* es un valor entero único que especifica *i*<sub>f</sub> , el índice de color de niebla.</span><span class="sxs-lookup"><span data-stu-id="fbc46-130">The *params* parameter is a single integer value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="fbc46-131">El índice de niebla predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="fbc46-131">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <span data-ttu-id="fbc46-132"><dt>**\_color de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-132"><dt>**GL\_FOG\_COLOR**</dt></span></span> </dl>       | <span data-ttu-id="fbc46-133">El parámetro *params* contiene cuatro valores enteros o de punto flotante que especifican *C*<sub>f</sub> , el color de niebla.</span><span class="sxs-lookup"><span data-stu-id="fbc46-133">The *params* parameter contains four integer or floating-point values that specify *C*<sub>f</sub> , the fog color.</span></span> <span data-ttu-id="fbc46-134">Los valores enteros se asignan linealmente de forma que el valor representable más positivo se asigna a 1,0 y el valor representable más negativo se asigna a-1,0.</span><span class="sxs-lookup"><span data-stu-id="fbc46-134">Integer values are mapped linearly such that the most positive representable value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="fbc46-135">Los valores de punto flotante se asignan directamente.</span><span class="sxs-lookup"><span data-stu-id="fbc46-135">Floating-point values are mapped directly.</span></span> <span data-ttu-id="fbc46-136">Después de la conversión, todos los componentes de color se fijan en el intervalo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fbc46-136">After conversion, all color components are clamped to the range \[0,1\].</span></span> <span data-ttu-id="fbc46-137">El color de niebla predeterminado es (0, 0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="fbc46-137">The default fog color is (0,0,0,0).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fbc46-138">*params*</span><span class="sxs-lookup"><span data-stu-id="fbc46-138">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="fbc46-139">Especifica el valor o los valores que se van a asignar a *PName*.</span><span class="sxs-lookup"><span data-stu-id="fbc46-139">Specifies the value or values to be assigned to *pname*.</span></span> <span data-ttu-id="fbc46-140">El \_ \_ color de niebla de contabilidad requiere una matriz de cuatro valores.</span><span class="sxs-lookup"><span data-stu-id="fbc46-140">GL\_FOG\_COLOR requires an array of four values.</span></span> <span data-ttu-id="fbc46-141">Todos los demás parámetros aceptan una matriz que contiene un solo valor.</span><span class="sxs-lookup"><span data-stu-id="fbc46-141">All other parameters accept an array containing only a single value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbc46-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbc46-142">Return value</span></span>

<span data-ttu-id="fbc46-143">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fbc46-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fbc46-144">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fbc46-144">Error codes</span></span>

<span data-ttu-id="fbc46-145">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="fbc46-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fbc46-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbc46-146">Name</span></span>                                                                                                  | <span data-ttu-id="fbc46-147">Significado</span><span class="sxs-lookup"><span data-stu-id="fbc46-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbc46-148"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fbc46-149">*PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="fbc46-149">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="fbc46-150"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fbc46-151">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fbc46-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fbc46-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbc46-152">Remarks</span></span>

<span data-ttu-id="fbc46-153">Para habilitar y deshabilitar la niebla con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md), use el argumento niebla de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="fbc46-153">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="fbc46-154">Mientras está habilitada, la niebla afecta a la geometría rasterizada, mapas de bits y bloques de píxeles, pero no operaciones de borrado de búfer.</span><span class="sxs-lookup"><span data-stu-id="fbc46-154">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="fbc46-155">La función **glFogiv** asigna el valor o los *valores de los* parámetros al parámetro de niebla especificado por *PName*.</span><span class="sxs-lookup"><span data-stu-id="fbc46-155">The **glFogiv** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="fbc46-156">La niebla combina un color de niebla con el color de posttexturización de cada fragmento de píxel rasterizado mediante un factor de mezcla *f*.</span><span class="sxs-lookup"><span data-stu-id="fbc46-156">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="fbc46-157">Factor *f* se calcula de una de estas tres maneras, según el modo de niebla.</span><span class="sxs-lookup"><span data-stu-id="fbc46-157">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="fbc46-158">Deje que *z* sea la distancia en coordenadas de ojo desde el origen al fragmento que se va a la luneta térmica.</span><span class="sxs-lookup"><span data-stu-id="fbc46-158">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="fbc46-159">La ecuación para la \_ niebla lineal de GL es:</span><span class="sxs-lookup"><span data-stu-id="fbc46-159">The equation for GL\_LINEAR fog is:</span></span>

![Ecuación que muestra el valor del factor de fusión en GL_LINEAR modo de niebla como una función de distancia.](images/fog01.png)

<span data-ttu-id="fbc46-161">La ecuación para la niebla de contabilidad de contabilidad \_ es:</span><span class="sxs-lookup"><span data-stu-id="fbc46-161">The equation for GL\_EXP fog is:</span></span>

![Ecuación que muestra el valor del factor de mezcla en el modo de niebla de GL_EXP.](images/fog02.png)

<span data-ttu-id="fbc46-163">La ecuación para la \_ niebla de EXP2 de GL es:</span><span class="sxs-lookup"><span data-stu-id="fbc46-163">The equation for GL\_EXP2 fog is:</span></span>

![Ecuación que muestra el valor del factor de mezcla en el modo de niebla de GL_EXP2.](images/fog03.png)

<span data-ttu-id="fbc46-165">Independientemente del modo de niebla, *f* se fija en el intervalo de \[ 0 a 1 \] después de su cálculo.</span><span class="sxs-lookup"><span data-stu-id="fbc46-165">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="fbc46-166">A continuación, si OpenGL está en modo de color RGBA, el color *C*<sub>r</sub> del fragmento se sustituye por</span><span class="sxs-lookup"><span data-stu-id="fbc46-166">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Ecuación que muestra el color del fragmento de la luneta térmica como función del factor de fusión y del color de la niebla.](images/fog04.png)

<span data-ttu-id="fbc46-168">En el modo de índice de color, el índice de color del fragmento *i*<sub>r</sub> se sustituye por</span><span class="sxs-lookup"><span data-stu-id="fbc46-168">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Ecuación que muestra el índice de color del fragmento de la luneta térmica como una función de factor de fusión y color indexado.](images/fog05.png)

<span data-ttu-id="fbc46-170">Las siguientes funciones recuperan información relacionada con las funciones de **glFog** :</span><span class="sxs-lookup"><span data-stu-id="fbc46-170">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="fbc46-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento del \_ color de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-171">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="fbc46-172">**glGet** con el argumento \_ Índice de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-172">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="fbc46-173">**glGet** con el argumento \_ densidad de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-173">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="fbc46-174">**glGet** con el argumento \_ Inicio de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-174">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="fbc46-175">**glGet** con el argumento \_ final de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-175">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="fbc46-176">**glGet** con el \_ modo de niebla de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-176">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="fbc46-177">[**glIsEnabled**](glisenabled.md) con niebla de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="fbc46-177">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc46-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbc46-178">Requirements</span></span>



| <span data-ttu-id="fbc46-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbc46-179">Requirement</span></span> | <span data-ttu-id="fbc46-180">Value</span><span class="sxs-lookup"><span data-stu-id="fbc46-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc46-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc46-181">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc46-182">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fbc46-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fbc46-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbc46-183">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc46-184">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fbc46-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fbc46-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbc46-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc46-186"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-186"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fbc46-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbc46-187">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbc46-188"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-188"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fbc46-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbc46-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbc46-190"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbc46-190"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc46-191">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbc46-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc46-192">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fbc46-192">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fbc46-193">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="fbc46-193">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="fbc46-194">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="fbc46-194">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="fbc46-195">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fbc46-195">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fbc46-196">**glGet**</span><span class="sxs-lookup"><span data-stu-id="fbc46-196">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="fbc46-197">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="fbc46-197">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





