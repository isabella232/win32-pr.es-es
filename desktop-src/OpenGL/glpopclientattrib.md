---
title: función glPopClientAttrib (GL. h)
description: Las funciones glPushClientAttrib y glPopClientAttrib guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente. | función glPopClientAttrib (GL. h)
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
keywords:
- glPopClientAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPopClientAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9f09e9c7292754a736594a9bf3d57a70063744
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362269"
---
# <a name="glpopclientattrib-function"></a><span data-ttu-id="485ca-105">glPopClientAttrib función)</span><span class="sxs-lookup"><span data-stu-id="485ca-105">glPopClientAttrib function</span></span>

<span data-ttu-id="485ca-106">Las funciones [**glPushClientAttrib**](glpushclientattrib.md) y **glPopClientAttrib** guardan y restauran grupos de variables de estado de cliente en la pila de atributo de cliente.</span><span class="sxs-lookup"><span data-stu-id="485ca-106">The [**glPushClientAttrib**](glpushclientattrib.md) and **glPopClientAttrib** functions save and restore groups of client-state variables on the client-attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="485ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="485ca-107">Syntax</span></span>


```C++
void WINAPI glPopClientAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="485ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="485ca-108">Parameters</span></span>

<span data-ttu-id="485ca-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="485ca-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="485ca-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="485ca-110">Return value</span></span>

<span data-ttu-id="485ca-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="485ca-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="485ca-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="485ca-112">Error codes</span></span>

<span data-ttu-id="485ca-113">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="485ca-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="485ca-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="485ca-114">Name</span></span>                                                                                               | <span data-ttu-id="485ca-115">Significado</span><span class="sxs-lookup"><span data-stu-id="485ca-115">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="485ca-116"><dt>**desbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="485ca-116"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="485ca-117">Se llamó a la función mientras la pila de atributos de cliente estaba llena.</span><span class="sxs-lookup"><span data-stu-id="485ca-117">The function was called while the client-attribute stack was full.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="485ca-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="485ca-118">Remarks</span></span>

<span data-ttu-id="485ca-119">La función **glPushClientAttrib** usa su parámetro Mask para determinar qué grupos de variables de estado de cliente se guardan en la pila de atributo de cliente.</span><span class="sxs-lookup"><span data-stu-id="485ca-119">The **glPushClientAttrib** function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack.</span></span> <span data-ttu-id="485ca-120">Puede usar el operador OR bit a bit para unir constantes simbólicas aceptadas para establecer bits y construir una máscara.</span><span class="sxs-lookup"><span data-stu-id="485ca-120">You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask.</span></span>

<span data-ttu-id="485ca-121">La función **glPopClientAttrib** restaura los valores de las variables de estado de cliente que se guardaron por última vez con **glPushclientAttrib**.</span><span class="sxs-lookup"><span data-stu-id="485ca-121">The **glPopClientAttrib** function restores the values of the client-state variables last saved with **glPushclientAttrib**.</span></span> <span data-ttu-id="485ca-122">Las variables de estado de cliente que no se guardaron previamente permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="485ca-122">Client-state variables not previously saved are left unchanged.</span></span> <span data-ttu-id="485ca-123">Si se insertan atributos en una pila completa de atributos de cliente o se extraen atributos de una pila vacía, se establece una marca de error y no se realiza ningún otro cambio en el estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="485ca-123">Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state.</span></span> <span data-ttu-id="485ca-124">De forma predeterminada, la pila de atributos de cliente está vacía.</span><span class="sxs-lookup"><span data-stu-id="485ca-124">By default the client attribute stack is empty.</span></span>

<span data-ttu-id="485ca-125">Algunos valores de estado de cliente de OpenGL no se pueden guardar en la pila de atributo de cliente.</span><span class="sxs-lookup"><span data-stu-id="485ca-125">Some OpenGL client-state values cannot be saved on the client-attribute stack.</span></span> <span data-ttu-id="485ca-126">Por ejemplo, no puede guardar los Estados SELECT o feedback en la pila Client-Attribute.</span><span class="sxs-lookup"><span data-stu-id="485ca-126">For example, you cannot save the select or feedback states on the client-attribute stack.</span></span> <span data-ttu-id="485ca-127">La profundidad de la pila de atributo de cliente es al menos 16.</span><span class="sxs-lookup"><span data-stu-id="485ca-127">The depth of the client-attribute stack is at least 16.</span></span>

<span data-ttu-id="485ca-128">Las funciones **glPushclientAttrib** y **glPopClientAttrib** no se compilan en listas de visualización, pero se ejecutan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="485ca-128">The **glPushclientAttrib** and **glPopClientAttrib** functions are not compiled into display lists, but are executed immediately.</span></span>

<span data-ttu-id="485ca-129">Las funciones **glPushClientAttrib** y **glPopClientAttrib** solo pueden mostrar los modos de almacenamiento en píxeles y los Estados de cliente de matriz de vértices.</span><span class="sxs-lookup"><span data-stu-id="485ca-129">The **glPushClientAttrib** and **glPopClientAttrib** functions can only push and pop pixel storage modes and vertex array client states.</span></span> <span data-ttu-id="485ca-130">Debe usar [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md) para los Estados de envío y de extracción que se mantienen en el servidor.</span><span class="sxs-lookup"><span data-stu-id="485ca-130">You must use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to push and pop states that are kept on the server.</span></span>

> [!Note]  
> <span data-ttu-id="485ca-131">Las funciones **glPushClientAttrib** y **glPopClientAttrib** solo están disponibles en la versión 1,1 o posterior de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="485ca-131">The **glPushClientAttrib** and **glPopClientAttrib** functions are only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="485ca-132">Las siguientes funciones recuperan información relacionada con **glPushClientAttrib** y **glPopClientAttrib**:</span><span class="sxs-lookup"><span data-stu-id="485ca-132">The following functions retrieve information related to **glPushClientAttrib** and **glPopClientAttrib**:</span></span>

<span data-ttu-id="485ca-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumentos \_ profundidad de \_ pila de ATRIB de cliente de \_ Contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="485ca-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="485ca-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ Max \_ Client la \_ \_ \_ profundidad de la pila</span><span class="sxs-lookup"><span data-stu-id="485ca-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_CLIENT\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="485ca-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="485ca-135">Requirements</span></span>



| <span data-ttu-id="485ca-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="485ca-136">Requirement</span></span> | <span data-ttu-id="485ca-137">Value</span><span class="sxs-lookup"><span data-stu-id="485ca-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="485ca-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="485ca-138">Minimum supported client</span></span><br/> | <span data-ttu-id="485ca-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="485ca-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="485ca-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="485ca-140">Minimum supported server</span></span><br/> | <span data-ttu-id="485ca-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="485ca-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="485ca-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="485ca-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="485ca-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="485ca-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="485ca-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="485ca-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="485ca-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="485ca-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="485ca-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="485ca-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="485ca-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="485ca-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="485ca-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="485ca-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485ca-149">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="485ca-149">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="485ca-150">**glDisableClientState**</span><span class="sxs-lookup"><span data-stu-id="485ca-150">**glDisableClientState**</span></span>](gldisableclientstate.md)
</dt> <dt>

[<span data-ttu-id="485ca-151">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="485ca-151">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="485ca-152">**glEnableClientState**</span><span class="sxs-lookup"><span data-stu-id="485ca-152">**glEnableClientState**</span></span>](glenableclientstate.md)
</dt> <dt>

[<span data-ttu-id="485ca-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="485ca-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="485ca-154">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="485ca-154">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="485ca-155">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="485ca-155">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="485ca-156">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="485ca-156">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="485ca-157">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="485ca-157">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="485ca-158">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="485ca-158">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="485ca-159">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="485ca-159">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="485ca-160">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="485ca-160">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="485ca-161">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="485ca-161">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





