---
title: función glNormalPointer (GL. h)
description: La función glNormalPointer define una matriz de normales.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- glNormalPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997131"
---
# <a name="glnormalpointer-function"></a><span data-ttu-id="81e44-104">glNormalPointer función)</span><span class="sxs-lookup"><span data-stu-id="81e44-104">glNormalPointer function</span></span>

<span data-ttu-id="81e44-105">La función **glNormalPointer** define una matriz de normales.</span><span class="sxs-lookup"><span data-stu-id="81e44-105">The **glNormalPointer** function defines an array of normals.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e44-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81e44-106">Syntax</span></span>


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="81e44-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81e44-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e44-108">*type*</span><span class="sxs-lookup"><span data-stu-id="81e44-108">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="81e44-109">El tipo de datos de cada coordenada de la matriz mediante las siguientes constantes simbólicas: GL \_ byte, GL \_ Short, GL \_ int, GL \_ float y GL \_ Double.</span><span class="sxs-lookup"><span data-stu-id="81e44-109">The data type of each coordinate in the array using the following symbolic constants: GL\_BYTE, GL\_SHORT, GL\_INT, GL\_FLOAT, and GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="81e44-110">*STRI*</span><span class="sxs-lookup"><span data-stu-id="81e44-110">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="81e44-111">El desplazamiento de bytes entre las normales consecutivas.</span><span class="sxs-lookup"><span data-stu-id="81e44-111">The byte offset between consecutive normals.</span></span> <span data-ttu-id="81e44-112">Cuando *STRIDE* es cero, los normales están estrechamente empaquetados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="81e44-112">When *stride* is zero, the normals are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="81e44-113">*puntero*</span><span class="sxs-lookup"><span data-stu-id="81e44-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="81e44-114">Puntero a la primera normal de la matriz.</span><span class="sxs-lookup"><span data-stu-id="81e44-114">A pointer to the first normal in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e44-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81e44-115">Return value</span></span>

<span data-ttu-id="81e44-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="81e44-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81e44-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="81e44-117">Error codes</span></span>

<span data-ttu-id="81e44-118">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="81e44-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="81e44-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="81e44-119">Name</span></span>                                                                                                  | <span data-ttu-id="81e44-120">Significado</span><span class="sxs-lookup"><span data-stu-id="81e44-120">Meaning</span></span>                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="81e44-121"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81e44-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="81e44-122">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="81e44-122">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="81e44-123"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81e44-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="81e44-124">*STRIDE* o *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="81e44-124">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="81e44-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81e44-125">Remarks</span></span>

<span data-ttu-id="81e44-126">La función **glNormalPointer** especifica la ubicación y los datos de una matriz de normalización que se va a utilizar al representar.</span><span class="sxs-lookup"><span data-stu-id="81e44-126">The **glNormalPointer** function specifies the location and data of an array of normals to use when rendering.</span></span> <span data-ttu-id="81e44-127">El parámetro de *tipo* especifica el tipo de datos de cada coordenada normal.</span><span class="sxs-lookup"><span data-stu-id="81e44-127">The *type* parameter specifies the data type of each normal coordinate.</span></span> <span data-ttu-id="81e44-128">El parámetro *STRIDE* determina el desplazamiento de bytes de una normal a la siguiente, lo que permite el empaquetado de vértices y atributos en una sola matriz o almacenamiento en matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="81e44-128">The *stride* parameter determines the byte offset from one normal to the next, enabling the packing of vertices and attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="81e44-129">En algunas implementaciones, el almacenamiento de vértices y atributos en una sola matriz puede ser más eficaz que el uso de matrices independientes. consulte [**glInterleavedArrays**](glinterleavedarrays.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="81e44-129">In some implementations storing the vertices and attributes in a single array can be more efficient than using separate arrays; see [**glInterleavedArrays**](glinterleavedarrays.md) for details.</span></span>

<span data-ttu-id="81e44-130">Una matriz normal se habilita cuando se especifica la \_ constante de \_ matriz normal de GL con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="81e44-130">A normal array is enabled when you specify the GL\_NORMAL\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="81e44-131">Cuando está habilitado, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) y [**glArrayElement**](glarrayelement.md) usan la matriz normal.</span><span class="sxs-lookup"><span data-stu-id="81e44-131">When enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) and [**glArrayElement**](glarrayelement.md) use the normal array.</span></span> <span data-ttu-id="81e44-132">De forma predeterminada, la matriz normal está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="81e44-132">By default the normal array is disabled.</span></span>

