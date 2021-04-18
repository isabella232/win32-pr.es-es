---
title: función glFinish (GL. h)
description: La función glFinish se bloquea hasta que se completa la ejecución de OpenGL.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- glFinish (función) OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535517"
---
# <a name="glfinish-function"></a><span data-ttu-id="bb299-104">glFinish función)</span><span class="sxs-lookup"><span data-stu-id="bb299-104">glFinish function</span></span>

<span data-ttu-id="bb299-105">La función **glFinish** se bloquea hasta que se completa la ejecución de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="bb299-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb299-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb299-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="bb299-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb299-107">Parameters</span></span>

<span data-ttu-id="bb299-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bb299-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb299-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb299-109">Return value</span></span>

<span data-ttu-id="bb299-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bb299-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb299-111">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bb299-111">Error codes</span></span>

<span data-ttu-id="bb299-112">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="bb299-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bb299-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb299-113">Name</span></span>                                                                                                  | <span data-ttu-id="bb299-114">Significado</span><span class="sxs-lookup"><span data-stu-id="bb299-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb299-115"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb299-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bb299-116">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bb299-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bb299-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb299-117">Remarks</span></span>

<span data-ttu-id="bb299-118">La función **glFinish** no devuelve ningún resultado hasta que se completen los efectos de todas las funciones OpenGL llamadas previamente.</span><span class="sxs-lookup"><span data-stu-id="bb299-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="bb299-119">Estos efectos incluyen todos los cambios en el estado de OpenGL, todos los cambios en el estado de conexión y todos los cambios realizados en el contenido de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="bb299-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="bb299-120">La función **glFinish** requiere un recorrido de ida y vuelta al servidor.</span><span class="sxs-lookup"><span data-stu-id="bb299-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb299-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb299-121">Requirements</span></span>



| <span data-ttu-id="bb299-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb299-122">Requirement</span></span> | <span data-ttu-id="bb299-123">Value</span><span class="sxs-lookup"><span data-stu-id="bb299-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb299-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb299-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb299-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bb299-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bb299-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb299-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb299-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb299-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb299-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb299-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb299-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb299-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bb299-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb299-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb299-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb299-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb299-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb299-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb299-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb299-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb299-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb299-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb299-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bb299-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bb299-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bb299-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bb299-137">**glFlush**</span><span class="sxs-lookup"><span data-stu-id="bb299-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





