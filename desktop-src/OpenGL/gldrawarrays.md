---
title: función glDrawArrays (GL. h)
description: La función glDrawArrays especifica varios primitivos que se van a representar.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- glDrawArrays (función) OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996524"
---
# <a name="gldrawarrays-function"></a><span data-ttu-id="a332f-104">glDrawArrays función)</span><span class="sxs-lookup"><span data-stu-id="a332f-104">glDrawArrays function</span></span>

<span data-ttu-id="a332f-105">La función **glDrawArrays** especifica varios primitivos que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="a332f-105">The **glDrawArrays** function specifies multiple primitives to render.</span></span>

## <a name="syntax"></a><span data-ttu-id="a332f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a332f-106">Syntax</span></span>


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a><span data-ttu-id="a332f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a332f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a332f-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="a332f-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="a332f-109">Tipo de primitivas que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="a332f-109">The kind of primitives to render.</span></span> <span data-ttu-id="a332f-110">Las constantes siguientes especifican tipos aceptables de primitivas: \_ puntos de GL, \_ franja de líneas de libro de contabilidad \_ , bucle de línea de libro de contabilidad, \_ \_ \_ líneas de contabilidad general, franja de \_ triángulo de contabilidad \_ , ventilador de triángulo de contabilidad general, \_ triángulos de contabilidad, \_ \_ \_ franja cuádruple de GL, \_ cuádruples de contabilidad \_ y polígono de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="a332f-110">The following constants specify acceptable types of primitives: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="a332f-111">*first*</span><span class="sxs-lookup"><span data-stu-id="a332f-111">*first*</span></span> 
</dt> <dd>

<span data-ttu-id="a332f-112">Índice inicial de las matrices habilitadas.</span><span class="sxs-lookup"><span data-stu-id="a332f-112">The starting index in the enabled arrays.</span></span>

</dd> <dt>

<span data-ttu-id="a332f-113">*count*</span><span class="sxs-lookup"><span data-stu-id="a332f-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="a332f-114">Número de índices que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="a332f-114">The number of indexes to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a332f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a332f-115">Return value</span></span>

<span data-ttu-id="a332f-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a332f-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a332f-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a332f-117">Error codes</span></span>

<span data-ttu-id="a332f-118">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a332f-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a332f-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a332f-119">Name</span></span>                                                                                                  | <span data-ttu-id="a332f-120">Significado</span><span class="sxs-lookup"><span data-stu-id="a332f-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a332f-121"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a332f-121"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a332f-122">el *recuento* es negativo.</span><span class="sxs-lookup"><span data-stu-id="a332f-122">*count* was negative.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="a332f-123"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a332f-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="a332f-124">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="a332f-124">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="a332f-125"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a332f-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a332f-126">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a332f-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a332f-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a332f-127">Remarks</span></span>

<span data-ttu-id="a332f-128">Con **glDrawArrays**, puede especificar varias primitivas geométricas que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="a332f-128">With **glDrawArrays**, you can specify multiple geometric primitives to render.</span></span> <span data-ttu-id="a332f-129">En lugar de llamar a funciones OpenGL independientes para pasar cada vértice, normal o color individual, puede especificar matrices independientes de vértices, normales y colores para definir una secuencia de primitivas (todo el mismo tipo) con una única llamada a **glDrawArrays**.</span><span class="sxs-lookup"><span data-stu-id="a332f-129">Instead of calling separate OpenGL functions to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors to define a sequence of primitives (all the same kind) with a single call to **glDrawArrays**.</span></span>

<span data-ttu-id="a332f-130">Cuando se llama a **glDrawArrays**, el *recuento* de elementos secuenciales de cada matriz habilitada se usa para construir una secuencia de primitivas geométricas, empezando por el *primer* elemento.</span><span class="sxs-lookup"><span data-stu-id="a332f-130">When you call **glDrawArrays**, *count* sequential elements from each enabled array are used to construct a sequence of geometric primitives, beginning with the *first* element.</span></span> <span data-ttu-id="a332f-131">El parámetro *mode* especifica qué tipo de primitivo se debe construir y cómo usar los elementos de la matriz para construir los primitivos.</span><span class="sxs-lookup"><span data-stu-id="a332f-131">The *mode* parameter specifies what kind of primitive to construct and how to use the array elements to construct the primitives.</span></span>

