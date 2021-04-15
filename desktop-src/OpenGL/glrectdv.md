---
title: función glRectdv (GL. h)
description: La función glRectdv dibuja un rectángulo.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- glRectdv (función) OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421938"
---
# <a name="glrectdv-function"></a><span data-ttu-id="371a9-104">glRectdv función)</span><span class="sxs-lookup"><span data-stu-id="371a9-104">glRectdv function</span></span>

<span data-ttu-id="371a9-105">La función **glRectdv** dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="371a9-105">The **glRectdv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="371a9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="371a9-106">Syntax</span></span>


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a><span data-ttu-id="371a9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="371a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="371a9-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="371a9-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="371a9-109">Puntero a un vértice de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="371a9-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="371a9-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="371a9-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="371a9-111">puntero al vértice opuesto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="371a9-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="371a9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="371a9-112">Return value</span></span>

<span data-ttu-id="371a9-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="371a9-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="371a9-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="371a9-114">Error codes</span></span>

<span data-ttu-id="371a9-115">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="371a9-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="371a9-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="371a9-116">Name</span></span>                                                                                                  | <span data-ttu-id="371a9-117">Significado</span><span class="sxs-lookup"><span data-stu-id="371a9-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="371a9-118"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="371a9-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="371a9-119">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="371a9-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="371a9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="371a9-120">Remarks</span></span>

<span data-ttu-id="371a9-121">La función **glRectd** admite la especificación eficaz de rectángulos como dos puntos de vértice.</span><span class="sxs-lookup"><span data-stu-id="371a9-121">The **glRectd** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="371a9-122">Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas (*x*, *y*), o como dos punteros a matrices, cada una con un par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="371a9-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="371a9-123">El rectángulo resultante se define en el plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="371a9-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="371a9-124">La función **glRectd**(*x1,* *Y1,* *x2,* *Y2*) es exactamente equivalente a la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="371a9-124">The **glRectd**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="371a9-125">**glBegin**(GL, \_ polígono);</span><span class="sxs-lookup"><span data-stu-id="371a9-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="371a9-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="371a9-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="371a9-127">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="371a9-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="371a9-128">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="371a9-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="371a9-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="371a9-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="371a9-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="371a9-130">**glEnd**( );</span></span>

<span data-ttu-id="371a9-131">Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con un bobinado en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="371a9-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="371a9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="371a9-132">Requirements</span></span>



| <span data-ttu-id="371a9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="371a9-133">Requirement</span></span> | <span data-ttu-id="371a9-134">Value</span><span class="sxs-lookup"><span data-stu-id="371a9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="371a9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="371a9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="371a9-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="371a9-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="371a9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="371a9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="371a9-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="371a9-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="371a9-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="371a9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="371a9-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="371a9-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="371a9-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="371a9-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="371a9-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="371a9-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="371a9-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="371a9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="371a9-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="371a9-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="371a9-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="371a9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371a9-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="371a9-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="371a9-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="371a9-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="371a9-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="371a9-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





