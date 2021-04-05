---
title: función glCallLists (GL. h)
description: La función glCallLists ejecuta una lista de listas de presentación.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- glCallLists (función) OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996530"
---
# <a name="glcalllists-function"></a><span data-ttu-id="b3342-104">glCallLists función)</span><span class="sxs-lookup"><span data-stu-id="b3342-104">glCallLists function</span></span>

<span data-ttu-id="b3342-105">La función **glCallLists** ejecuta una lista de listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="b3342-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3342-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3342-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="b3342-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3342-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3342-108">*n*</span><span class="sxs-lookup"><span data-stu-id="b3342-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="b3342-109">El número de listas de presentación que se van a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="b3342-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="b3342-110">*type*</span><span class="sxs-lookup"><span data-stu-id="b3342-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="b3342-111">Tipo de valores de *las listas*.</span><span class="sxs-lookup"><span data-stu-id="b3342-111">The type of values in *lists*.</span></span> <span data-ttu-id="b3342-112">Se aceptan las siguientes constantes simbólicas.</span><span class="sxs-lookup"><span data-stu-id="b3342-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="b3342-113">Value</span><span class="sxs-lookup"><span data-stu-id="b3342-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="b3342-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b3342-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="b3342-115"><dt>**BYTE de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="b3342-116">El parámetro *lists* se trata como una matriz de bytes con signo, cada uno en el intervalo de-128 a 127.</span><span class="sxs-lookup"><span data-stu-id="b3342-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="b3342-117"><dt>**\_byte sin signo de \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="b3342-118">El parámetro *lists* se trata como una matriz de bytes sin signo, cada uno en el intervalo comprendido entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="b3342-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="b3342-119"><dt>**CONTABILIDAD \_ breve**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="b3342-120">El parámetro *lists* se trata como una matriz de enteros de 2 bytes con signo, cada uno en el intervalo de-32768 a 32767.</span><span class="sxs-lookup"><span data-stu-id="b3342-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="b3342-121"><dt>**libro de contabilidad \_ corto sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="b3342-122">El parámetro *lists* se trata como una matriz de enteros de 2 bytes sin signo, cada uno en el intervalo comprendido entre 0 y 65535.</span><span class="sxs-lookup"><span data-stu-id="b3342-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="b3342-123"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="b3342-124">El parámetro *lists* se trata como una matriz de enteros de 4 bytes con signo.</span><span class="sxs-lookup"><span data-stu-id="b3342-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="b3342-125"><dt>**libro de contabilidad \_ sin signo \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="b3342-126">El parámetro *lists* se trata como una matriz de enteros de 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="b3342-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="b3342-127"><dt>**valor \_ float de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="b3342-128">El parámetro *lists* se trata como una matriz de valores de punto flotante de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="b3342-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="b3342-129"><dt>**GL \_ 2 \_ bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="b3342-130">El parámetro *lists* se trata como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="b3342-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="b3342-131">Cada par de bytes especifica un nombre de lista de presentación único.</span><span class="sxs-lookup"><span data-stu-id="b3342-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="b3342-132">El valor del par se calcula como 256 veces el valor sin signo del primer byte más el valor sin signo del segundo byte.</span><span class="sxs-lookup"><span data-stu-id="b3342-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="b3342-133"><dt>**GL \_ 3 \_ bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="b3342-134">El parámetro *lists* se trata como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="b3342-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="b3342-135">Cada triple de bytes especifica un nombre de lista de presentación único.</span><span class="sxs-lookup"><span data-stu-id="b3342-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="b3342-136">El valor del tripledo se calcula como 65536 veces el valor sin signo del primer byte, más 256 veces el valor sin signo del segundo byte, más el valor sin signo del tercer byte.</span><span class="sxs-lookup"><span data-stu-id="b3342-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="b3342-137"><dt>**CONT. \_ 4 \_ bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="b3342-138">El parámetro *lists* se trata como una matriz de bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="b3342-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="b3342-139">Cada cuádruple de bytes especifica un nombre de lista de presentación único.</span><span class="sxs-lookup"><span data-stu-id="b3342-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="b3342-140">El valor de quadruplet se calcula como 16777216 veces el valor sin signo del primer byte, más 65536 veces el valor sin signo del segundo byte, más 256 veces el valor sin signo del tercer byte, más el valor sin signo del cuarto byte, más el valor sin signo.</span><span class="sxs-lookup"><span data-stu-id="b3342-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b3342-141">*Coge*</span><span class="sxs-lookup"><span data-stu-id="b3342-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="b3342-142">Dirección de una matriz de desplazamientos de nombre de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="b3342-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="b3342-143">El tipo de puntero es void porque los desplazamientos pueden ser bytes, cortos, ints o Float, dependiendo del valor de *tipo*.</span><span class="sxs-lookup"><span data-stu-id="b3342-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3342-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3342-144">Return value</span></span>

