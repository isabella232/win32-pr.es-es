---
title: función glRectsv (GL. h)
description: La función glRectsv dibuja un rectángulo.
ms.assetid: 0f7dc4fc-b6ce-4240-89d9-69f54c0c9f2b
keywords:
- glRectsv (función) OpenGL
topic_type:
- apiref
api_name:
- glRectsv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bdf6ce7d882db9c7cc1f78deddc3ca651a2c6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493150"
---
# <a name="glrectsv-function"></a><span data-ttu-id="aabe6-104">glRectsv función)</span><span class="sxs-lookup"><span data-stu-id="aabe6-104">glRectsv function</span></span>

<span data-ttu-id="aabe6-105">La función **glRectsv** dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="aabe6-105">The **glRectsv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="aabe6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aabe6-106">Syntax</span></span>


```C++
void WINAPI glRectsv(
   const GLshort *v1,
   const GLshort *v2
);
```



## <a name="parameters"></a><span data-ttu-id="aabe6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aabe6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aabe6-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="aabe6-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="aabe6-109">Puntero a un vértice de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="aabe6-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="aabe6-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="aabe6-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="aabe6-111">puntero al vértice opuesto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="aabe6-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aabe6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aabe6-112">Return value</span></span>

<span data-ttu-id="aabe6-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aabe6-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aabe6-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="aabe6-114">Error codes</span></span>

<span data-ttu-id="aabe6-115">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="aabe6-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="aabe6-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="aabe6-116">Name</span></span>                                                                                                  | <span data-ttu-id="aabe6-117">Significado</span><span class="sxs-lookup"><span data-stu-id="aabe6-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aabe6-118"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aabe6-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="aabe6-119">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="aabe6-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="aabe6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aabe6-120">Remarks</span></span>

<span data-ttu-id="aabe6-121">La función **glRects** admite la especificación eficaz de rectángulos como dos puntos de vértice.</span><span class="sxs-lookup"><span data-stu-id="aabe6-121">The **glRects** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="aabe6-122">Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas (*x*, *y*), o como dos punteros a matrices, cada una con un par (*x,* *y*).</span><span class="sxs-lookup"><span data-stu-id="aabe6-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x,* *y*) pair.</span></span> <span data-ttu-id="aabe6-123">El rectángulo resultante se define en el plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="aabe6-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="aabe6-124">La función **glRects**(*x1,* *Y1,* *x2,* *Y2*) es exactamente equivalente a la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="aabe6-124">The **glRects**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="aabe6-125">**glBegin**(GL, \_ polígono);</span><span class="sxs-lookup"><span data-stu-id="aabe6-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="aabe6-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="aabe6-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="aabe6-127">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="aabe6-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="aabe6-128">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="aabe6-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="aabe6-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="aabe6-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="aabe6-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="aabe6-130">**glEnd**( );</span></span>

<span data-ttu-id="aabe6-131">Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con un bobinado en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="aabe6-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="aabe6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aabe6-132">Requirements</span></span>



| <span data-ttu-id="aabe6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aabe6-133">Requirement</span></span> | <span data-ttu-id="aabe6-134">Value</span><span class="sxs-lookup"><span data-stu-id="aabe6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aabe6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aabe6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aabe6-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aabe6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aabe6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aabe6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aabe6-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aabe6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aabe6-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aabe6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="aabe6-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aabe6-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aabe6-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aabe6-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="aabe6-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aabe6-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aabe6-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aabe6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aabe6-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aabe6-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aabe6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="aabe6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aabe6-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aabe6-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aabe6-147">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="aabe6-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aabe6-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="aabe6-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





