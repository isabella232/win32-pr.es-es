---
title: Función glFogi (Gl.h)
description: La función glFogi especifica los parámetros de niebla.
ms.assetid: c2ffb41d-3d97-4b72-b16d-cfbffa1179d1
keywords:
- glFogi (función) OpenGL
topic_type:
- apiref
api_name:
- glFogi
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc718a007035204f6e984eea87f1e21ba09ac8f0
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "103913961"
---
# <a name="glfogi-function"></a><span data-ttu-id="0df11-104">glFogi función)</span><span class="sxs-lookup"><span data-stu-id="0df11-104">glFogi function</span></span>

<span data-ttu-id="0df11-105">La función **glFogi** especifica los parámetros de niebla.</span><span class="sxs-lookup"><span data-stu-id="0df11-105">The **glFogi** function specifies fog parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df11-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0df11-106">Syntax</span></span>


```C++
void WINAPI glFogi(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="0df11-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0df11-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df11-108">*PName*</span><span class="sxs-lookup"><span data-stu-id="0df11-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="0df11-109">Especifica un parámetro de niebla de un solo valor.</span><span class="sxs-lookup"><span data-stu-id="0df11-109">Specifies a single-valued fog parameter.</span></span>

<span data-ttu-id="0df11-110">Acepta uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0df11-110">Accepts one of the following values.</span></span>



| <span data-ttu-id="0df11-111">Value</span><span class="sxs-lookup"><span data-stu-id="0df11-111">Value</span></span>                                                                                                                                                             | <span data-ttu-id="0df11-112">Significado</span><span class="sxs-lookup"><span data-stu-id="0df11-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <span data-ttu-id="0df11-113"><dt>**\_modo de niebla de contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-113"><dt>**GL\_FOG\_MODE**</dt></span></span> </dl>          | <span data-ttu-id="0df11-114">El parámetro *params* es un valor entero único que especifica la ecuación que se va a utilizar para calcular el factor de mezcla de niebla, *f*.</span><span class="sxs-lookup"><span data-stu-id="0df11-114">The *params* parameter is a single integer value that specifies the equation to be used to compute the fog blend factor, *f*.</span></span> <span data-ttu-id="0df11-115">Se aceptan tres constantes simbólicas: GL \_ lineal, GL \_ EXP y GL \_ EXP2.</span><span class="sxs-lookup"><span data-stu-id="0df11-115">Three symbolic constants are accepted: GL\_LINEAR, GL\_EXP, and GL\_EXP2.</span></span> <span data-ttu-id="0df11-116">Las ecuaciones correspondientes a estas constantes simbólicas se definen en la sección Comentarios siguiente.</span><span class="sxs-lookup"><span data-stu-id="0df11-116">The equations corresponding to these symbolic constants are defined in the following Remarks section.</span></span> <span data-ttu-id="0df11-117">El modo de niebla predeterminado es GL \_ exp.</span><span class="sxs-lookup"><span data-stu-id="0df11-117">The default fog mode is GL\_EXP.</span></span><br/> |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <span data-ttu-id="0df11-118"><dt>**\_densidad de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-118"><dt>**GL\_FOG\_DENSITY**</dt></span></span> </dl> | <span data-ttu-id="0df11-119">El parámetro *params* es un valor entero único que especifica la *densidad*, la densidad de niebla utilizada en ambas ecuaciones de niebla exponencial.</span><span class="sxs-lookup"><span data-stu-id="0df11-119">The *params* parameter is a single integer value that specifies *density*, the fog density used in both exponential fog equations.</span></span> <span data-ttu-id="0df11-120">Solo se aceptan las densidades no negativas.</span><span class="sxs-lookup"><span data-stu-id="0df11-120">Only nonnegative densities are accepted.</span></span> <span data-ttu-id="0df11-121">La densidad de niebla predeterminada es 1,0.</span><span class="sxs-lookup"><span data-stu-id="0df11-121">The default fog density is 1.0.</span></span><br/>                                                                                                                                    |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <span data-ttu-id="0df11-122"><dt>**\_Inicio de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-122"><dt>**GL\_FOG\_START**</dt></span></span> </dl>       | <span data-ttu-id="0df11-123">El parámetro *params* es un valor entero único que especifica *Start*, la distancia cercana utilizada en la ecuación de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="0df11-123">The *params* parameter is a single integer value that specifies *start*, the near distance used in the linear fog equation.</span></span> <span data-ttu-id="0df11-124">El valor predeterminado cerca de la distancia es 0,0.</span><span class="sxs-lookup"><span data-stu-id="0df11-124">The default near distance is 0.0.</span></span><br/>                                                                                                                                                                                  |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <span data-ttu-id="0df11-125"><dt>**finalización de la niebla de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-125"><dt>**GL\_FOG\_END**</dt></span></span> </dl>             | <span data-ttu-id="0df11-126">El parámetro *params* es un valor entero único que especifica *End*, la distancia lejana utilizada en la ecuación de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="0df11-126">The *params* parameter is a single integer value that specifies *end*, the far distance used in the linear fog equation.</span></span> <span data-ttu-id="0df11-127">La distancia predeterminada es 1,0.</span><span class="sxs-lookup"><span data-stu-id="0df11-127">The default far distance is 1.0.</span></span><br/>                                                                                                                                                                                      |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <span data-ttu-id="0df11-128"><dt>**\_Índice de niebla de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-128"><dt>**GL\_FOG\_INDEX**</dt></span></span> </dl>       | <span data-ttu-id="0df11-129">El parámetro *params* es un valor entero único que especifica *i*<sub>f</sub> , el índice de color de niebla.</span><span class="sxs-lookup"><span data-stu-id="0df11-129">The *params* parameter is a single integer value that specifies *i*<sub>f</sub> , the fog color index.</span></span> <span data-ttu-id="0df11-130">El índice de niebla predeterminado es 0,0.</span><span class="sxs-lookup"><span data-stu-id="0df11-130">The default fog index is 0.0.</span></span><br/>                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="0df11-131">*param*</span><span class="sxs-lookup"><span data-stu-id="0df11-131">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="0df11-132">Especifica el valor en el que se establecerá *PName* .</span><span class="sxs-lookup"><span data-stu-id="0df11-132">Specifies the value that *pname* will be set to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0df11-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0df11-133">Return value</span></span>

<span data-ttu-id="0df11-134">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0df11-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0df11-135">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0df11-135">Error codes</span></span>

<span data-ttu-id="0df11-136">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="0df11-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0df11-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="0df11-137">Name</span></span>                                                                                                  | <span data-ttu-id="0df11-138">Significado</span><span class="sxs-lookup"><span data-stu-id="0df11-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0df11-139"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0df11-140">*PName* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="0df11-140">*pname* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="0df11-141"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0df11-142">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0df11-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0df11-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0df11-143">Remarks</span></span>

<span data-ttu-id="0df11-144">Para habilitar y deshabilitar la niebla con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md), use el argumento niebla de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="0df11-144">You enable and disable fog with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), using the argument GL\_FOG.</span></span> <span data-ttu-id="0df11-145">Mientras está habilitada, la niebla afecta a la geometría rasterizada, mapas de bits y bloques de píxeles, pero no operaciones de borrado de búfer.</span><span class="sxs-lookup"><span data-stu-id="0df11-145">While enabled, fog affects rasterized geometry, bitmaps, and pixel blocks, but not buffer-clear operations.</span></span>

<span data-ttu-id="0df11-146">La función **glFogi** asigna el valor o los *valores de los* parámetros al parámetro de niebla especificado por *PName*.</span><span class="sxs-lookup"><span data-stu-id="0df11-146">The **glFogi** function assigns the value or values in *params* to the fog parameter specified by *pname*.</span></span>

<span data-ttu-id="0df11-147">La niebla combina un color de niebla con el color de posttexturización de cada fragmento de píxel rasterizado mediante un factor de mezcla *f*.</span><span class="sxs-lookup"><span data-stu-id="0df11-147">Fog blends a fog color with each rasterized pixel fragment's posttexturing color using a blending factor *f*.</span></span> <span data-ttu-id="0df11-148">Factor *f* se calcula de una de estas tres maneras, según el modo de niebla.</span><span class="sxs-lookup"><span data-stu-id="0df11-148">Factor *f* is computed in one of three ways, depending on the fog mode.</span></span> <span data-ttu-id="0df11-149">Deje que *z* sea la distancia en coordenadas de ojo desde el origen al fragmento que se va a la luneta térmica.</span><span class="sxs-lookup"><span data-stu-id="0df11-149">Let *z* be the distance in eye coordinates from the origin to the fragment being fogged.</span></span> <span data-ttu-id="0df11-150">La ecuación para la \_ niebla lineal de GL es:</span><span class="sxs-lookup"><span data-stu-id="0df11-150">The equation for GL\_LINEAR fog is:</span></span>

![Ecuación que muestra el valor de la niebla de GL_LINEAR.](images/fog01.png)

<span data-ttu-id="0df11-152">La ecuación para la niebla de contabilidad de contabilidad \_ es:</span><span class="sxs-lookup"><span data-stu-id="0df11-152">The equation for GL\_EXP fog is:</span></span>

![Ecuación que muestra el valor del factor de mezcla en el modo de niebla de GL_EXP.](images/fog02.png)

<span data-ttu-id="0df11-154">La ecuación para la \_ niebla de EXP2 de GL es:</span><span class="sxs-lookup"><span data-stu-id="0df11-154">The equation for GL\_EXP2 fog is:</span></span>

![Ecuación que muestra el valor del factor de mezcla en el modo de niebla de GL_EXP2.](images/fog03.png)

<span data-ttu-id="0df11-156">Independientemente del modo de niebla, *f* se fija en el intervalo de \[ 0 a 1 \] después de su cálculo.</span><span class="sxs-lookup"><span data-stu-id="0df11-156">Regardless of the fog mode, *f* is clamped to the range \[0,1\] after it is computed.</span></span> <span data-ttu-id="0df11-157">A continuación, si OpenGL está en modo de color RGBA, el color *C*<sub>r</sub> del fragmento se sustituye por</span><span class="sxs-lookup"><span data-stu-id="0df11-157">Then, if OpenGL is in RGBA color mode, the fragment's color *C*<sub>r</sub> is replaced by</span></span>

![Ecuación que muestra el color del fragmento de la luneta térmica como función del factor de fusión y del color de la niebla.](images/fog04.png)

<span data-ttu-id="0df11-159">En el modo de índice de color, el índice de color del fragmento *i*<sub>r</sub> se sustituye por</span><span class="sxs-lookup"><span data-stu-id="0df11-159">In color-index mode, the fragment's color index *i*<sub>r</sub> is replaced by</span></span>

![Ecuación que muestra el índice de color del fragmento de la luneta térmica como una función de factor de fusión y color indexado.](images/fog05.png)

<span data-ttu-id="0df11-161">Las siguientes funciones recuperan información relacionada con las funciones de **glFog** :</span><span class="sxs-lookup"><span data-stu-id="0df11-161">The following functions retrieve information related to the **glFog** functions:</span></span>

<span data-ttu-id="0df11-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento del \_ color de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="0df11-162">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FOG\_COLOR</span></span>

<span data-ttu-id="0df11-163">**glGet** con el argumento \_ Índice de niebla de GL \_</span><span class="sxs-lookup"><span data-stu-id="0df11-163">**glGet** with argument GL\_FOG\_INDEX</span></span>

<span data-ttu-id="0df11-164">**glGet** con el argumento \_ densidad de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="0df11-164">**glGet** with argument GL\_FOG\_DENSITY</span></span>

<span data-ttu-id="0df11-165">**glGet** con el argumento \_ Inicio de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="0df11-165">**glGet** with argument GL\_FOG\_START</span></span>

<span data-ttu-id="0df11-166">**glGet** con el argumento \_ final de niebla de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="0df11-166">**glGet** with argument GL\_FOG\_END</span></span>

<span data-ttu-id="0df11-167">**glGet** con el \_ modo de niebla de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="0df11-167">**glGet** with argument GL\_FOG\_MODE</span></span>

<span data-ttu-id="0df11-168">[**glIsEnabled**](glisenabled.md) con niebla de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="0df11-168">[**glIsEnabled**](glisenabled.md) with argument GL\_FOG</span></span>

## <a name="requirements"></a><span data-ttu-id="0df11-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0df11-169">Requirements</span></span>



| <span data-ttu-id="0df11-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="0df11-170">Requirement</span></span> | <span data-ttu-id="0df11-171">Value</span><span class="sxs-lookup"><span data-stu-id="0df11-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0df11-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0df11-172">Minimum supported client</span></span><br/> | <span data-ttu-id="0df11-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0df11-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0df11-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0df11-174">Minimum supported server</span></span><br/> | <span data-ttu-id="0df11-175">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0df11-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0df11-176">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0df11-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df11-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0df11-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0df11-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="0df11-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0df11-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0df11-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df11-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df11-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0df11-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="0df11-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0df11-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0df11-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0df11-184">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="0df11-184">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="0df11-185">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="0df11-185">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0df11-186">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0df11-186">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0df11-187">**glGet**</span><span class="sxs-lookup"><span data-stu-id="0df11-187">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="0df11-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0df11-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





