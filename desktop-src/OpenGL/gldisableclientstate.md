---
title: función glDisableClientState (GL. h)
description: Las funciones glEnableClientState y glDisableClientState habilitan y deshabilitan las matrices, respectivamente. | función glDisableClientState (GL. h)
ms.assetid: b3316519-00ed-45f8-9c4b-2e04c483751e
keywords:
- glDisableClientState (función) OpenGL
topic_type:
- apiref
api_name:
- glDisableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 163a7c3b679c979e5c800d2aa41ba2abb00e11f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670199"
---
# <a name="gldisableclientstate-function"></a><span data-ttu-id="4fb8f-105">glDisableClientState función)</span><span class="sxs-lookup"><span data-stu-id="4fb8f-105">glDisableClientState function</span></span>

<span data-ttu-id="4fb8f-106">Las funciones [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** habilitan y deshabilitan las matrices, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-106">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable arrays respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb8f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fb8f-107">Syntax</span></span>


```C++
void WINAPI glDisableClientState(
   GLenum array
);
```



## <a name="parameters"></a><span data-ttu-id="4fb8f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fb8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb8f-109">*array*</span><span class="sxs-lookup"><span data-stu-id="4fb8f-109">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="4fb8f-110">Constante simbólica de la matriz que desea habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-110">A symbolic constant for the array you want to enable or disable.</span></span> <span data-ttu-id="4fb8f-111">Este parámetro puede suponer uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-111">This parameter can assume one of the following values.</span></span>



| <span data-ttu-id="4fb8f-112">Value</span><span class="sxs-lookup"><span data-stu-id="4fb8f-112">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="4fb8f-113">Significado</span><span class="sxs-lookup"><span data-stu-id="4fb8f-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <span data-ttu-id="4fb8f-114"><dt>**\_matriz de colores de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-114"><dt>**GL\_COLOR\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="4fb8f-115">Si está habilitada, use matrices de color con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-115">If enabled, use color arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="4fb8f-116">Vea también [**glColorPointer**](glcolorpointer.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-116">See also [**glColorPointer**](glcolorpointer.md).</span></span><br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <span data-ttu-id="4fb8f-117"><dt>**\_matriz de \_ marcas de borde de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-117"><dt>**GL\_EDGE\_FLAG\_ARRAY**</dt></span></span> </dl>             | <span data-ttu-id="4fb8f-118">Si está habilitada, use matrices de marca perimetral con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-118">If enabled, use edge flag arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="4fb8f-119">Vea también [**glEdgeFlagPointer**](gledgeflagpointer.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-119">See also [**glEdgeFlagPointer**](gledgeflagpointer.md).</span></span><br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <span data-ttu-id="4fb8f-120"><dt>**\_matriz de índice de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-120"><dt>**GL\_INDEX\_ARRAY**</dt></span></span> </dl>                          | <span data-ttu-id="4fb8f-121">Si está habilitada, use matrices de índice con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-121">If enabled, use index arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="4fb8f-122">Vea también [**glIndexPointer**](glindexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-122">See also [**glIndexPointer**](glindexpointer.md).</span></span><br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <span data-ttu-id="4fb8f-123"><dt>**\_matriz normal de contabilidad general \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-123"><dt>**GL\_NORMAL\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="4fb8f-124">Si está habilitada, use matrices normales con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-124">If enabled, use normal arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="4fb8f-125">Vea también [**glNormalPointer**](glnormalpointer.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-125">See also [**glNormalPointer**](glnormalpointer.md).</span></span><br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <span data-ttu-id="4fb8f-126"><dt>**\_matriz de \_ coordenadas de textura de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-126"><dt>**GL\_TEXTURE\_COORD\_ARRAY**</dt></span></span> </dl> | <span data-ttu-id="4fb8f-127">Si está habilitada, use matrices de coordenadas de textura con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-127">If enabled, use texture coordinate arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="4fb8f-128">Vea también [**glTexCoordPointer**](gltexcoordpointer.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-128">See also [**glTexCoordPointer**](gltexcoordpointer.md).</span></span><br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <span data-ttu-id="4fb8f-129"><dt>**\_matriz de vértices de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-129"><dt>**GL\_VERTEX\_ARRAY**</dt></span></span> </dl>                       | <span data-ttu-id="4fb8f-130">Si está habilitada, use matrices de vértices con llamadas a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-130">If enabled, use vertex arrays with calls to [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md), or [**glDrawArrays**](gldrawarrays.md).</span></span><br/> <span data-ttu-id="4fb8f-131">Vea también [**glVertexPointer**](glvertexpointer.md).</span><span class="sxs-lookup"><span data-stu-id="4fb8f-131">See also [**glVertexPointer**](glvertexpointer.md).</span></span><br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb8f-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fb8f-132">Return value</span></span>

<span data-ttu-id="4fb8f-133">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-133">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fb8f-134">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4fb8f-134">Error codes</span></span>

<span data-ttu-id="4fb8f-135">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-135">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4fb8f-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="4fb8f-136">Name</span></span>                                                                                             | <span data-ttu-id="4fb8f-137">Significado</span><span class="sxs-lookup"><span data-stu-id="4fb8f-137">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="4fb8f-138"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-138"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="4fb8f-139">la *matriz* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-139">*array* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4fb8f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fb8f-140">Remarks</span></span>

<span data-ttu-id="4fb8f-141">Las funciones [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** habilitan y deshabilitan varias matrices individuales.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-141">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions enable and disable various individual arrays.</span></span> <span data-ttu-id="4fb8f-142">Use [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para determinar el valor actual de cualquier funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-142">Use [**glIsEnabled**](glisenabled.md) or [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to determine the current setting of any capability.</span></span>

<span data-ttu-id="4fb8f-143">La llamada a [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** entre llamadas a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md) puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-143">Calling [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** between calls to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md) can cause an error.</span></span> <span data-ttu-id="4fb8f-144">Si no se genera ningún error, el comportamiento es indefinido.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-144">If no error is generated, the behavior is undefined.</span></span>

> [!Note]  
> <span data-ttu-id="4fb8f-145">Las funciones [**glEnableClientState**](glenableclientstate.md) y **glDisableClientState** solo están disponibles en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4fb8f-145">The [**glEnableClientState**](glenableclientstate.md) and **glDisableClientState** functions are only available in OpenGL version 1.1 or later.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fb8f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fb8f-146">Requirements</span></span>



| <span data-ttu-id="4fb8f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb8f-147">Requirement</span></span> | <span data-ttu-id="4fb8f-148">Value</span><span class="sxs-lookup"><span data-stu-id="4fb8f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb8f-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fb8f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb8f-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4fb8f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4fb8f-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fb8f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb8f-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fb8f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4fb8f-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fb8f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fb8f-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4fb8f-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4fb8f-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fb8f-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4fb8f-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fb8f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fb8f-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fb8f-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb8f-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb8f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb8f-160">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-160">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-162">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-162">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-163">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-163">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-164">**glDrawElements**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-164">**glDrawElements**</span></span>](gldrawelements.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-165">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-165">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-167">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-167">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-168">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-168">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-169">**glGetPointerv**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-169">**glGetPointerv**</span></span>](glgetpointerv.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-170">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-170">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-171">**glInterleavedArrays**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-171">**glInterleavedArrays**</span></span>](glinterleavedarrays.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-172">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-172">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-173">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-173">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="4fb8f-174">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="4fb8f-174">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





