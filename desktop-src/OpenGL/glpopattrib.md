---
title: función glPopAttrib (GL. h)
description: Extrae la pila de atributos.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- glPopAttrib (función) OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666023"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="2585b-104">glPopAttrib función)</span><span class="sxs-lookup"><span data-stu-id="2585b-104">glPopAttrib function</span></span>

<span data-ttu-id="2585b-105">Extrae la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="2585b-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="2585b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2585b-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="2585b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2585b-107">Parameters</span></span>

<span data-ttu-id="2585b-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2585b-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2585b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2585b-109">Return value</span></span>

<span data-ttu-id="2585b-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2585b-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2585b-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2585b-111">Error codes</span></span>

<span data-ttu-id="2585b-112">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="2585b-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2585b-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="2585b-113">Name</span></span>                                                                                                  | <span data-ttu-id="2585b-114">Significado</span><span class="sxs-lookup"><span data-stu-id="2585b-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2585b-115"><dt>**subdesbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585b-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="2585b-116">Se llamó a la función mientras la pila de atributos estaba vacía.</span><span class="sxs-lookup"><span data-stu-id="2585b-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="2585b-117"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2585b-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2585b-118">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2585b-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2585b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2585b-119">Remarks</span></span>

<span data-ttu-id="2585b-120">La función [**glPushAttrib**](glpushattrib.md) toma un argumento, una máscara que indica los grupos de variables de estado que se van a guardar en la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="2585b-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="2585b-121">Las constantes simbólicas se utilizan para establecer bits en la máscara.</span><span class="sxs-lookup"><span data-stu-id="2585b-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="2585b-122">Normalmente, el parámetro Mask se construye **mediante la** combinación de varias de estas constantes.</span><span class="sxs-lookup"><span data-stu-id="2585b-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="2585b-123">La máscara especial GL \_ todos \_ los \_ bits attrib se pueden usar para guardar todos los Estados apilables.</span><span class="sxs-lookup"><span data-stu-id="2585b-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="2585b-124">La función **glPopAttrib** restaura los valores de las variables de estado guardadas con el último comando [**glPushAttrib**](glpushattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="2585b-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="2585b-125">Los que no se han guardado permanecen inalterados.</span><span class="sxs-lookup"><span data-stu-id="2585b-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="2585b-126">Es un error insertar atributos en una pila completa o desactivar los atributos de una pila vacía.</span><span class="sxs-lookup"><span data-stu-id="2585b-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="2585b-127">En cualquier caso, se establece la marca de error y no se realiza ningún otro cambio en el estado de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2585b-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="2585b-128">Inicialmente, la pila de atributos está vacía.</span><span class="sxs-lookup"><span data-stu-id="2585b-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="2585b-129">No todos los valores del estado de OpenGL se pueden guardar en la pila de atributos.</span><span class="sxs-lookup"><span data-stu-id="2585b-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="2585b-130">Por ejemplo, el estado del paquete de píxeles y desempaquetado, el estado del modo de representación y el estado de selección y de comentarios no se pueden guardar.</span><span class="sxs-lookup"><span data-stu-id="2585b-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="2585b-131">La profundidad de la pila de atributos depende de la implementación, pero debe ser al menos 16.</span><span class="sxs-lookup"><span data-stu-id="2585b-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="2585b-132">Las siguientes funciones recuperan información relacionada con [**glPushAttrib**](glpushattrib.md) y **glPopAttrib**:</span><span class="sxs-lookup"><span data-stu-id="2585b-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="2585b-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ pila de atrib \_ \_</span><span class="sxs-lookup"><span data-stu-id="2585b-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="2585b-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ profundidad máxima de la pila de Max \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="2585b-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="2585b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2585b-135">Requirements</span></span>



| <span data-ttu-id="2585b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2585b-136">Requirement</span></span> | <span data-ttu-id="2585b-137">Value</span><span class="sxs-lookup"><span data-stu-id="2585b-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2585b-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2585b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2585b-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2585b-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2585b-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2585b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2585b-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2585b-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2585b-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2585b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2585b-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2585b-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2585b-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2585b-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="2585b-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2585b-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2585b-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2585b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2585b-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2585b-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2585b-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="2585b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2585b-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2585b-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2585b-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2585b-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2585b-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="2585b-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2585b-152">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="2585b-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="2585b-153">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="2585b-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="2585b-154">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="2585b-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="2585b-155">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="2585b-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="2585b-156">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="2585b-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="2585b-157">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="2585b-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="2585b-158">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="2585b-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="2585b-159">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="2585b-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="2585b-160">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="2585b-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="2585b-161">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="2585b-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="2585b-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="2585b-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="2585b-163">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="2585b-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="2585b-164">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2585b-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="2585b-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2585b-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





