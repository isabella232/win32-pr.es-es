---
title: función glIndexPointer (GL. h)
description: La función glIndexPointer define una matriz de índices de color.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- glIndexPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489154"
---
# <a name="glindexpointer-function"></a><span data-ttu-id="68f08-104">glIndexPointer función)</span><span class="sxs-lookup"><span data-stu-id="68f08-104">glIndexPointer function</span></span>

<span data-ttu-id="68f08-105">La función **glIndexPointer** define una matriz de índices de color.</span><span class="sxs-lookup"><span data-stu-id="68f08-105">The **glIndexPointer** function defines an array of color indexes.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f08-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68f08-106">Syntax</span></span>


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="68f08-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68f08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f08-108">*type*</span><span class="sxs-lookup"><span data-stu-id="68f08-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="68f08-109">El tipo de datos de cada índice de color de la matriz mediante las siguientes constantes simbólicas: GL \_ Short, GL \_ int, GL \_ float, GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="68f08-109">The data type of each color index in the array using the following symbolic constants: GL\_SHORT, GL\_INT, GL\_FLOAT, GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="68f08-110">*STRI*</span><span class="sxs-lookup"><span data-stu-id="68f08-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="68f08-111">El desplazamiento de bytes entre índices de color consecutivos.</span><span class="sxs-lookup"><span data-stu-id="68f08-111">The byte offset between consecutive color indexes.</span></span> <span data-ttu-id="68f08-112">Cuando *STRIDE* es cero, los índices de color están estrechamente empaquetados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="68f08-112">When *stride* is zero, the color indexes are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="68f08-113">*puntero*</span><span class="sxs-lookup"><span data-stu-id="68f08-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="68f08-114">Puntero al primer índice de color de la matriz.</span><span class="sxs-lookup"><span data-stu-id="68f08-114">A pointer to the first color index in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f08-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68f08-115">Return value</span></span>

<span data-ttu-id="68f08-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="68f08-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68f08-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="68f08-117">Error codes</span></span>

<span data-ttu-id="68f08-118">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="68f08-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="68f08-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="68f08-119">Name</span></span>                                                                                              | <span data-ttu-id="68f08-120">Significado</span><span class="sxs-lookup"><span data-stu-id="68f08-120">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="68f08-121"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68f08-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="68f08-122">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="68f08-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="68f08-123"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68f08-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="68f08-124">*STRIDE* o *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="68f08-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68f08-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68f08-125">Remarks</span></span>

<span data-ttu-id="68f08-126">La función **glIndexPointer** especifica la ubicación y los datos de una matriz de índices de color que se van a utilizar al representar.</span><span class="sxs-lookup"><span data-stu-id="68f08-126">The **glIndexPointer** function specifies the location and data of an array of color indexes to use when rendering.</span></span> <span data-ttu-id="68f08-127">El parámetro de *tipo* especifica el tipo de datos de cada índice de color y *STRIDE* determina el desplazamiento de bytes de un índice de color al siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="68f08-127">The *type* parameter specifies the data type of each color index and *stride* determines the byte offset from one color index to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="68f08-128">En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="68f08-128">In some implementations, storing the vertices and attributes in a single array can be more efficient than using separate arrays.</span></span> <span data-ttu-id="68f08-129">Para obtener más información, vea [**glInterleavedArrays**](glinterleavedarrays.md).</span><span class="sxs-lookup"><span data-stu-id="68f08-129">For more information, see [**glInterleavedArrays**](glinterleavedarrays.md).</span></span>

<span data-ttu-id="68f08-130">Una matriz de índice de color se habilita al especificar la constante de matriz de índice de GL \_ \_ con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="68f08-130">A color-index array is enabled when you specify the GL\_INDEX\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="68f08-131">Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md) y [**glArrayElement**](glarrayelement.md) usan la matriz de índices de color.</span><span class="sxs-lookup"><span data-stu-id="68f08-131">When enabled, [**glDrawArrays**](gldrawarrays.md) and [**glArrayElement**](glarrayelement.md) use the color-index array.</span></span> <span data-ttu-id="68f08-132">De forma predeterminada, la matriz de índices de color está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="68f08-132">By default the color-index array is disabled.</span></span>

