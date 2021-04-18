---
title: función glVertexPointer (GL. h)
description: La función glVertexPointer define una matriz de datos de vértice.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- glVertexPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492119"
---
# <a name="glvertexpointer-function"></a><span data-ttu-id="1efe0-104">glVertexPointer función)</span><span class="sxs-lookup"><span data-stu-id="1efe0-104">glVertexPointer function</span></span>

<span data-ttu-id="1efe0-105">La función **glVertexPointer** define una matriz de datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="1efe0-105">The **glVertexPointer** function defines an array of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1efe0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1efe0-106">Syntax</span></span>


```C++
void WINAPI glVertexPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="1efe0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1efe0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1efe0-108">*size*</span><span class="sxs-lookup"><span data-stu-id="1efe0-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="1efe0-109">Número de coordenadas por vértice.</span><span class="sxs-lookup"><span data-stu-id="1efe0-109">The number of coordinates per vertex.</span></span> <span data-ttu-id="1efe0-110">El valor de *size* debe ser 2, 3 ó 4.</span><span class="sxs-lookup"><span data-stu-id="1efe0-110">The value of *size* must be 2, 3, or 4.</span></span>

</dd> <dt>

<span data-ttu-id="1efe0-111">*type*</span><span class="sxs-lookup"><span data-stu-id="1efe0-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1efe0-112">El tipo de datos de cada coordenada de la matriz mediante las siguientes constantes simbólicas: GL \_ Short, GL \_ int, GL \_ float y GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="1efe0-112">The data type of each coordinate in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="1efe0-113">*STRI*</span><span class="sxs-lookup"><span data-stu-id="1efe0-113">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="1efe0-114">Desplazamiento de bytes entre los vértices consecutivos.</span><span class="sxs-lookup"><span data-stu-id="1efe0-114">The byte offset between consecutive vertices.</span></span> <span data-ttu-id="1efe0-115">Cuando *STRIDE* es cero, los vértices están estrechamente empaquetados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="1efe0-115">When *stride* is zero, the vertices are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="1efe0-116">*puntero*</span><span class="sxs-lookup"><span data-stu-id="1efe0-116">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1efe0-117">Puntero a la primera coordenada del primer vértice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="1efe0-117">A pointer to the first coordinate of the first vertex in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1efe0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1efe0-118">Return value</span></span>

<span data-ttu-id="1efe0-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1efe0-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1efe0-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1efe0-120">Error codes</span></span>

<span data-ttu-id="1efe0-121">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1efe0-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1efe0-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="1efe0-122">Name</span></span>                                                                                              | <span data-ttu-id="1efe0-123">Significado</span><span class="sxs-lookup"><span data-stu-id="1efe0-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="1efe0-124"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1efe0-124"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1efe0-125">*el tamaño* no era 2, 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="1efe0-125">*size* was not 2, 3, or 4.</span></span> <br/>        |
| <dl> <span data-ttu-id="1efe0-126"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1efe0-126"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="1efe0-127">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="1efe0-127">*type* was not an accepted value.</span></span><br/>  |
| <dl> <span data-ttu-id="1efe0-128"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1efe0-128"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1efe0-129">*STRIDE* o *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="1efe0-129">*stride* or *count* was negative.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="1efe0-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1efe0-130">Remarks</span></span>

<span data-ttu-id="1efe0-131">La función **glVertexPointer** especifica la ubicación y los datos de una matriz de coordenadas de vértice que se van a usar en la representación.</span><span class="sxs-lookup"><span data-stu-id="1efe0-131">The **glVertexPointer** function specifies the location and data of an array of vertex coordinates to use when rendering.</span></span> <span data-ttu-id="1efe0-132">El parámetro *size* especifica el número de coordenadas por vértice.</span><span class="sxs-lookup"><span data-stu-id="1efe0-132">The *size* parameter specifies the number of coordinates per vertex.</span></span> <span data-ttu-id="1efe0-133">El parámetro de *tipo* especifica el tipo de datos de cada coordenada del vértice.</span><span class="sxs-lookup"><span data-stu-id="1efe0-133">The *type* parameter specifies the data type of each vertex coordinate.</span></span> <span data-ttu-id="1efe0-134">El parámetro *STRIDE* determina el desplazamiento de bytes de un vértice al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="1efe0-134">The *stride* parameter determines the byte offset from one vertex to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="1efe0-135">En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes (vea [**glInterleavedArrays**](glinterleavedarrays.md)).</span><span class="sxs-lookup"><span data-stu-id="1efe0-135">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays (see [**glInterleavedArrays**](glinterleavedarrays.md)).</span></span>

<span data-ttu-id="1efe0-136">Una matriz de vértices se habilita al especificar la \_ \_ constante de matriz de vértices de GL con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="1efe0-136">A vertex array is enabled when you specify the GL\_VERTEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="1efe0-137">Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)y [**glArrayElement**](glarrayelement.md) usan la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="1efe0-137">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md), and [**glArrayElement**](glarrayelement.md) use the vertex array.</span></span> <span data-ttu-id="1efe0-138">De forma predeterminada, la matriz de vértices está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="1efe0-138">By default, the vertex array is disabled.</span></span>

<span data-ttu-id="1efe0-139">No se puede incluir **glVertexPointer** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="1efe0-139">You cannot include **glVertexPointer** in display lists.</span></span>

<span data-ttu-id="1efe0-140">Cuando se especifica una matriz de vértices mediante **glVertexPointer**, los valores de todos los parámetros de matriz de vértices de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="1efe0-140">When you specify a vertex array using **glVertexPointer**, the values of all the function's vertex array parameters are saved in a client-side state, and static array elements can be cached.</span></span> <span data-ttu-id="1efe0-141">Dado que los parámetros de la matriz de vértices son de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="1efe0-141">Because the vertex array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="1efe0-142">Aunque no se genera ningún error si se llama a **glVertexPointer** en pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) , los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1efe0-142">Although no error is generated if you call **glVertexPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="1efe0-143">Las siguientes funciones recuperan información relacionada con **glVertexPointer**:</span><span class="sxs-lookup"><span data-stu-id="1efe0-143">The following functions retrieve information related to **glVertexPointer**:</span></span>

<span data-ttu-id="1efe0-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ tamaño de matriz de vértices de GL \_</span><span class="sxs-lookup"><span data-stu-id="1efe0-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VERTEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="1efe0-145">**glGet** con argumento \_ intervalo de matriz de VÉRTICEs de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1efe0-145">**glGet** with argument GL\_VERTEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="1efe0-146">**glGet** con el argumento \_ \_ Count de matriz de vértices de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="1efe0-146">**glGet** with argument GL\_VERTEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="1efe0-147">**glGet** con argumento \_ tipo de matriz de VÉRTICEs de contabilidad \_ \_</span><span class="sxs-lookup"><span data-stu-id="1efe0-147">**glGet** with argument GL\_VERTEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="1efe0-148">[**glGetPointerv**](glgetpointerv.md) con el argumento de \_ matriz de vértices de contabilidad de argumentos \_ \_</span><span class="sxs-lookup"><span data-stu-id="1efe0-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_VERTEX\_ARRAY\_POINTER</span></span>

<span data-ttu-id="1efe0-149">[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz de VÉRTICEs de GL \_</span><span class="sxs-lookup"><span data-stu-id="1efe0-149">[**glIsEnabled**](glisenabled.md) with argument GL\_VERTEX\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="1efe0-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1efe0-150">Requirements</span></span>



| <span data-ttu-id="1efe0-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1efe0-151">Requirement</span></span> | <span data-ttu-id="1efe0-152">Value</span><span class="sxs-lookup"><span data-stu-id="1efe0-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1efe0-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1efe0-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1efe0-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1efe0-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1efe0-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1efe0-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1efe0-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1efe0-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1efe0-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1efe0-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="1efe0-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1efe0-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1efe0-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1efe0-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="1efe0-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1efe0-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1efe0-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1efe0-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1efe0-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1efe0-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1efe0-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="1efe0-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efe0-164">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="1efe0-164">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="1efe0-165">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="1efe0-165">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="1efe0-166">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="1efe0-166">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="1efe0-167">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="1efe0-167">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="1efe0-168">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="1efe0-168">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="1efe0-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="1efe0-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="1efe0-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="1efe0-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="1efe0-171">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="1efe0-171">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="1efe0-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1efe0-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1efe0-173">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="1efe0-173">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="1efe0-174">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="1efe0-174">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> </dl>

 

 





