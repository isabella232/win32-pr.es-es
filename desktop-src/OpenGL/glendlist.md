---
title: función glEndList (GL. h)
description: Las funciones glNewList y glEndList crean o reemplazan una lista de visualización. | función glEndList (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- glEndList (función) OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689804"
---
# <a name="glendlist-function"></a><span data-ttu-id="39bb5-105">glEndList función)</span><span class="sxs-lookup"><span data-stu-id="39bb5-105">glEndList function</span></span>

<span data-ttu-id="39bb5-106">Las funciones [**glNewList**](glnewlist.md) y **glEndList** crean o reemplazan una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="39bb5-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="39bb5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39bb5-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="39bb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39bb5-108">Parameters</span></span>

<span data-ttu-id="39bb5-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="39bb5-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39bb5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39bb5-110">Return value</span></span>

<span data-ttu-id="39bb5-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="39bb5-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39bb5-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="39bb5-112">Error codes</span></span>

<span data-ttu-id="39bb5-113">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="39bb5-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="39bb5-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="39bb5-114">Name</span></span>                                                                                                  | <span data-ttu-id="39bb5-115">Significado</span><span class="sxs-lookup"><span data-stu-id="39bb5-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39bb5-116"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="39bb5-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="39bb5-117">se llamó a **glEndList** sin un **glNewList** anterior, o si se llamó a **glNewList** mientras se estaba definiendo una lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="39bb5-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="39bb5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39bb5-118">Remarks</span></span>

<span data-ttu-id="39bb5-119">Las listas de visualización son grupos de comandos OpenGL que se han almacenado para su posterior ejecución.</span><span class="sxs-lookup"><span data-stu-id="39bb5-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="39bb5-120">Las listas de visualización se crean con [**glNewList**](glnewlist.md).</span><span class="sxs-lookup"><span data-stu-id="39bb5-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="39bb5-121">Todos los comandos subsiguientes se colocan en la lista de visualización, en el orden emitido, hasta que se llame a **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="39bb5-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="39bb5-122">La función [**glNewList**](glnewlist.md) tiene dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="39bb5-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="39bb5-123">El primer parámetro, *List*, es un entero positivo que se convierte en el nombre único de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="39bb5-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="39bb5-124">Los nombres se pueden crear y reservar con [**glGenLists**](glgenlists.md) y probar la unicidad con [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="39bb5-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="39bb5-125">El segundo parámetro, *mode*, es una constante simbólica que puede suponer uno de los dos valores anteriores.</span><span class="sxs-lookup"><span data-stu-id="39bb5-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="39bb5-126">Algunos comandos no se compilan en la lista de visualización, pero se ejecutan inmediatamente, independientemente del modo de la lista de visualización.</span><span class="sxs-lookup"><span data-stu-id="39bb5-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="39bb5-127">Estos comandos son [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**GlIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)y todas las rutinas de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="39bb5-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="39bb5-128">De forma similar, [**glTexImage2D**](glteximage2d.md) y [**glTexImage1D**](glteximage1d.md) se ejecutan inmediatamente y no se compilan en la lista de visualización cuando su primer argumento es la textura de proxy \_ de contabilidad \_ \_ 2D o la \_ \_ textura de proxy de GL \_ 1D, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="39bb5-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="39bb5-129">Cuando se encuentra la función **glEndList** , la definición de la lista de visualización se completa mediante la Asociación de la lista con la *lista* de nombres únicos (especificada en el comando [**glNewList**](glnewlist.md) ).</span><span class="sxs-lookup"><span data-stu-id="39bb5-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="39bb5-130">Si ya existe una lista de visualización con la *lista* de nombres, solo se reemplaza cuando se llama a **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="39bb5-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="39bb5-131">Las funciones [**glCallList**](glcalllist.md) y [**glCallLists**](glcalllists.md) se pueden especificar en las listas de visualización.</span><span class="sxs-lookup"><span data-stu-id="39bb5-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="39bb5-132">Los comandos de la lista de visualización o las listas ejecutadas por **glCallList** o **glCallLists** no se incluyen en la lista de visualización que se está creando, incluso si el modo de creación de lista es GL \_ compile \_ y \_ Execute.</span><span class="sxs-lookup"><span data-stu-id="39bb5-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="39bb5-133">La siguiente función recupera información relacionada con [**glNewList**](glnewlist.md):</span><span class="sxs-lookup"><span data-stu-id="39bb5-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="39bb5-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="39bb5-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="39bb5-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39bb5-135">Requirements</span></span>



| <span data-ttu-id="39bb5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="39bb5-136">Requirement</span></span> | <span data-ttu-id="39bb5-137">Value</span><span class="sxs-lookup"><span data-stu-id="39bb5-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39bb5-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39bb5-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39bb5-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="39bb5-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="39bb5-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39bb5-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39bb5-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="39bb5-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39bb5-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39bb5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="39bb5-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="39bb5-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="39bb5-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39bb5-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="39bb5-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39bb5-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="39bb5-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39bb5-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39bb5-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39bb5-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39bb5-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="39bb5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bb5-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="39bb5-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="39bb5-150">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="39bb5-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="39bb5-151">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="39bb5-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="39bb5-152">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="39bb5-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="39bb5-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="39bb5-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="39bb5-154">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="39bb5-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="39bb5-155">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="39bb5-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="39bb5-156">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="39bb5-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





