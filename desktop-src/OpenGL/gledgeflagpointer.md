---
title: función glEdgeFlagPointer (GL. h)
description: La función glEdgeFlagPointer define una matriz de marcas de borde.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- glEdgeFlagPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802804"
---
# <a name="gledgeflagpointer-function"></a><span data-ttu-id="36058-104">glEdgeFlagPointer función)</span><span class="sxs-lookup"><span data-stu-id="36058-104">glEdgeFlagPointer function</span></span>

<span data-ttu-id="36058-105">La función **glEdgeFlagPointer** define una matriz de marcas de borde.</span><span class="sxs-lookup"><span data-stu-id="36058-105">The **glEdgeFlagPointer** function defines an array of edge flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="36058-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36058-106">Syntax</span></span>


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="36058-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36058-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36058-108">*STRI*</span><span class="sxs-lookup"><span data-stu-id="36058-108">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="36058-109">El desplazamiento de bytes entre las marcas de borde consecutivas.</span><span class="sxs-lookup"><span data-stu-id="36058-109">The byte offset between consecutive edge flags.</span></span> <span data-ttu-id="36058-110">Cuando *STRIDE* es cero, las marcas de borde están estrechamente empaquetadas en la matriz.</span><span class="sxs-lookup"><span data-stu-id="36058-110">When *stride* is zero, the edge flags are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="36058-111">*puntero*</span><span class="sxs-lookup"><span data-stu-id="36058-111">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="36058-112">Puntero a la primera marca de borde de la matriz.</span><span class="sxs-lookup"><span data-stu-id="36058-112">A pointer to the first edge flag in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36058-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36058-113">Return value</span></span>

<span data-ttu-id="36058-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="36058-114">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="36058-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="36058-115">Error codes</span></span>

<span data-ttu-id="36058-116">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="36058-116">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="36058-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="36058-117">Name</span></span>                                                                                             | <span data-ttu-id="36058-118">Significado</span><span class="sxs-lookup"><span data-stu-id="36058-118">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="36058-119"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36058-119"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="36058-120">*STRIDE* o *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="36058-120">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="36058-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36058-121">Remarks</span></span>

<span data-ttu-id="36058-122">La función **glEdgeFlagPointer** especifica la ubicación y los datos de una matriz de marcas de borde booleanos que se van a usar en la representación.</span><span class="sxs-lookup"><span data-stu-id="36058-122">The **glEdgeFlagPointer** function specifies the location and data of an array of Boolean edge flags to use when rendering.</span></span> <span data-ttu-id="36058-123">El parámetro *STRIDE* determina el desplazamiento de bytes de una marca perimetral a la siguiente, que habilita el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="36058-123">The *stride* parameter determines the byte offset from one edge flag to the next, which enables the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="36058-124">En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="36058-124">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span>

<span data-ttu-id="36058-125">Una matriz de marcas de borde se habilita al especificar la constante de la matriz de marca de borde de GL \_ \_ \_ con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="36058-125">An edge-flag array is enabled when you specify the GL\_EDGE\_FLAG\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="36058-126">Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md) o [**glArrayElement**](glarrayelement.md) usa la matriz de marcas de borde.</span><span class="sxs-lookup"><span data-stu-id="36058-126">When enabled, [**glDrawArrays**](gldrawarrays.md) or [**glArrayElement**](glarrayelement.md) uses the edge-flag array.</span></span> <span data-ttu-id="36058-127">De forma predeterminada, la matriz de marcas de borde está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="36058-127">By default the edge-flag array is disabled.</span></span>

