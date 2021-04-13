---
title: función glRectfv (GL. h)
description: La función glRectfv dibuja un rectángulo.
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- glRectfv (función) OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871cd3edc44598ba66fb686d9957af7322d77730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421937"
---
# <a name="glrectfv-function"></a><span data-ttu-id="fc0fa-104">glRectfv función)</span><span class="sxs-lookup"><span data-stu-id="fc0fa-104">glRectfv function</span></span>

<span data-ttu-id="fc0fa-105">La función [**glRectfv**](glrectdv.md) dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-105">The [**glRectfv**](glrectdv.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0fa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc0fa-106">Syntax</span></span>


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
);
```



## <a name="parameters"></a><span data-ttu-id="fc0fa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc0fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc0fa-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="fc0fa-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="fc0fa-109">Puntero a un vértice de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="fc0fa-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="fc0fa-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="fc0fa-111">puntero al vértice opuesto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc0fa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc0fa-112">Return value</span></span>

<span data-ttu-id="fc0fa-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fc0fa-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fc0fa-114">Error codes</span></span>

<span data-ttu-id="fc0fa-115">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fc0fa-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc0fa-116">Name</span></span>                                                                                                  | <span data-ttu-id="fc0fa-117">Significado</span><span class="sxs-lookup"><span data-stu-id="fc0fa-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fc0fa-118"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fc0fa-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fc0fa-119">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fc0fa-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fc0fa-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc0fa-120">Remarks</span></span>

<span data-ttu-id="fc0fa-121">La función **glRectf** admite la especificación eficaz de rectángulos como dos puntos de vértice.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-121">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="fc0fa-122">Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas (*x*, *y*), o como dos punteros a matrices, cada una con un par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="fc0fa-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="fc0fa-123">El rectángulo resultante se define en el plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="fc0fa-124">La función **glRectf**(*x1,* *Y1,* *x2,* *Y2*) es exactamente equivalente a la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc0fa-124">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="fc0fa-125">**glBegin**(GL, \_ polígono);</span><span class="sxs-lookup"><span data-stu-id="fc0fa-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="fc0fa-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="fc0fa-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="fc0fa-127">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="fc0fa-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="fc0fa-128">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="fc0fa-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="fc0fa-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="fc0fa-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="fc0fa-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="fc0fa-130">**glEnd**( );</span></span>

<span data-ttu-id="fc0fa-131">Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con un bobinado en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="fc0fa-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc0fa-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc0fa-132">Requirements</span></span>



| <span data-ttu-id="fc0fa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc0fa-133">Requirement</span></span> | <span data-ttu-id="fc0fa-134">Value</span><span class="sxs-lookup"><span data-stu-id="fc0fa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0fa-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc0fa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fc0fa-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fc0fa-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fc0fa-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc0fa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fc0fa-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc0fa-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc0fa-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc0fa-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc0fa-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc0fa-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fc0fa-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc0fa-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc0fa-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc0fa-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc0fa-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc0fa-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc0fa-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc0fa-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc0fa-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc0fa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0fa-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fc0fa-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fc0fa-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fc0fa-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fc0fa-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="fc0fa-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