<span data-ttu-id="68f08-133">No se puede incluir **glIndexPointer** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="68f08-133">You cannot include **glIndexPointer** in display lists.</span></span>

<span data-ttu-id="68f08-134">Cuando se especifica una matriz de índice de color mediante **glIndexPointer**, los valores de todos los parámetros de matriz de índice de color de la función se guardan en un estado del lado cliente y los elementos de matriz estáticos se pueden almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="68f08-134">When you specify a color-index array using **glIndexPointer**, the values of all the function's color-index array parameters are saved in a client-side state and static array elements can be cached.</span></span> <span data-ttu-id="68f08-135">Dado que los parámetros de matriz de índice de color son de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="68f08-135">Because the color-index array parameters are client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span>

<span data-ttu-id="68f08-136">Aunque no se genera ningún error cuando se llama a **glIndexPointer** en pares [**glBegin**](glbegin.md) y **glEnd** , los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="68f08-136">Although no error is generated when you call **glIndexPointer** within [**glBegin**](glbegin.md) and **glEnd** pairs, the results are undefined.</span></span>

<span data-ttu-id="68f08-137">Las siguientes funciones recuperan información relacionada con **glIndexPointer**:</span><span class="sxs-lookup"><span data-stu-id="68f08-137">The following functions retrieve information related to **glIndexPointer**:</span></span>

<span data-ttu-id="68f08-138">[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="68f08-138">[**glIsEnabled**](glisenabled.md) with argument GL\_INDEX\_ARRAY</span></span>

<span data-ttu-id="68f08-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ intervalo de \_ matriz de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="68f08-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_INDEX\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="68f08-140">**glGet** con argumento \_ \_ recuento de matriz de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="68f08-140">**glGet** with argument GL\_INDEX\_ARRAY\_COUNT</span></span>

<span data-ttu-id="68f08-141">**glGet** con argumento \_ tipo de \_ matriz de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="68f08-141">**glGet** with argument GL\_INDEX\_ARRAY\_TYPE</span></span>

<span data-ttu-id="68f08-142">**glGet** con el argumento \_ \_ tamaño de matriz de índice de GL \_</span><span class="sxs-lookup"><span data-stu-id="68f08-142">**glGet** with argument GL\_INDEX\_ARRAY\_SIZE</span></span>

<span data-ttu-id="68f08-143">[**glGetPointerv**](glgetpointerv.md) con argumento de \_ matriz de índice de contabilidad de argumentos \_ \_</span><span class="sxs-lookup"><span data-stu-id="68f08-143">[**glGetPointerv**](glgetpointerv.md) with argument GL\_INDEX\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="68f08-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68f08-144">Requirements</span></span>



| <span data-ttu-id="68f08-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="68f08-145">Requirement</span></span> | <span data-ttu-id="68f08-146">Value</span><span class="sxs-lookup"><span data-stu-id="68f08-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68f08-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68f08-147">Minimum supported client</span></span><br/> | <span data-ttu-id="68f08-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68f08-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="68f08-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68f08-149">Minimum supported server</span></span><br/> | <span data-ttu-id="68f08-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68f08-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68f08-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68f08-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="68f08-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="68f08-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="68f08-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68f08-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="68f08-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68f08-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="68f08-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68f08-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68f08-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f08-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68f08-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="68f08-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f08-158">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="68f08-158">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="68f08-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="68f08-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="68f08-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="68f08-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="68f08-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="68f08-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="68f08-162">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="68f08-162">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="68f08-163">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="68f08-163">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="68f08-164">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="68f08-164">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="68f08-165">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="68f08-165">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="68f08-166">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="68f08-166">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="68f08-167">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="68f08-167">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





