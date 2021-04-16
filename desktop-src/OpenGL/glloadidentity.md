---
title: función glLoadIdentity (GL. h)
description: La función glLoadIdentity reemplaza la matriz actual por la matriz de identidad.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- glLoadIdentity (función) OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568075"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="f9cf4-104">glLoadIdentity función)</span><span class="sxs-lookup"><span data-stu-id="f9cf4-104">glLoadIdentity function</span></span>

<span data-ttu-id="f9cf4-105">La función **glLoadIdentity** reemplaza la matriz actual por la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9cf4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9cf4-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="f9cf4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9cf4-107">Parameters</span></span>

<span data-ttu-id="f9cf4-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9cf4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9cf4-109">Return value</span></span>

<span data-ttu-id="f9cf4-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9cf4-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f9cf4-111">Error codes</span></span>

<span data-ttu-id="f9cf4-112">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f9cf4-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9cf4-113">Name</span></span>                                                                                                  | <span data-ttu-id="f9cf4-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f9cf4-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9cf4-115"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9cf4-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f9cf4-116">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f9cf4-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f9cf4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9cf4-117">Remarks</span></span>

<span data-ttu-id="f9cf4-118">La función **glLoadIdentity** reemplaza la matriz actual por la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="f9cf4-119">Es semánticamente equivalente a llamar a [**glLoadMatrix**](glloadmatrix.md) con la siguiente matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![Diagrama que muestra la matriz de identidades a la que llama glLoadIdentity.](images/load01.png)

<span data-ttu-id="f9cf4-121">Sin embargo, en algunos casos, es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="f9cf4-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="f9cf4-122">Las siguientes funciones recuperan información relacionada con **glLoadIdentity**:</span><span class="sxs-lookup"><span data-stu-id="f9cf4-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="f9cf4-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de matriz de contabilidad de argumentos \_</span><span class="sxs-lookup"><span data-stu-id="f9cf4-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="f9cf4-124">**glGet** con el argumento \_ MODELVIEW \_ matriz de contabilidad</span><span class="sxs-lookup"><span data-stu-id="f9cf4-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="f9cf4-125">**glGet** con el argumento \_ matriz de proyección de contabilidad \_</span><span class="sxs-lookup"><span data-stu-id="f9cf4-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="f9cf4-126">**glGet** con el argumento \_ matriz de textura de GL \_</span><span class="sxs-lookup"><span data-stu-id="f9cf4-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="f9cf4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9cf4-127">Requirements</span></span>



| <span data-ttu-id="f9cf4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9cf4-128">Requirement</span></span> | <span data-ttu-id="f9cf4-129">Value</span><span class="sxs-lookup"><span data-stu-id="f9cf4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9cf4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9cf4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f9cf4-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f9cf4-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f9cf4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9cf4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f9cf4-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9cf4-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9cf4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9cf4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9cf4-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9cf4-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f9cf4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9cf4-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9cf4-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9cf4-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f9cf4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9cf4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9cf4-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9cf4-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9cf4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9cf4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9cf4-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f9cf4-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f9cf4-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f9cf4-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f9cf4-143">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="f9cf4-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="f9cf4-144">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="f9cf4-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="f9cf4-145">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="f9cf4-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="f9cf4-146">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="f9cf4-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