<span data-ttu-id="b3342-145">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b3342-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3342-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3342-146">Remarks</span></span>

<span data-ttu-id="b3342-147">La función **glCallLists** hace que cada lista de visualización de la lista de nombres pasados como *listas* se ejecute.</span><span class="sxs-lookup"><span data-stu-id="b3342-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="b3342-148">Como resultado, las funciones guardadas en cada lista de visualización se ejecutan en orden, como si se hubiesen llamado sin usar una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="b3342-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="b3342-149">Se omiten los nombres de las listas de visualización que no se han definido.</span><span class="sxs-lookup"><span data-stu-id="b3342-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="b3342-150">La función **glCallLists** proporciona un medio eficaz para ejecutar listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="b3342-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="b3342-151">El parámetro *n* especifica el número de listas con distintos formatos de nombre (especificados por el parámetro de *tipo* ) **glCallLists** ejecuta.</span><span class="sxs-lookup"><span data-stu-id="b3342-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="b3342-152">La lista de nombres de lista de visualización no termina en NULL.</span><span class="sxs-lookup"><span data-stu-id="b3342-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="b3342-153">En su lugar, *n* especifica el número de nombres que se tomarán de *las listas*.</span><span class="sxs-lookup"><span data-stu-id="b3342-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="b3342-154">La función [**glListBase**](gllistbase.md) hace que un nivel adicional de direccionamiento indirecto esté disponible.</span><span class="sxs-lookup"><span data-stu-id="b3342-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="b3342-155">La función **glListBase** especifica un desplazamiento sin signo que se agrega a cada nombre de la lista de visualización especificado en *las listas* antes de que se ejecute la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="b3342-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="b3342-156">La función **glCallLists** puede aparecer dentro de una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="b3342-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="b3342-157">Para evitar la posibilidad de que se produzca una recursividad infinita como resultado de la llamada a otras listas, se coloca un límite en el nivel de anidamiento de las listas de visualización durante la ejecución de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="b3342-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="b3342-158">Este límite debe ser al menos 64 y depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="b3342-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="b3342-159">El estado de OpenGL no se guarda y se restaura a través de una llamada a **glCallLists**.</span><span class="sxs-lookup"><span data-stu-id="b3342-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="b3342-160">Por lo tanto, los cambios realizados en el estado de OpenGL durante la ejecución de las listas de visualización permanecen una vez completada la ejecución.</span><span class="sxs-lookup"><span data-stu-id="b3342-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="b3342-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)y [**glPopMatrix**](glpopmatrix.md) para conservar el estado de OpenGL en las llamadas a **glCallLists** .</span><span class="sxs-lookup"><span data-stu-id="b3342-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="b3342-162">Puede ejecutar listas de visualización entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md), siempre que la lista de visualización incluya solo las funciones que se permiten en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="b3342-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="b3342-163">Las siguientes funciones recuperan información relacionada con la función **glCallLists** :</span><span class="sxs-lookup"><span data-stu-id="b3342-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="b3342-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento base de la lista de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="b3342-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="b3342-165">**glGet** con el argumento \_ \_ anidamiento de lista Max de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="b3342-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="b3342-166">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="b3342-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="b3342-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3342-167">Requirements</span></span>



| <span data-ttu-id="b3342-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3342-168">Requirement</span></span> | <span data-ttu-id="b3342-169">Value</span><span class="sxs-lookup"><span data-stu-id="b3342-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3342-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3342-170">Minimum supported client</span></span><br/> | <span data-ttu-id="b3342-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b3342-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3342-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3342-172">Minimum supported server</span></span><br/> | <span data-ttu-id="b3342-173">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b3342-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3342-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3342-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3342-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3342-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3342-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3342-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3342-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3342-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3342-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3342-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3342-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3342-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3342-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3342-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3342-182">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b3342-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b3342-183">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="b3342-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="b3342-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="b3342-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b3342-185">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="b3342-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="b3342-186">**glGet**</span><span class="sxs-lookup"><span data-stu-id="b3342-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="b3342-187">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="b3342-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="b3342-188">**glListBase**</span><span class="sxs-lookup"><span data-stu-id="b3342-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="b3342-189">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="b3342-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="b3342-190">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="b3342-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="b3342-191">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="b3342-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="b3342-192">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="b3342-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="b3342-193">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="b3342-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





