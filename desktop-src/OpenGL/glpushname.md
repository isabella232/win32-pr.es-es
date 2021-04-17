---
title: función glPushName (GL. h)
description: Las funciones glPushName y glPopName envían y extraen la pila de nombres. | función glPushName (GL. h)
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName (función) OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689777"
---
# <a name="glpushname-function"></a><span data-ttu-id="65813-105">glPushName función)</span><span class="sxs-lookup"><span data-stu-id="65813-105">glPushName function</span></span>

<span data-ttu-id="65813-106">Las funciones **glPushName** y [**glPopName**](glpopname.md) envían y extraen la pila de nombres.</span><span class="sxs-lookup"><span data-stu-id="65813-106">The **glPushName** and [**glPopName**](glpopname.md) functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="65813-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65813-107">Syntax</span></span>


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="65813-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65813-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65813-109">*name*</span><span class="sxs-lookup"><span data-stu-id="65813-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="65813-110">Nombre que se va A insertar en la pila de nombres.</span><span class="sxs-lookup"><span data-stu-id="65813-110">A name that will be pushed onto the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65813-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65813-111">Return value</span></span>

<span data-ttu-id="65813-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="65813-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65813-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="65813-113">Error codes</span></span>

<span data-ttu-id="65813-114">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="65813-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="65813-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="65813-115">Name</span></span>                                                                                                  | <span data-ttu-id="65813-116">Significado</span><span class="sxs-lookup"><span data-stu-id="65813-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65813-117"><dt>**desbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="65813-117"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="65813-118">Se llamó a la función mientras la pila de matriz actual estaba llena.</span><span class="sxs-lookup"><span data-stu-id="65813-118">The function was called while the current matrix stack was full.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="65813-119"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="65813-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="65813-120">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="65813-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65813-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65813-121">Remarks</span></span>

<span data-ttu-id="65813-122">La función **glPushName** hace que el nombre se inserte en la pila de nombres, que inicialmente está vacía.</span><span class="sxs-lookup"><span data-stu-id="65813-122">The **glPushName** function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="65813-123">La función [**glPopName**](glpopname.md) extrae un nombre de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="65813-123">The [**glPopName**](glpopname.md) function pops one name off the top of the stack.</span></span> <span data-ttu-id="65813-124">La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="65813-124">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="65813-125">Consta de un conjunto ordenado de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="65813-125">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="65813-126">La pila de nombres está siempre vacía mientras que el modo de representación no es de selección de libro \_ .</span><span class="sxs-lookup"><span data-stu-id="65813-126">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="65813-127">Se omiten las llamadas a **glPushName** o [**glPopName**](glpopname.md) mientras que el modo de representación no es Select de GL \_ .</span><span class="sxs-lookup"><span data-stu-id="65813-127">Calls to **glPushName** or [**glPopName**](glpopname.md) while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="65813-128">Las siguientes funciones recuperan información relacionada con **glPushName** y [**glPopName**](glpopname.md):</span><span class="sxs-lookup"><span data-stu-id="65813-128">The following functions retrieve information related to **glPushName** and [**glPopName**](glpopname.md):</span></span>

<span data-ttu-id="65813-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="65813-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="65813-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento LM \_ Max \_ name \_ stack \_ Depth</span><span class="sxs-lookup"><span data-stu-id="65813-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="65813-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65813-131">Requirements</span></span>



| <span data-ttu-id="65813-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="65813-132">Requirement</span></span> | <span data-ttu-id="65813-133">Value</span><span class="sxs-lookup"><span data-stu-id="65813-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65813-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65813-134">Minimum supported client</span></span><br/> | <span data-ttu-id="65813-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="65813-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65813-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65813-136">Minimum supported server</span></span><br/> | <span data-ttu-id="65813-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65813-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65813-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65813-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="65813-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="65813-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="65813-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65813-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="65813-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65813-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65813-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65813-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65813-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65813-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65813-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="65813-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65813-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="65813-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="65813-146">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="65813-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="65813-147">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="65813-147">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="65813-148">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="65813-148">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="65813-149">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="65813-149">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="65813-150">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="65813-150">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