<span data-ttu-id="a332f-132">Una vez que **glDrawArrays** devuelve, los valores de los atributos de vértice modificados por **glDrawArrays** son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="a332f-132">After **glDrawArrays** returns, the values of vertex attributes that are modified by **glDrawArrays** are undefined.</span></span> <span data-ttu-id="a332f-133">Por ejemplo, si \_ \_ la matriz de colores de GL está habilitada, el valor del color actual no está definido después de que **glDrawArrays** devuelva.</span><span class="sxs-lookup"><span data-stu-id="a332f-133">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawArrays** returns.</span></span> <span data-ttu-id="a332f-134">Los atributos no modificados por **glDrawArrays** permanecen definidos.</span><span class="sxs-lookup"><span data-stu-id="a332f-134">Attributes not modified by **glDrawArrays** remain defined.</span></span> <span data-ttu-id="a332f-135">Cuando \_ \_ no se habilita la matriz de vértices de contabilidad, no se generan primitivas geométricas, pero los atributos correspondientes a las matrices habilitadas se modifican.</span><span class="sxs-lookup"><span data-stu-id="a332f-135">When GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated but the attributes corresponding to enabled arrays are modified.</span></span>

<span data-ttu-id="a332f-136">Puede incluir **glDrawArrays** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="a332f-136">You can include **glDrawArrays** in display lists.</span></span> <span data-ttu-id="a332f-137">Cuando se incluye **glDrawArrays** en una lista de visualización, los datos de la matriz necesarios, determinados por los punteros de matriz y habilitados, se generan y se escriben en la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="a332f-137">When you include **glDrawArrays** in a display list, the necessary array data, determined by the array pointers and the enables, are generated and entered in the display list.</span></span> <span data-ttu-id="a332f-138">Los valores de punteros de matriz y habilitados se determinan durante la creación de listas de presentación.</span><span class="sxs-lookup"><span data-stu-id="a332f-138">The values of array pointers and enables are determined during the creation of display lists.</span></span>

<span data-ttu-id="a332f-139">Puede leer datos de matriz estática en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="a332f-139">You can read static array data at any time.</span></span> <span data-ttu-id="a332f-140">Si se modifican los elementos de una matriz estática y no se especifica de nuevo la matriz, los resultados de las llamadas subsiguientes a **glDrawArrays** no se definen.</span><span class="sxs-lookup"><span data-stu-id="a332f-140">If any static array elements are modified and the array is not specified again, the results of any subsequent calls to **glDrawArrays** are undefined.</span></span>

<span data-ttu-id="a332f-141">Aunque no se genera ningún error cuando se especifica una matriz más de una vez dentro de pares [**glBegin**](glbegin.md) y [**glend**](glend.md) , los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="a332f-141">Although no error is generated when you specify an array more than once within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs, the results are undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="a332f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a332f-142">Requirements</span></span>



| <span data-ttu-id="a332f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a332f-143">Requirement</span></span> | <span data-ttu-id="a332f-144">Value</span><span class="sxs-lookup"><span data-stu-id="a332f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a332f-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a332f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a332f-146">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a332f-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a332f-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a332f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a332f-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a332f-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a332f-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a332f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a332f-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a332f-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a332f-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a332f-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="a332f-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a332f-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a332f-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a332f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a332f-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a332f-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a332f-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="a332f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a332f-156">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="a332f-156">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="a332f-157">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a332f-157">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a332f-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="a332f-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="a332f-159">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="a332f-159">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="a332f-160">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a332f-160">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a332f-161">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="a332f-161">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="a332f-162">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="a332f-162">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="a332f-163">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="a332f-163">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="a332f-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="a332f-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="a332f-165">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="a332f-165">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="a332f-166">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="a332f-166">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





