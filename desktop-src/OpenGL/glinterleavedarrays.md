---
title: función glInterleavedArrays (GL. h)
description: La función glInterleavedArrays especifica y habilita simultáneamente varias matrices intercaladas en una matriz agregada más grande.
ms.assetid: f1133949-d755-43e3-bf29-8e4c7fb17980
keywords:
- glInterleavedArrays (función) OpenGL
topic_type:
- apiref
api_name:
- glInterleavedArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41403210e78d1a65dd700561243846d6e45bad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422043"
---
# <a name="glinterleavedarrays-function"></a><span data-ttu-id="2daa9-104">glInterleavedArrays función)</span><span class="sxs-lookup"><span data-stu-id="2daa9-104">glInterleavedArrays function</span></span>

<span data-ttu-id="2daa9-105">La función **glInterleavedArrays** especifica y habilita simultáneamente varias matrices intercaladas en una matriz agregada más grande.</span><span class="sxs-lookup"><span data-stu-id="2daa9-105">The **glInterleavedArrays** function simultaneously specifies and enables several interleaved arrays in a larger aggregate array.</span></span>

## <a name="syntax"></a><span data-ttu-id="2daa9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2daa9-106">Syntax</span></span>


```C++
void WINAPI glInterleavedArrays(
         GLenum  format,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a><span data-ttu-id="2daa9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2daa9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2daa9-108">*format*</span><span class="sxs-lookup"><span data-stu-id="2daa9-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="2daa9-109">Tipo de matriz que se va a habilitar.</span><span class="sxs-lookup"><span data-stu-id="2daa9-109">The type of array to enable.</span></span> <span data-ttu-id="2daa9-110">El parámetro puede suponer uno de los siguientes valores simbólicos: GL \_ V2F, GL \_ V3F, GL \_ C4UB \_ V2F, GL \_ C4UB \_ V3F, GL \_ C3F \_ V3F, GL \_ N3F \_ V3F, GL \_ C4F \_ N3F V3F \_ , GL \_ T2F \_ V3F, GL \_ T4F \_ V4F, GL \_ T2F C4UB V3F \_ \_ , GL \_ T2F C3F V3F, GL \_ \_ \_ T2F \_ N3F \_ V3F, GL \_ T2F \_ C4F \_ N3F \_ V3F o \_ GL \_ T4F \_ \_ C4F N3F V4F.</span><span class="sxs-lookup"><span data-stu-id="2daa9-110">The parameter can assume one of the following symbolic values: GL\_V2F, GL\_V3F, GL\_C4UB\_V2F, GL\_C4UB\_V3F, GL\_C3F\_V3F, GL\_N3F\_V3F, GL\_C4F\_N3F\_V3F, GL\_T2F\_V3F, GL\_T4F\_V4F, GL\_T2F\_C4UB\_V3F, GL\_T2F\_C3F\_V3F, GL\_T2F\_N3F\_V3F, GL\_T2F\_C4F\_N3F\_V3F, or GL\_T4F\_C4F\_N3F\_V4F.</span></span>

</dd> <dt>

<span data-ttu-id="2daa9-111">*STRI*</span><span class="sxs-lookup"><span data-stu-id="2daa9-111">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="2daa9-112">Desplazamiento en bytes entre cada elemento de la matriz agregado.</span><span class="sxs-lookup"><span data-stu-id="2daa9-112">The offset in bytes between each aggregate array element.</span></span>

</dd> <dt>

<span data-ttu-id="2daa9-113">*puntero*</span><span class="sxs-lookup"><span data-stu-id="2daa9-113">*pointer*</span></span> 
</dt> <dd>

<span data-ttu-id="2daa9-114">Puntero al primer elemento de una matriz agregada.</span><span class="sxs-lookup"><span data-stu-id="2daa9-114">A pointer to the first element of an aggregate array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2daa9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2daa9-115">Return value</span></span>

<span data-ttu-id="2daa9-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2daa9-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2daa9-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2daa9-117">Error codes</span></span>

<span data-ttu-id="2daa9-118">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="2daa9-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2daa9-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="2daa9-119">Name</span></span>                                                                                                  | <span data-ttu-id="2daa9-120">Significado</span><span class="sxs-lookup"><span data-stu-id="2daa9-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2daa9-121"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2daa9-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2daa9-122">el *formato* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="2daa9-122">*format* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="2daa9-123"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2daa9-123"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="2daa9-124">*STRIDE* era un valor negativo.</span><span class="sxs-lookup"><span data-stu-id="2daa9-124">*stride* was a negative value.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="2daa9-125"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2daa9-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2daa9-126">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2daa9-126">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2daa9-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2daa9-127">Remarks</span></span>

<span data-ttu-id="2daa9-128">Con la función **glInterleavedArrays** , puede especificar y habilitar simultáneamente varias matrices de color intercalado, normales, de textura y de vértices cuyos elementos formen parte de un elemento de matriz agregado mayor.</span><span class="sxs-lookup"><span data-stu-id="2daa9-128">With the **glInterleavedArrays** function, you can simultaneously specify and enable several interleaved color, normal, texture, and vertex arrays whose elements are part of a larger aggregate array element.</span></span> <span data-ttu-id="2daa9-129">En algunas arquitecturas de memoria, es más eficaz que especificar las matrices por separado.</span><span class="sxs-lookup"><span data-stu-id="2daa9-129">For some memory architectures, this is more efficient than specifying the arrays separately.</span></span>

<span data-ttu-id="2daa9-130">Si el parámetro *STRIDE* es cero, los elementos de la matriz agregada se almacenan consecutivamente; de lo contrario, se producen bytes *STRIDE* entre los elementos de matriz agregados.</span><span class="sxs-lookup"><span data-stu-id="2daa9-130">If the *stride* parameter is zero then the aggregate array elements are stored consecutively; otherwise *stride* bytes occur between aggregate array elements.</span></span>

<span data-ttu-id="2daa9-131">El parámetro *Format* sirve como una clave que describe cómo extraer matrices individuales de la matriz agregada:</span><span class="sxs-lookup"><span data-stu-id="2daa9-131">The *format* parameter serves as a key that describes how to extract individual arrays from the aggregate array:</span></span>

-   <span data-ttu-id="2daa9-132">Si *Format* contiene un T, las coordenadas de textura se extraen de la matriz intercalada.</span><span class="sxs-lookup"><span data-stu-id="2daa9-132">If *format* contains a T, then texture coordinates are extracted from the interleaved array.</span></span>
-   <span data-ttu-id="2daa9-133">Si C está presente, se extraen los valores de color.</span><span class="sxs-lookup"><span data-stu-id="2daa9-133">If C is present, color values are extracted.</span></span>
-   <span data-ttu-id="2daa9-134">Si N está presente, se extraen las coordenadas normales.</span><span class="sxs-lookup"><span data-stu-id="2daa9-134">If N is present, normal coordinates are extracted.</span></span>
-   <span data-ttu-id="2daa9-135">Las coordenadas del vértice siempre se extraen.</span><span class="sxs-lookup"><span data-stu-id="2daa9-135">Vertex coordinates are always extracted.</span></span>
-   <span data-ttu-id="2daa9-136">Los dígitos 2, 3 y 4 denotan el número de valores que se extraen.</span><span class="sxs-lookup"><span data-stu-id="2daa9-136">The digits 2, 3, and 4 denote how many values are extracted.</span></span>
-   <span data-ttu-id="2daa9-137">F indica que los valores se extraen como valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="2daa9-137">F indicates that values are extracted as floating point values.</span></span>
-   <span data-ttu-id="2daa9-138">Si 4UB sigue a la C, los colores también se pueden extraer como 4 bytes sin signo.</span><span class="sxs-lookup"><span data-stu-id="2daa9-138">If 4UB follows the C, colors may also be extracted as 4 unsigned bytes.</span></span> <span data-ttu-id="2daa9-139">Si un color se extrae como 4 bytes sin signo, el elemento de matriz de vértices que sigue se encuentra en la primera dirección alineada de punto flotante posible.</span><span class="sxs-lookup"><span data-stu-id="2daa9-139">If a color is extracted as 4 unsigned bytes, the vertex array element that follows is located at the first possible floating-point aligned address.</span></span>

<span data-ttu-id="2daa9-140">Si llama a **glInterleavedArrays** mientras compila una lista de visualización, no se compilará en la lista, pero se ejecutará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="2daa9-140">If you call **glInterleavedArrays** while compiling a display list, it is not compiled into the list but is executed immediately.</span></span>

<span data-ttu-id="2daa9-141">No se pueden incluir llamadas a **glInterleavedArrays** en **glDisableClientState** entre llamadas a [**glBegin**](glbegin.md) y la llamada correspondiente a **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="2daa9-141">You cannot include calls to **glInterleavedArrays** in **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to **glEnd**.</span></span>

> [!Note]  
> <span data-ttu-id="2daa9-142">La función **glInterleavedArrays** solo está disponible en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2daa9-142">The **glInterleavedArrays** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="2daa9-143">La función **glInterleavedArrays** se implementa en el lado cliente sin ningún protocolo.</span><span class="sxs-lookup"><span data-stu-id="2daa9-143">The **glInterleavedArrays** function is implemented on the client side with no protocol.</span></span> <span data-ttu-id="2daa9-144">Dado que los parámetros de la matriz de vértices son de cliente, no se guardan ni restauran en [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**.</span><span class="sxs-lookup"><span data-stu-id="2daa9-144">Because the vertex array parameters are client-side state, they are not saved or restored by [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**.</span></span> <span data-ttu-id="2daa9-145">En su lugar, use [**glPushClientAttrib**](glpushclientattrib.md) y **glPopClientAttrib** .</span><span class="sxs-lookup"><span data-stu-id="2daa9-145">Use [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="2daa9-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2daa9-146">Requirements</span></span>



| <span data-ttu-id="2daa9-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="2daa9-147">Requirement</span></span> | <span data-ttu-id="2daa9-148">Value</span><span class="sxs-lookup"><span data-stu-id="2daa9-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2daa9-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2daa9-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2daa9-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2daa9-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2daa9-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2daa9-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2daa9-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2daa9-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2daa9-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2daa9-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="2daa9-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2daa9-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2daa9-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2daa9-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="2daa9-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2daa9-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2daa9-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2daa9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2daa9-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2daa9-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2daa9-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="2daa9-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2daa9-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="2daa9-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="2daa9-161">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa9-161">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="2daa9-162">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="2daa9-162">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="2daa9-163">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="2daa9-163">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="2daa9-164">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa9-164">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="2daa9-165">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="2daa9-165">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="2daa9-166">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="2daa9-166">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="2daa9-167">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa9-167">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="2daa9-168">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa9-168">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="2daa9-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="2daa9-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="2daa9-170">**glPushClientAttrib**</span><span class="sxs-lookup"><span data-stu-id="2daa9-170">**glPushClientAttrib**</span></span>](glpushclientattrib.md)
</dt> <dt>

[<span data-ttu-id="2daa9-171">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa9-171">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="2daa9-172">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="2daa9-172">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





