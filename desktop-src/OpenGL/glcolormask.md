---
title: función glColorMask (GL. h)
description: La función glColorMask habilita y deshabilita la escritura de componentes de color de búfer de fotogramas.
ms.assetid: 23d7f94e-f290-423c-a841-f86caf94009d
keywords:
- glColorMask (función) OpenGL
topic_type:
- apiref
api_name:
- glColorMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9aa36eeceeae4aaa9373d73b50fda09663edb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905096"
---
# <a name="glcolormask-function"></a><span data-ttu-id="8ec79-104">glColorMask función)</span><span class="sxs-lookup"><span data-stu-id="8ec79-104">glColorMask function</span></span>

<span data-ttu-id="8ec79-105">La función **glColorMask** habilita y deshabilita la escritura de componentes de color de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8ec79-105">The **glColorMask** function enables and disables writing of frame-buffer color components.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec79-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ec79-106">Syntax</span></span>


```C++
void WINAPI glColorMask(
   GLboolean red,
   GLboolean green,
   GLboolean blue,
   GLboolean alpha
);
```



## <a name="parameters"></a><span data-ttu-id="8ec79-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ec79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec79-108">*alerta*</span><span class="sxs-lookup"><span data-stu-id="8ec79-108">*red*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec79-109">Especifique si el rojo puede o no se puede escribir en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8ec79-109">Specify whether red can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="8ec79-110">Los valores predeterminados son GL \_ true, lo que indica que se puede escribir el componente de color.</span><span class="sxs-lookup"><span data-stu-id="8ec79-110">The default values is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="8ec79-111">*verde*</span><span class="sxs-lookup"><span data-stu-id="8ec79-111">*green*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec79-112">Especifique si el color verde puede o no se puede escribir en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8ec79-112">Specify whether green can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="8ec79-113">El valor predeterminado es GL \_ true, que indica que se puede escribir el componente de color.</span><span class="sxs-lookup"><span data-stu-id="8ec79-113">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="8ec79-114">*azul*</span><span class="sxs-lookup"><span data-stu-id="8ec79-114">*blue*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec79-115">Especifique si el azul puede o no se puede escribir en el fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8ec79-115">Specify whether blue can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="8ec79-116">El valor predeterminado es GL \_ true, que indica que se puede escribir el componente de color.</span><span class="sxs-lookup"><span data-stu-id="8ec79-116">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> <dt>

<span data-ttu-id="8ec79-117">*alpha*</span><span class="sxs-lookup"><span data-stu-id="8ec79-117">*alpha*</span></span> 
</dt> <dd>

<span data-ttu-id="8ec79-118">Especifique si alfa puede o no se puede escribir en fotogramas.</span><span class="sxs-lookup"><span data-stu-id="8ec79-118">Specify whether alpha can or cannot be written into the framebuffer.</span></span> <span data-ttu-id="8ec79-119">El valor predeterminado es GL \_ true, que indica que se puede escribir el componente de color.</span><span class="sxs-lookup"><span data-stu-id="8ec79-119">The default value is GL\_TRUE, indicating that the color component can be written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec79-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec79-120">Return value</span></span>

<span data-ttu-id="8ec79-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8ec79-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ec79-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8ec79-122">Error codes</span></span>

<span data-ttu-id="8ec79-123">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="8ec79-123">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8ec79-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ec79-124">Name</span></span>                                                                                                  | <span data-ttu-id="8ec79-125">Significado</span><span class="sxs-lookup"><span data-stu-id="8ec79-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ec79-126"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec79-126"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8ec79-127">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8ec79-127">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8ec79-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ec79-128">Remarks</span></span>

<span data-ttu-id="8ec79-129">La función **glColorMask** especifica si los componentes de color individuales de fotogramas se pueden o no se pueden escribir.</span><span class="sxs-lookup"><span data-stu-id="8ec79-129">The **glColorMask** function specifies whether the individual color components in the framebuffer can or cannot be written.</span></span> <span data-ttu-id="8ec79-130">Por ejemplo, si el valor de *rojo* es GL \_ false, no se realiza ningún cambio en el componente rojo de ningún píxel de ninguno de los búferes de color, independientemente de la operación de dibujo que se intente.</span><span class="sxs-lookup"><span data-stu-id="8ec79-130">If *red* is GL\_FALSE, for example, no change is made to the red component of any pixel in any of the color buffers, regardless of the drawing operation attempted.</span></span>

<span data-ttu-id="8ec79-131">No se pueden controlar los cambios en los distintos bits de los componentes.</span><span class="sxs-lookup"><span data-stu-id="8ec79-131">Changes to individual bits of components cannot be controlled.</span></span> <span data-ttu-id="8ec79-132">En su lugar, los cambios se habilitan o deshabilitan para los componentes de color completos.</span><span class="sxs-lookup"><span data-stu-id="8ec79-132">Rather, changes are either enabled or disabled for entire color components.</span></span>

<span data-ttu-id="8ec79-133">Las siguientes funciones recuperan información relacionada con **glColorMask**:</span><span class="sxs-lookup"><span data-stu-id="8ec79-133">The following functions retrieve information related to **glColorMask**:</span></span>

<span data-ttu-id="8ec79-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ color \_ WRITEMASK</span><span class="sxs-lookup"><span data-stu-id="8ec79-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_WRITEMASK</span></span>

<span data-ttu-id="8ec79-135">**glGet** con el argumento del \_ modo RGBA de GL \_</span><span class="sxs-lookup"><span data-stu-id="8ec79-135">**glGet** with argument GL\_RGBA\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec79-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec79-136">Requirements</span></span>



| <span data-ttu-id="8ec79-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec79-137">Requirement</span></span> | <span data-ttu-id="8ec79-138">Value</span><span class="sxs-lookup"><span data-stu-id="8ec79-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec79-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ec79-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec79-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8ec79-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8ec79-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ec79-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec79-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8ec79-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ec79-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ec79-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec79-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec79-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8ec79-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ec79-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ec79-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ec79-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ec79-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ec79-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ec79-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ec79-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec79-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ec79-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec79-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8ec79-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8ec79-151">**glColor**</span><span class="sxs-lookup"><span data-stu-id="8ec79-151">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="8ec79-152">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="8ec79-152">**glDepthMask**</span></span>](gldepthmask.md)
</dt> <dt>

[<span data-ttu-id="8ec79-153">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="8ec79-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8ec79-154">**glGet**</span><span class="sxs-lookup"><span data-stu-id="8ec79-154">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="8ec79-155">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="8ec79-155">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="8ec79-156">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="8ec79-156">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="8ec79-157">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="8ec79-157">**glStencilMask**</span></span>](glstencilmask.md)
</dt> </dl>

 

 





