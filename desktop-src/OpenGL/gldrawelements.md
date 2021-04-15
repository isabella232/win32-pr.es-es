---
title: función glDrawElements (GL. h)
description: La función glDrawElements representa primitivos de los datos de la matriz.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- glDrawElements (función) OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534486"
---
# <a name="gldrawelements-function"></a><span data-ttu-id="9fbb7-104">glDrawElements función)</span><span class="sxs-lookup"><span data-stu-id="9fbb7-104">glDrawElements function</span></span>

<span data-ttu-id="9fbb7-105">La función **glDrawElements** representa primitivos de los datos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-105">The **glDrawElements** function renders primitives from array data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fbb7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fbb7-106">Syntax</span></span>


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a><span data-ttu-id="9fbb7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fbb7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fbb7-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="9fbb7-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="9fbb7-109">Tipo de primitivas que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-109">The kind of primitives to render.</span></span> <span data-ttu-id="9fbb7-110">Puede suponer uno de los siguientes valores simbólicos: \_ puntos de contabilidad, \_ franja de línea de contabilidad, bucle de línea de libro de contabilidad, \_ \_ \_ líneas de contabilidad general, franja de \_ \_ triángulo de contabilidad \_ , ventilador de triángulo de contabilidad general, \_ \_ \_ triángulos de GL, franja cuádruple de contabilidad, \_ \_ cuádruples de contabilidad \_ y polígono de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="9fbb7-110">It can assume one of the following symbolic values: GL\_POINTS, GL\_LINE\_STRIP, GL\_LINE\_LOOP, GL\_LINES, GL\_TRIANGLE\_STRIP, GL\_TRIANGLE\_FAN, GL\_TRIANGLES, GL\_QUAD\_STRIP, GL\_QUADS, and GL\_POLYGON.</span></span>

</dd> <dt>

<span data-ttu-id="9fbb7-111">*count*</span><span class="sxs-lookup"><span data-stu-id="9fbb7-111">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="9fbb7-112">Número de elementos que se van a representar.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-112">The number of elements to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="9fbb7-113">*type*</span><span class="sxs-lookup"><span data-stu-id="9fbb7-113">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="9fbb7-114">Tipo de los valores de los índices.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-114">The type of the values in indices.</span></span> <span data-ttu-id="9fbb7-115">Debe ser un byte sin signo de libro de contabilidad, un valor \_ \_ \_ Short sin signo o un valor entero de GL \_ \_ sin signo \_ .</span><span class="sxs-lookup"><span data-stu-id="9fbb7-115">Must be one of GL\_UNSIGNED\_BYTE, GL\_UNSIGNED\_SHORT, or GL\_UNSIGNED\_INT.</span></span>

</dd> <dt>

<span data-ttu-id="9fbb7-116">*índices*</span><span class="sxs-lookup"><span data-stu-id="9fbb7-116">*indices*</span></span> 
</dt> <dd>

<span data-ttu-id="9fbb7-117">Puntero a la ubicación donde se almacenan los índices.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-117">A pointer to the location where the indices are stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fbb7-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fbb7-118">Return value</span></span>

<span data-ttu-id="9fbb7-119">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-119">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9fbb7-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9fbb7-120">Error codes</span></span>

<span data-ttu-id="9fbb7-121">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-121">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9fbb7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fbb7-122">Name</span></span>                                                                                                  | <span data-ttu-id="9fbb7-123">Significado</span><span class="sxs-lookup"><span data-stu-id="9fbb7-123">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9fbb7-124"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fbb7-124"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="9fbb7-125">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-125">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="9fbb7-126"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fbb7-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9fbb7-127">*Count* era un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-127">*count* was a negative value.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="9fbb7-128"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fbb7-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9fbb7-129">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9fbb7-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9fbb7-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fbb7-130">Remarks</span></span>

