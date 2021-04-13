---
title: función glPushClientAttrib (GL. h)
description: Las funciones glPushClientAttrib y glPopClientAttrib guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente. | función glPushClientAttrib (GL. h)
ms.assetid: 69f28af6-1023-4546-95ff-169525c23b07
keywords:
- glPushClientAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPushClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944e2e4229f0d36f0009ce337fd3806020322dbf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362355"
---
# <a name="glpushclientattrib-function"></a><span data-ttu-id="5ed98-105">glPushClientAttrib función)</span><span class="sxs-lookup"><span data-stu-id="5ed98-105">glPushClientAttrib function</span></span>

<span data-ttu-id="5ed98-106">Las funciones **glPushClientAttrib** y [**glPopClientAttrib**](glpopclientattrib.md) guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente.</span><span class="sxs-lookup"><span data-stu-id="5ed98-106">The **glPushClientAttrib** and [**glPopClientAttrib**](glpopclientattrib.md) functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed98-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ed98-107">Syntax</span></span>


```C++
void WINAPI glPushClientAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="5ed98-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ed98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed98-109">*mask*</span><span class="sxs-lookup"><span data-stu-id="5ed98-109">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="5ed98-110">Máscara que indica los atributos que se van a guardar.</span><span class="sxs-lookup"><span data-stu-id="5ed98-110">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="5ed98-111">A continuación se indican las constantes de máscara simbólica y sus Estados de cliente de OpenGL asociados.</span><span class="sxs-lookup"><span data-stu-id="5ed98-111">The following are the symbolic mask constants and their associated OpenGL client states.</span></span>



| <span data-ttu-id="5ed98-112">Value</span><span class="sxs-lookup"><span data-stu-id="5ed98-112">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="5ed98-113">Significado</span><span class="sxs-lookup"><span data-stu-id="5ed98-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="GL_CLIENT_PIXEL_STORE_BIT"></span><span id="gl_client_pixel_store_bit"></span><dl> <span data-ttu-id="5ed98-114"><dt>**\_bit de \_ almacén de píxeles de cliente de contabilidad \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-114"><dt>**GL\_CLIENT\_PIXEL\_STORE\_BIT**</dt></span></span> </dl>                                             | <span data-ttu-id="5ed98-115">Atributos de modo de almacenamiento en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5ed98-115">Pixel storage mode attributes.</span></span><br/>         |
| <span id="GL_CLIENT_VERTEX_ARRAY_BIT"></span><span id="gl_client_vertex_array_bit"></span><dl> <span data-ttu-id="5ed98-116"><dt>**\_bit de \_ matriz de vértices de cliente de \_ Contabilidad \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-116"><dt>**GL\_CLIENT\_VERTEX\_ARRAY\_BIT**</dt></span></span> </dl>                                          | <span data-ttu-id="5ed98-117">Atributos de la matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="5ed98-117">Vertex array attributes.</span></span><br/>               |
| <span id="GL_CLIENT_ALL_ATTRIB_BITs"></span><span id="gl_client_all_attrib_bits"></span><span id="GL_CLIENT_ALL_ATTRIB_BITS"></span><dl> <span data-ttu-id="5ed98-118"><dt>**\_ \_ Todos los \_ bits attrib \_ de cliente de contabilidad**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-118"><dt>**GL\_CLIENT\_ALL\_ATTRIB\_BITs**</dt></span></span> </dl> | <span data-ttu-id="5ed98-119">todos los atributos de estado de cliente que se van a apilar.</span><span class="sxs-lookup"><span data-stu-id="5ed98-119">all stackable client-state attributes.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed98-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ed98-120">Return value</span></span>

<span data-ttu-id="5ed98-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5ed98-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ed98-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5ed98-122">Error codes</span></span>

<span data-ttu-id="5ed98-123">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="5ed98-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5ed98-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ed98-124">Name</span></span>                                                                                               | <span data-ttu-id="5ed98-125">Significado</span><span class="sxs-lookup"><span data-stu-id="5ed98-125">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ed98-126"><dt>**desbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-126"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="5ed98-127">Se llamó a la función mientras la pila de atributos de cliente estaba llena.</span><span class="sxs-lookup"><span data-stu-id="5ed98-127">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5ed98-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ed98-128">Remarks</span></span>

<span data-ttu-id="5ed98-129">La función **glPushClientAttrib** usa su parámetro Mask para determinar qué grupos de variables de estado de cliente se guardan en la pila de atributo de cliente.</span><span class="sxs-lookup"><span data-stu-id="5ed98-129">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="5ed98-130">Puede usar el operador OR bit a bit para unir constantes simbólicas aceptadas para establecer bits y construir una máscara.</span><span class="sxs-lookup"><span data-stu-id="5ed98-130">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="5ed98-131">La función [**glPopClientAttrib**](glpopclientattrib.md) restaura los valores de las variables de estado de cliente que se guardaron por última vez con **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="5ed98-131">The [**glPopClientAttrib**](glpopclientattrib.md) function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="5ed98-132">Las variables de estado de cliente que no se guardaron previamente permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="5ed98-132">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="5ed98-133">Si se insertan atributos en una pila completa de atributos de cliente o se extraen atributos de una pila vacía, se establece una marca de error y no se realiza ningún otro cambio en el estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5ed98-133">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="5ed98-134">De forma predeterminada, la pila de atributos de cliente está vacía.</span><span class="sxs-lookup"><span data-stu-id="5ed98-134">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="5ed98-135">Algunos valores de estado de cliente de OpenGL no se pueden guardar en la pila de atributo de cliente.</span><span class="sxs-lookup"><span data-stu-id="5ed98-135">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="5ed98-136">Por ejemplo, no puede guardar los Estados SELECT o feedback en la pila Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="5ed98-136">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="5ed98-137">La profundidad de la pila de atributo de cliente es al menos 16.</span><span class="sxs-lookup"><span data-stu-id="5ed98-137">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="5ed98-138">Las funciones **glPushclientAttrib** y **glPopClientAttrib** no se compilan en listas de visualización, pero se ejecutan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5ed98-138">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="5ed98-139">Las funciones **glPushClientAttrib** y **glPopClientAttrib** solo pueden mostrar los modos de almacenamiento en píxeles y los Estados de cliente de matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="5ed98-139">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="5ed98-140">Debe usar [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) para los Estados de envío y de extracción que se mantienen en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5ed98-140">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="5ed98-141">Las funciones **glPushClientAttrib** y **glPopClientAttrib** solo están disponibles en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5ed98-141">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="5ed98-142">Las siguientes funciones recuperan información relacionada con **glPushClientAttrib** y **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="5ed98-142">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="5ed98-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumentos \_ profundidad de \_ pila de ATRIB de cliente de \_ Contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="5ed98-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="5ed98-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ Max \_ Client la \_ \_ \_ profundidad de la pila</span><span class="sxs-lookup"><span data-stu-id="5ed98-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed98-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed98-145">Requirements</span></span>



| <span data-ttu-id="5ed98-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed98-146">Requirement</span></span> | <span data-ttu-id="5ed98-147">Value</span><span class="sxs-lookup"><span data-stu-id="5ed98-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed98-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ed98-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed98-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5ed98-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5ed98-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ed98-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed98-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ed98-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ed98-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ed98-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed98-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-153"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5ed98-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ed98-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ed98-155"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-155"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5ed98-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ed98-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ed98-157"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed98-157"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed98-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ed98-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed98-159">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="5ed98-159">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="5ed98-160">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="5ed98-160">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="5ed98-161">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="5ed98-161">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="5ed98-162">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="5ed98-162">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="5ed98-163">**glGet**</span><span class="sxs-lookup"><span data-stu-id="5ed98-163">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="5ed98-164">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="5ed98-164">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="5ed98-165">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="5ed98-165">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="5ed98-166">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="5ed98-166">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="5ed98-167">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="5ed98-167">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="5ed98-168">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="5ed98-168">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="5ed98-169">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="5ed98-169">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="5ed98-170">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="5ed98-170">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="5ed98-171">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="5ed98-171">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





