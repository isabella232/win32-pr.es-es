---
title: función glColorPointer (GL. h)
description: La función glColorPointer define una matriz de colores.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- glColorPointer (función) OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489737"
---
# <a name="glcolorpointer-function"></a><span data-ttu-id="1e146-104">glColorPointer función)</span><span class="sxs-lookup"><span data-stu-id="1e146-104">glColorPointer function</span></span>

<span data-ttu-id="1e146-105">La función **glColorPointer** define una matriz de colores.</span><span class="sxs-lookup"><span data-stu-id="1e146-105">The **glColorPointer** function defines an array of colors.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e146-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e146-106">Syntax</span></span>


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="1e146-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e146-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e146-108">*size*</span><span class="sxs-lookup"><span data-stu-id="1e146-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="1e146-109">El número de componentes por color.</span><span class="sxs-lookup"><span data-stu-id="1e146-109">The number of components per color.</span></span> <span data-ttu-id="1e146-110">El valor debe ser 3 ó 4.</span><span class="sxs-lookup"><span data-stu-id="1e146-110">The value must be either 3 or 4.</span></span>

</dd> <dt>

<span data-ttu-id="1e146-111">*type*</span><span class="sxs-lookup"><span data-stu-id="1e146-111">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="1e146-112">El tipo de datos de cada componente de color de una matriz de colores.</span><span class="sxs-lookup"><span data-stu-id="1e146-112">The data type of each color component in a color array.</span></span> <span data-ttu-id="1e146-113">Los tipos de datos aceptables se especifican con las siguientes constantes: \_ bytes de GL, \_ bytes sin signo de contabilidad general, \_ GL \_ Short, GL \_ sin signo \_ corto, GL \_ int, libro de contabilidad \_ sin signo de contabilidad flotante, \_ GL \_ float o GL \_ doble.</span><span class="sxs-lookup"><span data-stu-id="1e146-113">Acceptable data types are specified with the following constants: GL\_BYTE, GL\_UNSIGNED\_BYTE, GL\_SHORT, GL\_UNSIGNED\_SHORT, GL\_INT, GL\_UNSIGNED\_INT, GL\_FLOAT, or GL\_DOUBLE.</span></span>

</dd> <dt>

<span data-ttu-id="1e146-114">*STRI*</span><span class="sxs-lookup"><span data-stu-id="1e146-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="1e146-115">Desplazamiento de bytes entre colores consecutivos.</span><span class="sxs-lookup"><span data-stu-id="1e146-115">The byte offset between consecutive colors.</span></span> <span data-ttu-id="1e146-116">Cuando *STRIDE* es cero, los colores se empaquetan estrechamente en la matriz.</span><span class="sxs-lookup"><span data-stu-id="1e146-116">When *stride* is zero, the colors are tightly packed in the array.</span></span>

</dd> <dt>

<span data-ttu-id="1e146-117">*puntero*</span><span class="sxs-lookup"><span data-stu-id="1e146-117">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="1e146-118">Puntero al primer componente del primer elemento de color de una matriz de colores.</span><span class="sxs-lookup"><span data-stu-id="1e146-118">A pointer to the first component of the first color element in a color array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e146-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e146-119">Return value</span></span>

<span data-ttu-id="1e146-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e146-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e146-121">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1e146-121">Error codes</span></span>

<span data-ttu-id="1e146-122">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="1e146-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1e146-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e146-123">Name</span></span>                                                                                              | <span data-ttu-id="1e146-124">Significado</span><span class="sxs-lookup"><span data-stu-id="1e146-124">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1e146-125"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e146-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1e146-126">*el tamaño* no era 3 ó 4.</span><span class="sxs-lookup"><span data-stu-id="1e146-126">*size* was not 3 or 4.</span></span><br/>            |
| <dl> <span data-ttu-id="1e146-127"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e146-127"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="1e146-128">el *tipo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="1e146-128">*type* was not an accepted value.</span></span><br/> |
| <dl> <span data-ttu-id="1e146-129"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e146-129"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="1e146-130">*STRIDE* o *Count* era negativo.</span><span class="sxs-lookup"><span data-stu-id="1e146-130">*stride* or *count* was negative.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e146-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e146-131">Remarks</span></span>

<span data-ttu-id="1e146-132">La función **glColorPointer** especifica la ubicación y el formato de datos de una matriz de componentes de color que se va a utilizar al representar.</span><span class="sxs-lookup"><span data-stu-id="1e146-132">The **glColorPointer** function specifies the location and data format of an array of color components to use when rendering.</span></span> <span data-ttu-id="1e146-133">El parámetro *STRIDE* determina el desplazamiento de bytes de un color a la siguiente, lo que permite el empaquetado de atributos de vértice en una sola matriz o almacenamiento en matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="1e146-133">The *stride* parameter determines the byte offset from one color to the next, enabling the packing of vertex attributes in a single array or storage in separate arrays.</span></span> <span data-ttu-id="1e146-134">En algunas implementaciones, el almacenamiento de atributos de vértices en una sola matriz puede ser más eficaz que el uso de matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="1e146-134">In some implementations, storing vertex attributes in a single array can be more efficient than the use of separate arrays.</span></span>

