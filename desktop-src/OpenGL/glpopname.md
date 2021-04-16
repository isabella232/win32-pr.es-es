---
title: función glPopName (GL. h)
description: Las funciones glPushName y glPopName envían y extraen la pila de nombres. | función glPopName (GL. h)
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glPopName (función) OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 830c4937b30cca64de3063b42ad16dd3adc87c89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689810"
---
# <a name="glpopname-function"></a><span data-ttu-id="26b20-105">glPopName función)</span><span class="sxs-lookup"><span data-stu-id="26b20-105">glPopName function</span></span>

<span data-ttu-id="26b20-106">Las funciones [**glPushName**](glpushname.md) y **glPopName** envían y extraen la pila de nombres.</span><span class="sxs-lookup"><span data-stu-id="26b20-106">The [**glPushName**](glpushname.md) and **glPopName** functions push and pop the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b20-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26b20-107">Syntax</span></span>


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a><span data-ttu-id="26b20-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26b20-108">Parameters</span></span>

<span data-ttu-id="26b20-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="26b20-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26b20-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26b20-110">Return value</span></span>

<span data-ttu-id="26b20-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="26b20-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="26b20-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="26b20-112">Error codes</span></span>

<span data-ttu-id="26b20-113">La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="26b20-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="26b20-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="26b20-114">Name</span></span>                                                                                                  | <span data-ttu-id="26b20-115">Significado</span><span class="sxs-lookup"><span data-stu-id="26b20-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26b20-116"><dt>**subdesbordamiento de la pila de GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26b20-116"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="26b20-117">Se llamó a la función mientras que la pila de matriz actual contenía solo una matriz única.</span><span class="sxs-lookup"><span data-stu-id="26b20-117">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="26b20-118"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="26b20-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="26b20-119">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="26b20-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="26b20-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26b20-120">Remarks</span></span>

<span data-ttu-id="26b20-121">La función [**glPushName**](glpushname.md) hace que el nombre se inserte en la pila de nombres, que inicialmente está vacía.</span><span class="sxs-lookup"><span data-stu-id="26b20-121">The [**glPushName**](glpushname.md) function causes name to be pushed onto the name stack, which is initially empty.</span></span> <span data-ttu-id="26b20-122">La función **glPopName** extrae un nombre de la parte superior de la pila.</span><span class="sxs-lookup"><span data-stu-id="26b20-122">The **glPopName** function pops one name off the top of the stack.</span></span> <span data-ttu-id="26b20-123">La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="26b20-123">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="26b20-124">Consta de un conjunto ordenado de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="26b20-124">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="26b20-125">La pila de nombres está siempre vacía mientras que el modo de representación no es de selección de libro \_ .</span><span class="sxs-lookup"><span data-stu-id="26b20-125">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="26b20-126">Se omiten las llamadas a [**glPushName**](glpushname.md) o **glPopName** mientras que el modo de representación no es Select de GL \_ .</span><span class="sxs-lookup"><span data-stu-id="26b20-126">Calls to [**glPushName**](glpushname.md) or **glPopName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="26b20-127">Las siguientes funciones recuperan información relacionada con [**glPushName**](glpushname.md) y **glPopName**:</span><span class="sxs-lookup"><span data-stu-id="26b20-127">The following functions retrieve information related to [**glPushName**](glpushname.md) and **glPopName**:</span></span>

<span data-ttu-id="26b20-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="26b20-128">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="26b20-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento LM \_ Max \_ name \_ stack \_ Depth</span><span class="sxs-lookup"><span data-stu-id="26b20-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="26b20-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26b20-130">Requirements</span></span>



| <span data-ttu-id="26b20-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b20-131">Requirement</span></span> | <span data-ttu-id="26b20-132">Value</span><span class="sxs-lookup"><span data-stu-id="26b20-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26b20-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26b20-133">Minimum supported client</span></span><br/> | <span data-ttu-id="26b20-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="26b20-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="26b20-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26b20-135">Minimum supported server</span></span><br/> | <span data-ttu-id="26b20-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="26b20-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="26b20-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26b20-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="26b20-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b20-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="26b20-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26b20-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="26b20-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26b20-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="26b20-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26b20-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26b20-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26b20-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b20-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="26b20-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b20-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="26b20-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="26b20-145">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="26b20-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="26b20-146">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="26b20-146">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="26b20-147">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="26b20-147">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="26b20-148">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="26b20-148">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="26b20-149">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="26b20-149">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