<span data-ttu-id="9fbb7-131">La función **glDrawElements** permite especificar varias primitivas geométricas con muy pocas llamadas de función.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-131">The **glDrawElements** function enables you to specify multiple geometric primitives with very few function calls.</span></span> <span data-ttu-id="9fbb7-132">En lugar de llamar a una función de OpenGL para pasar cada vértice, normal o color individual, puede especificar de antemano matrices independientes de vértices, normales y colores y utilizarlos para definir una secuencia de primitivas (todo el mismo tipo) con una única llamada a **glDrawElements**.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-132">Instead of calling an OpenGL function to pass each individual vertex, normal, or color, you can specify separate arrays of vertices, normals, and colors beforehand and use them to define a sequence of primitives (all of the same type) with a single call to **glDrawElements**.</span></span>

<span data-ttu-id="9fbb7-133">Cuando se llama a la función **glDrawElements** , se usan elementos secuenciales de *recuento* de *índices* para construir una secuencia de primitivas geométricas.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-133">When you call the **glDrawElements** function, it uses *count* sequential elements from *indices* to construct a sequence of geometric primitives.</span></span> <span data-ttu-id="9fbb7-134">El parámetro *mode* especifica qué tipo de primitivas se construyen y cómo se usan los elementos de la matriz para construir estos primitivos.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-134">The *mode* parameter specifies what kind of primitives are constructed, and how the array elements are used to construct these primitives.</span></span> <span data-ttu-id="9fbb7-135">Si \_ \_ no está habilitada la matriz de vértices de contabilidad, no se generan primitivas geométricas.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-135">If GL\_VERTEX\_ARRAY is not enabled, no geometric primitives are generated.</span></span>

<span data-ttu-id="9fbb7-136">Los atributos de vértices modificados por **glDrawElements** tienen un valor no especificado después de que **glDrawElements** devuelve.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-136">Vertex attributes that are modified by **glDrawElements** have an unspecified value after **glDrawElements** returns.</span></span> <span data-ttu-id="9fbb7-137">Por ejemplo, si \_ \_ la matriz de colores de GL está habilitada, el valor del color actual no está definido después de que se ejecute **glDrawElements** .</span><span class="sxs-lookup"><span data-stu-id="9fbb7-137">For example, if GL\_COLOR\_ARRAY is enabled, the value of the current color is undefined after **glDrawElements** executes.</span></span> <span data-ttu-id="9fbb7-138">Los atributos que no se modifican permanecen inalterados.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-138">Attributes that aren't modified remain unchanged.</span></span>

<span data-ttu-id="9fbb7-139">Puede incluir la función **glDrawElements** en mostrar listas.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-139">You can include the **glDrawElements** function in display lists.</span></span> <span data-ttu-id="9fbb7-140">Cuando **glDrawElements** se incluye en una lista de visualización, los datos de la matriz necesarios (determinados por los punteros de matriz y habilitados) también se especifican en la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-140">When **glDrawElements** is included in a display list, the necessary array data (determined by the array pointers and enables) is also entered into the display list.</span></span> <span data-ttu-id="9fbb7-141">Dado que los punteros de matriz y los habilitados son variables de estado de cliente, sus valores afectan a las listas de visualización cuando se crean las listas, no cuando se ejecutan las listas.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-141">Because the array pointers and enables are client-side state variables, their values affect display lists when the lists are created, not when the lists are executed.</span></span>

> [!Note]  
> <span data-ttu-id="9fbb7-142">La función **glDrawElements** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9fbb7-142">The **glDrawElements** function is only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9fbb7-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fbb7-143">Requirements</span></span>



| <span data-ttu-id="9fbb7-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fbb7-144">Requirement</span></span> | <span data-ttu-id="9fbb7-145">Value</span><span class="sxs-lookup"><span data-stu-id="9fbb7-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fbb7-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fbb7-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9fbb7-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9fbb7-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9fbb7-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fbb7-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9fbb7-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9fbb7-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9fbb7-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fbb7-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fbb7-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fbb7-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9fbb7-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fbb7-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fbb7-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fbb7-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9fbb7-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fbb7-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fbb7-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fbb7-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fbb7-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fbb7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fbb7-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-165">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-165">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="9fbb7-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="9fbb7-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





