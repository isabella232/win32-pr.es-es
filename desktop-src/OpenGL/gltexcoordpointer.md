---
title: función glTexCoordPointer (GL. h)
description: La función glTexCoordPointer define una matriz de coordenadas de textura.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- glTexCoordPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686248"
---
# <a name="gltexcoordpointer-function"></a><span data-ttu-id="73ace-104">glTexCoordPointer función)</span><span class="sxs-lookup"><span data-stu-id="73ace-104">glTexCoordPointer function</span></span>

<span data-ttu-id="73ace-105">La función **glTexCoordPointer** define una matriz de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="73ace-105">The **glTexCoordPointer** function defines an array of texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ace-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73ace-106">Syntax</span></span>


```C++
void WINAPI glTexCoordPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="73ace-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73ace-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ace-108">*size*</span><span class="sxs-lookup"><span data-stu-id="73ace-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="73ace-109">Número de coordenadas por elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="73ace-109">The number of coordinates per array element.</span></span> <span data-ttu-id="73ace-110">El valor de *size* debe ser 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="73ace-110">The value of *size* must be 1, 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="73ace-111">*type*</span><span class="sxs-lookup"><span data-stu-id="73ace-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="73ace-112">El tipo de datos de cada coordenada de textura de la matriz mediante las siguientes constantes simbólicas: **GL \_ Short**, **GL \_ int**, **GL \_ float** y **GL \_ Double**.</span><span class="sxs-lookup"><span data-stu-id="73ace-112">The data type of each texture coordinate in the array using the following symbolic constants: **GL\_SHORT**, **GL\_INT**, **GL\_FLOAT**, and **GL\_DOUBLE**.</span></span>

</dd> <dt>

<span data-ttu-id="73ace-113">*STRI*</span><span class="sxs-lookup"><span data-stu-id="73ace-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="73ace-114">El desplazamiento de bytes entre los elementos de la matriz consecutivos.</span><span class="sxs-lookup"><span data-stu-id="73ace-114">The byte offset between consecutive array elements.</span></span> <span data-ttu-id="73ace-115">Cuando *STRIDE* es cero, los elementos de la matriz están estrechamente empaquetados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="73ace-115">When *stride* is zero, the array elements are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="73ace-116">*puntero*</span><span class="sxs-lookup"><span data-stu-id="73ace-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="73ace-117">Puntero a la primera coordenada del primer elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="73ace-117">A pointer to the first coordinate of the first element in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ace-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73ace-118">Return value</span></span>

<span data-ttu-id="73ace-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="73ace-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73ace-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="73ace-120">Error codes</span></span>

<span data-ttu-id="73ace-121">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="73ace-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="73ace-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="73ace-122">Name</span></span>                                                                                              | <span data-ttu-id="73ace-123">Significado</span><span class="sxs-lookup"><span data-stu-id="73ace-123">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="73ace-124"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="73ace-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="73ace-125">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="73ace-125">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="73ace-126"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="73ace-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="73ace-127">*el tamaño* no era 1, 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="73ace-127">*size* was not 1, 2, 3, or 4.</span></span><br/>     |
| <dl> <span data-ttu-id="73ace-128"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="73ace-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="73ace-129">*STRIDE* es negativo.</span><span class="sxs-lookup"><span data-stu-id="73ace-129">*stride* was negative.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="73ace-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73ace-130">Remarks</span></span>

<span data-ttu-id="73ace-131">La función **glTexCoordPointer** especifica la ubicación y los datos de una matriz de coordenadas de textura que se van a utilizar al representar. El parámetro *size* especifica el número de coordenadas utilizadas para cada elemento de la matriz. El parámetro de *tipo* especifica el tipo de datos de cada coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="73ace-131">The **glTexCoordPointer** function specifies the location and data of an array of texture coordinates to use when rendering.The *size* parameter specifies the number of coordinates used for each element of the array.The *type* parameter specifies the data type of each texture coordinate.</span></span> <span data-ttu-id="73ace-132">El parámetro *STRIDE* determina el desplazamiento de bytes de un elemento de matriz al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="73ace-132">The *stride* parameter determines the byte offset from one array element to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="73ace-133">En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="73ace-133">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="73ace-134">Para obtener más información, vea [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="73ace-134">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span> <span data-ttu-id="73ace-135">Cuando se especifica una matriz de coordenadas de textura, el tamaño, el tipo, el intervalo y el puntero se guardan en el estado del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="73ace-135">When a texture coordinate array is specified, size, type, stride, and pointer are saved client-side state.</span></span>

<span data-ttu-id="73ace-136">Una matriz de coordenadas de textura se habilita al especificar la constante de la **\_ \_ \_ matriz de textura de GL** con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="73ace-136">A texture coordinate array is enabled when you specify the **GL\_TEXTURE\_COORD\_ARRAY** constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="73ace-137">Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)y [**glArrayElement**](glarrayelement.md) usan la matriz de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="73ace-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the texture coordinate array.</span></span> <span data-ttu-id="73ace-138">De forma predeterminada, la matriz de coordenadas de textura está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="73ace-138">By default the texture coordinate array is disabled.</span></span>

<span data-ttu-id="73ace-139">No se puede incluir **glTexCoordPointer** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="73ace-139">You cannot include **glTexCoordPointer** in display lists.</span></span>

<span data-ttu-id="73ace-140">Cuando se especifica una matriz de coordenadas de textura mediante **glTexCoordPointer**, los valores de todos los parámetros de matriz de coordenadas de textura de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="73ace-140">When you specify a texture coordinate array using **glTexCoordPointer**, the values of all the function's texture coordinate array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="73ace-141">Dado que los parámetros de la matriz de coordenadas de textura son de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="73ace-141">Because the texture coordinate array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="73ace-142">Aunque no se genera ningún error cuando se llama a **glTexCoordPointer** en pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) , los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="73ace-142">Although no error is generated when you call **glTexCoordPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="73ace-143">Las siguientes funciones recuperan información relacionada con **glTexCoordPointer**:</span><span class="sxs-lookup"><span data-stu-id="73ace-143">The following functions retrieve information related to **glTexCoordPointer**:</span></span>

<span data-ttu-id="73ace-144">[**glIsEnabled**](glisenabled.md) con la **\_ matriz de \_ coordenadas \_ de textura de GL** de argumento</span><span class="sxs-lookup"><span data-stu-id="73ace-144">[**glIsEnabled**](glisenabled.md) with argument **GL\_TEXTURE\_COORD\_ARRAY**</span></span>

<span data-ttu-id="73ace-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con **el argumento GL Texture de la \_ \_ \_ matriz \_ tamaño** de la matriz</span><span class="sxs-lookup"><span data-stu-id="73ace-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_SIZE**</span></span>

<span data-ttu-id="73ace-146">**glGet** con argumento **GL de la \_ \_ \_ matriz \_ coordenadas de textura de contabilidad**</span><span class="sxs-lookup"><span data-stu-id="73ace-146">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_STRIDE**</span></span>

<span data-ttu-id="73ace-147">**glGet** con el **argumento \_ \_ número de \_ matriz \_ de textura de GL de contabilidad**</span><span class="sxs-lookup"><span data-stu-id="73ace-147">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_COUNT**</span></span>

<span data-ttu-id="73ace-148">**glGet** con el **argumento \_ GL \_ Texture \_ \_ tipo de matriz**</span><span class="sxs-lookup"><span data-stu-id="73ace-148">**glGet** with argument **GL\_TEXTURE\_COORD\_ARRAY\_TYPE**</span></span>

<span data-ttu-id="73ace-149">[**glGetPointerv**](glgetpointerv.md) con el argumento GL de la **\_ \_ \_ \_ matriz coordenadas de textura de contabilidad**</span><span class="sxs-lookup"><span data-stu-id="73ace-149">[**glGetPointerv**](glgetpointerv.md) with argument **GL\_TEXTURE\_COORD\_ARRAY\_POINTER**</span></span>

## <a name="requirements"></a><span data-ttu-id="73ace-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73ace-150">Requirements</span></span>



| <span data-ttu-id="73ace-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ace-151">Requirement</span></span> | <span data-ttu-id="73ace-152">Value</span><span class="sxs-lookup"><span data-stu-id="73ace-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ace-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73ace-153">Minimum supported client</span></span><br/> | <span data-ttu-id="73ace-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="73ace-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73ace-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73ace-155">Minimum supported server</span></span><br/> | <span data-ttu-id="73ace-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="73ace-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73ace-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73ace-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="73ace-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ace-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="73ace-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73ace-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="73ace-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73ace-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="73ace-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73ace-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ace-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ace-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ace-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="73ace-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ace-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="73ace-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="73ace-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="73ace-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="73ace-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="73ace-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="73ace-167">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="73ace-167">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="73ace-168">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="73ace-168">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="73ace-169">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="73ace-169">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="73ace-170">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="73ace-170">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="73ace-171">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="73ace-171">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="73ace-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="73ace-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="73ace-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="73ace-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="73ace-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="73ace-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="73ace-175">**glPopClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="73ace-175">**glPopClientAttrib**</span></span>](glpopclientattrib.md)
</dt> <dt>

[<span data-ttu-id="73ace-176">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="73ace-176">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="73ace-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="73ace-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="73ace-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="73ace-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