<span data-ttu-id="81e44-133">No se puede incluir **glNormalPointer** en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="81e44-133">You cannot include **glNormalPointer** in display lists.</span></span>

<span data-ttu-id="81e44-134">Cuando se especifica una matriz normal mediante **glNormalPointer**, los valores de todos los parámetros de matriz normales de la función se guardan en un estado del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="81e44-134">When you specify a normal array using **glNormalPointer**, the values of all the function's normal array parameters are saved in a client-side state.</span></span> <span data-ttu-id="81e44-135">Dado que los parámetros de matriz normales se guardan en un estado de cliente, los valores no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="81e44-135">Because the normal array parameters are saved in a client-side state, their values are not saved or restored by [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span>

<span data-ttu-id="81e44-136">Aunque no se genera ningún error cuando se llama a **glNormalPointer** en pares [**glBegin**](glbegin.md) y [**glEnd**](glend.md) , los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="81e44-136">Although no error is generated when you call **glNormalPointer** within [**glBegin**](glbegin.md) and [**glEnd**](glend.md) pairs, the results are undefined.</span></span>

<span data-ttu-id="81e44-137">Las siguientes funciones están asociadas a **glNormalPointer**:</span><span class="sxs-lookup"><span data-stu-id="81e44-137">The following functions are associated with **glNormalPointer**:</span></span>

<span data-ttu-id="81e44-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento \_ intervalo de \_ matriz \_ normal de GL</span><span class="sxs-lookup"><span data-stu-id="81e44-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NORMAL\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="81e44-139">**glGet** con el argumento \_ \_ recuento de matriz normal de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="81e44-139">**glGet** with argument GL\_NORMAL\_ARRAY\_COUNT</span></span>

<span data-ttu-id="81e44-140">**glGet** con argumento \_ tipo de \_ matriz \_ normal de contabilidad</span><span class="sxs-lookup"><span data-stu-id="81e44-140">**glGet** with argument GL\_NORMAL\_ARRAY\_TYPE</span></span>

<span data-ttu-id="81e44-141">**glGetPointerv** con el argumento \_ , \_ puntero de matriz normal de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="81e44-141">**glGetPointerv** with argument GL\_NORMAL\_ARRAY\_POINTER</span></span>

<span data-ttu-id="81e44-142">[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz normal de GL \_</span><span class="sxs-lookup"><span data-stu-id="81e44-142">[**glIsEnabled**](glisenabled.md) with argument GL\_NORMAL\_ARRAY</span></span>

## <a name="requirements"></a><span data-ttu-id="81e44-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81e44-143">Requirements</span></span>



| <span data-ttu-id="81e44-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e44-144">Requirement</span></span> | <span data-ttu-id="81e44-145">Value</span><span class="sxs-lookup"><span data-stu-id="81e44-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81e44-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81e44-146">Minimum supported client</span></span><br/> | <span data-ttu-id="81e44-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81e44-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81e44-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81e44-148">Minimum supported server</span></span><br/> | <span data-ttu-id="81e44-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81e44-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81e44-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81e44-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="81e44-151"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="81e44-151"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="81e44-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81e44-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="81e44-153"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81e44-153"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="81e44-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81e44-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81e44-155"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81e44-155"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e44-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="81e44-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e44-157">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="81e44-157">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="81e44-158">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="81e44-158">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="81e44-159">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="81e44-159">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="81e44-160">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="81e44-160">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="81e44-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="81e44-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="81e44-162">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="81e44-162">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="81e44-163">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="81e44-163">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="81e44-164">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="81e44-164">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="81e44-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="81e44-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="81e44-166">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="81e44-166">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="81e44-167">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="81e44-167">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="81e44-168">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="81e44-168">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> <dt>

[<span data-ttu-id="81e44-169">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="81e44-169">**glGetString**</span></span>](glgetstring.md)
</dt> </dl>

 

 





