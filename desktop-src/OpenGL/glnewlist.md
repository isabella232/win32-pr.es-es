---
title: función glNewList (GL. h)
description: Las funciones glNewList y glEndList crean o reemplazan una lista de visualización. | función glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glNewList (función) OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670175"
---
# <a name="glnewlist-function"></a><span data-ttu-id="28756-105">glNewList función)</span><span class="sxs-lookup"><span data-stu-id="28756-105">glNewList function</span></span>

<span data-ttu-id="28756-106">Las funciones **glNewList** y [**glEndList**](glendlist.md) crean o reemplazan una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="28756-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="28756-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28756-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="28756-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28756-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28756-109">*list*</span><span class="sxs-lookup"><span data-stu-id="28756-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="28756-110">Nombre de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="28756-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="28756-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="28756-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="28756-112">Modo de compilación.</span><span class="sxs-lookup"><span data-stu-id="28756-112">The compilation mode.</span></span> <span data-ttu-id="28756-113">Se aceptan los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="28756-113">The following values are accepted.</span></span>



| <span data-ttu-id="28756-114">Value</span><span class="sxs-lookup"><span data-stu-id="28756-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="28756-115">Significado</span><span class="sxs-lookup"><span data-stu-id="28756-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="28756-116"><dt>**\_compilación GL**</dt></span><span class="sxs-lookup"><span data-stu-id="28756-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="28756-117">Simplemente se compilan los comandos.</span><span class="sxs-lookup"><span data-stu-id="28756-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="28756-118"><dt>**\_compilación \_ y \_ ejecución de GL**</dt></span><span class="sxs-lookup"><span data-stu-id="28756-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="28756-119">Los comandos se ejecutan a medida que se compilan en la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="28756-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28756-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28756-120">Return value</span></span>

<span data-ttu-id="28756-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="28756-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28756-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="28756-122">Error codes</span></span>

<span data-ttu-id="28756-123">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="28756-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="28756-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="28756-124">Name</span></span>                                                                                                  | <span data-ttu-id="28756-125">Significado</span><span class="sxs-lookup"><span data-stu-id="28756-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28756-126"><dt>**\_valor no válido de GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28756-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="28756-127">la *lista* era cero.</span><span class="sxs-lookup"><span data-stu-id="28756-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="28756-128"><dt>**\_enumeración GL no válida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28756-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="28756-129">el *modo* no era un valor aceptado.</span><span class="sxs-lookup"><span data-stu-id="28756-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="28756-130"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28756-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="28756-131">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="28756-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="28756-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28756-132">Remarks</span></span>

<span data-ttu-id="28756-133">Las listas de visualización son grupos de comandos OpenGL que se han almacenado para su posterior ejecución.</span><span class="sxs-lookup"><span data-stu-id="28756-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="28756-134">Las listas de visualización se crean con **glNewList**.</span><span class="sxs-lookup"><span data-stu-id="28756-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="28756-135">Todos los comandos subsiguientes se colocan en la lista de visualización, en el orden emitido, hasta que se llame a **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="28756-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="28756-136">La función **glNewList** tiene dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="28756-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="28756-137">El primer parámetro, *List*, es un entero positivo que se convierte en el nombre único de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="28756-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="28756-138">Los nombres se pueden crear y reservar con [**glGenLists**](glgenlists.md) y probar la unicidad con [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="28756-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="28756-139">El segundo parámetro, *mode*, es una constante simbólica que puede suponer uno de los dos valores anteriores.</span><span class="sxs-lookup"><span data-stu-id="28756-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="28756-140">Algunos comandos no se compilan en la lista de visualización, pero se ejecutan inmediatamente, independientemente del modo de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="28756-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="28756-141">Estos comandos son [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)y todas las rutinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="28756-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="28756-142">De forma similar, [**glTexImage2D**](glteximage2d.md) y [**glTexImage1D**](glteximage1d.md) se ejecutan inmediatamente y no se compilan en la lista de visualización cuando su primer argumento es la textura de proxy \_ de contabilidad \_ \_ 2D o la \_ \_ textura de proxy de GL \_ 1D, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="28756-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="28756-143">Cuando se encuentra la función **glEndList** , la definición de la lista de visualización se completa mediante la Asociación de la lista con la *lista* de nombres únicos (especificada en el comando **glNewList** ).</span><span class="sxs-lookup"><span data-stu-id="28756-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="28756-144">Si ya existe una lista de visualización con la *lista* de nombres, solo se reemplaza cuando se llama a **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="28756-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="28756-145">Las funciones [**glCallList**](glcalllist.md) y [**glCallLists**](glcalllists.md) se pueden especificar en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="28756-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="28756-146">Los comandos de la lista de visualización o las listas ejecutadas por **glCallList** o **glCallLists** no se incluyen en la lista de visualización que se está creando, incluso si el modo de creación de lista es GL \_ compile \_ y \_ Execute.</span><span class="sxs-lookup"><span data-stu-id="28756-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="28756-147">La siguiente función recupera información relacionada con **glNewList**:</span><span class="sxs-lookup"><span data-stu-id="28756-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="28756-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="28756-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="28756-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28756-149">Requirements</span></span>



| <span data-ttu-id="28756-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="28756-150">Requirement</span></span> | <span data-ttu-id="28756-151">Value</span><span class="sxs-lookup"><span data-stu-id="28756-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28756-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28756-152">Minimum supported client</span></span><br/> | <span data-ttu-id="28756-153">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28756-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28756-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28756-154">Minimum supported server</span></span><br/> | <span data-ttu-id="28756-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28756-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28756-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28756-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="28756-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="28756-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="28756-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28756-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="28756-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28756-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="28756-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28756-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28756-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28756-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28756-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="28756-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28756-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="28756-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="28756-164">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="28756-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="28756-165">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="28756-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="28756-166">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="28756-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="28756-167">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="28756-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="28756-168">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="28756-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="28756-169">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="28756-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="28756-170">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="28756-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





