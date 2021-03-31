---
title: función glInitNames (GL. h)
description: La función glInitNames inicializa la pila de nombres.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glInitNames (función) OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149925"
---
# <a name="glinitnames-function"></a><span data-ttu-id="23fa9-104">glInitNames función)</span><span class="sxs-lookup"><span data-stu-id="23fa9-104">glInitNames function</span></span>

<span data-ttu-id="23fa9-105">La función **glInitNames** inicializa la pila de nombres.</span><span class="sxs-lookup"><span data-stu-id="23fa9-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fa9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23fa9-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="23fa9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23fa9-107">Parameters</span></span>

<span data-ttu-id="23fa9-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="23fa9-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="23fa9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23fa9-109">Return value</span></span>

<span data-ttu-id="23fa9-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="23fa9-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23fa9-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="23fa9-111">Error codes</span></span>

<span data-ttu-id="23fa9-112">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="23fa9-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="23fa9-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="23fa9-113">Name</span></span>                                                                                                  | <span data-ttu-id="23fa9-114">Significado</span><span class="sxs-lookup"><span data-stu-id="23fa9-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23fa9-115"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="23fa9-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="23fa9-116">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="23fa9-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="23fa9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23fa9-117">Remarks</span></span>

<span data-ttu-id="23fa9-118">La función **glInitNames** hace que la pila de nombres se inicialice en su estado vacío predeterminado.</span><span class="sxs-lookup"><span data-stu-id="23fa9-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="23fa9-119">La pila de nombres se usa durante el modo de selección para permitir que los conjuntos de comandos de representación se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="23fa9-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="23fa9-120">Consta de un conjunto ordenado de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="23fa9-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="23fa9-121">La pila de nombres está siempre vacía mientras que el modo de representación no es de selección de libro \_ .</span><span class="sxs-lookup"><span data-stu-id="23fa9-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="23fa9-122">Se omiten las llamadas a **glInitNames** mientras el modo de representación no sea Select de GL \_ .</span><span class="sxs-lookup"><span data-stu-id="23fa9-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="23fa9-123">Las siguientes funciones recuperan información relacionada con **glInitNames**:</span><span class="sxs-lookup"><span data-stu-id="23fa9-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="23fa9-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de profundidad de la pila de nombre del libro \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="23fa9-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="23fa9-125">**glGet** con el argumento LM \_ Max \_ name \_ stack \_ Depth</span><span class="sxs-lookup"><span data-stu-id="23fa9-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="23fa9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fa9-126">Requirements</span></span>



| <span data-ttu-id="23fa9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fa9-127">Requirement</span></span> | <span data-ttu-id="23fa9-128">Value</span><span class="sxs-lookup"><span data-stu-id="23fa9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23fa9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23fa9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="23fa9-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="23fa9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="23fa9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23fa9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="23fa9-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23fa9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23fa9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23fa9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fa9-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="23fa9-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="23fa9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23fa9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="23fa9-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23fa9-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="23fa9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23fa9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23fa9-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23fa9-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23fa9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="23fa9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fa9-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="23fa9-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="23fa9-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="23fa9-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="23fa9-142">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="23fa9-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="23fa9-143">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="23fa9-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="23fa9-144">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="23fa9-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="23fa9-145">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="23fa9-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