<span data-ttu-id="36058-128">Use **glDrawArrays** para construir una secuencia de primitivas (todo el mismo tipo) a partir de matrices de atributos de vértices y vértices predeterminados.</span><span class="sxs-lookup"><span data-stu-id="36058-128">Use **glDrawArrays** to construct a sequence of primitives (all of the same type) from prespecified vertex and vertex attribute arrays.</span></span> <span data-ttu-id="36058-129">Use **glArrayElement** para especificar primitivos mediante la indexación de vértices y atributos de vértice, y [**glDrawElements**](gldrawelements.md) para construir una secuencia de primitivas mediante la indexación de vértices y atributos de vértice.</span><span class="sxs-lookup"><span data-stu-id="36058-129">Use **glArrayElement** to specify primitives by indexing vertices and vertex attributes, and [**glDrawElements**](gldrawelements.md) to construct a sequence of primitives by indexing vertices and vertex attributes.</span></span>

<span data-ttu-id="36058-130">No se puede incluir **glEdgeFlagPointer** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="36058-130">You cannot include **glEdgeFlagPointer** in display lists.</span></span>

<span data-ttu-id="36058-131">Cuando se especifica una matriz de marcas de borde con **glEdgeFlagPointer**, los valores de todos los parámetros de matriz de marcas de borde de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="36058-131">When you specify an edge-flag array using **glEdgeFlagPointer**, the values of all the function's edge-flag array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="36058-132">Dado que los parámetros de matriz perimetral-Flag están en un estado de cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) no guardan ni restauran sus valores.</span><span class="sxs-lookup"><span data-stu-id="36058-132">Because the edge-flag array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore their values.</span></span>

<span data-ttu-id="36058-133">Aunque llamar a **glEdgeFlagPointer** dentro de un par glend de [**glBegin**](glbegin.md)no / [](glend.md) genera un error, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="36058-133">Although calling **glEdgeFlagPointer** within a [**glBegin**](glbegin.md)/[**glend**](glend.md) pair does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="36058-134">Las siguientes funciones recuperan información relacionada con la función **glEdgeFlagPointer** :</span><span class="sxs-lookup"><span data-stu-id="36058-134">The following functions retrieve information related to the **glEdgeFlagPointer** function:</span></span>

<span data-ttu-id="36058-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ intervalo de \_ matriz de marca de margen de \_ Contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="36058-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="36058-136">**glGet** con argumento \_ \_ \_ recuento de matriz de marcas de margen de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="36058-136">**glGet** with argument GL\_EDGE\_FLAG\_ARRAY\_COUNT</span></span>

<span data-ttu-id="36058-137">[**glGetPointerv**](glgetpointerv.md) con argumento de \_ \_ matriz de marca de borde de \_ contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="36058-137">[**glGetPointerv**](glgetpointerv.md) with argument GL\_EDGE\_FLAG\_ARRAY\_POINTER</span></span>

<span data-ttu-id="36058-138">[**glIsEnabled**](glisenabled.md) con el argumento \_ \_ matriz de marca del borde de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="36058-138">[**glIsEnabled**](glisenabled.md) with argument GL\_EDGE\_FLAG\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="36058-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36058-139">Requirements</span></span>



| <span data-ttu-id="36058-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="36058-140">Requirement</span></span> | <span data-ttu-id="36058-141">Value</span><span class="sxs-lookup"><span data-stu-id="36058-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36058-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36058-142">Minimum supported client</span></span><br/> | <span data-ttu-id="36058-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="36058-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="36058-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36058-144">Minimum supported server</span></span><br/> | <span data-ttu-id="36058-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36058-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36058-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36058-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="36058-147"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="36058-147"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="36058-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36058-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="36058-149"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36058-149"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="36058-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36058-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36058-151"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36058-151"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36058-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="36058-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36058-153">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="36058-153">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="36058-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="36058-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="36058-155">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="36058-155">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="36058-156">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="36058-156">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="36058-157">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="36058-157">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="36058-158">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="36058-158">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="36058-159">**glGet**</span><span class="sxs-lookup"><span data-stu-id="36058-159">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="36058-160">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="36058-160">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="36058-161">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="36058-161">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="36058-162">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="36058-162">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="36058-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="36058-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="36058-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="36058-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="36058-165">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="36058-165">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="36058-166">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="36058-166">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="36058-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="36058-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="36058-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="36058-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