<span data-ttu-id="1e146-135">La matriz de colores se habilita especificando la \_ \_ constante de matriz de colores GL con [**glEnableClientState**](glenableclientstate.md).</span><span class="sxs-lookup"><span data-stu-id="1e146-135">Enabled the color array by specifying the GL\_COLOR\_ARRAY constant with [**glEnableClientState**](glenableclientstate.md).</span></span> <span data-ttu-id="1e146-136">La llamada a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md) usa la matriz de colores que, por tanto, está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1e146-136">Calling [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md) uses the color array that is thus enabled.</span></span> <span data-ttu-id="1e146-137">De forma predeterminada, la matriz de colores está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="1e146-137">By default, the color array is disabled.</span></span> <span data-ttu-id="1e146-138">Las llamadas a **glColorPointer** no se pueden escribir en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="1e146-138">The **glColorPointer** calls cannot by entered in display lists.</span></span>

<span data-ttu-id="1e146-139">Cuando se especifica una matriz de colores mediante **glColorPointer**, los valores de todos los parámetros de la matriz de colores de la función se guardan en un estado de cliente y se pueden almacenar en caché los elementos de matriz estáticos.</span><span class="sxs-lookup"><span data-stu-id="1e146-139">When you specify a color array using **glColorPointer**, the values of all the function's color array parameters are saved in a client-side state, and you can cache static array elements.</span></span> <span data-ttu-id="1e146-140">Dado que los parámetros de la matriz de colores están en un estado de cliente, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) no guardan ni restauran los valores de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="1e146-140">Because the color array parameters are in a client-side state, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) do not save or restore the parameters' values.</span></span>

<span data-ttu-id="1e146-141">Aunque si se especifica la matriz de colores en pares [**glBegin**](glbegin.md) y [**glend**](glend.md) no se genera un error, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1e146-141">Although specifying the color array within [**glBegin**](glbegin.md) and [**glend**](glend.md) pairs does not generate an error, the results are undefined.</span></span>

<span data-ttu-id="1e146-142">Las siguientes funciones recuperan información relacionada con la función **glColorPointer** :</span><span class="sxs-lookup"><span data-stu-id="1e146-142">The following functions retrieve information related to the **glColorPointer** function:</span></span>

<span data-ttu-id="1e146-143">[**glIsEnabled**](glisenabled.md) con el argumento \_ matriz de color de GL \_</span><span class="sxs-lookup"><span data-stu-id="1e146-143">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_ARRAY</span></span>

<span data-ttu-id="1e146-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ \_ tamaño de matriz de color de GL \_</span><span class="sxs-lookup"><span data-stu-id="1e146-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_ARRAY\_SIZE</span></span>

<span data-ttu-id="1e146-145">**glGet** con el argumento \_ \_ tipo de matriz de color GL \_</span><span class="sxs-lookup"><span data-stu-id="1e146-145">**glGet** with argument GL\_COLOR\_ARRAY\_TYPE</span></span>

<span data-ttu-id="1e146-146">**glGet** con argumento \_ intervalo de \_ matriz de color de GL \_</span><span class="sxs-lookup"><span data-stu-id="1e146-146">**glGet** with argument GL\_COLOR\_ARRAY\_STRIDE</span></span>

<span data-ttu-id="1e146-147">**glGet** con el argumento \_ \_ número de matriz de color de GL \_</span><span class="sxs-lookup"><span data-stu-id="1e146-147">**glGet** with argument GL\_COLOR\_ARRAY\_COUNT</span></span>

<span data-ttu-id="1e146-148">[**glGetPointerv**](glgetpointerv.md) con el argumento de \_ matriz de color de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e146-148">[**glGetPointerv**](glgetpointerv.md) with argument GL\_COLOR\_ARRAY\_POINTER</span></span>

## <a name="requirements"></a><span data-ttu-id="1e146-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e146-149">Requirements</span></span>



| <span data-ttu-id="1e146-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e146-150">Requirement</span></span> | <span data-ttu-id="1e146-151">Value</span><span class="sxs-lookup"><span data-stu-id="1e146-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e146-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e146-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1e146-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e146-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e146-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e146-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1e146-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e146-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e146-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e146-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e146-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e146-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1e146-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e146-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e146-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e146-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e146-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e146-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e146-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e146-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e146-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e146-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e146-163">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="1e146-163">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="1e146-164">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1e146-164">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1e146-165">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="1e146-165">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="1e146-166">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="1e146-166">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="1e146-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="1e146-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="1e146-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1e146-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1e146-169">**glGet**</span><span class="sxs-lookup"><span data-stu-id="1e146-169">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="1e146-170">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="1e146-170">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="1e146-171">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="1e146-171">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="1e146-172">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="1e146-172">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="1e146-173">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="1e146-173">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="1e146-174">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="1e146-174">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="1e146-175">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="1e146-175">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="1e146-176">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="1e146-176">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="1e146-177">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="1e146-177">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="1e146-178">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="1e146-178">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





