---
title: función glRectf (GL. h)
description: La función glRectf dibuja un rectángulo.
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- glRectf (función) OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0c7036ae7395dce66d88f52c30631be801c4af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489143"
---
# <a name="glrectf-function"></a><span data-ttu-id="2ec92-104">glRectf función)</span><span class="sxs-lookup"><span data-stu-id="2ec92-104">glRectf function</span></span>

<span data-ttu-id="2ec92-105">La función [**glRectf**](glrectd.md) dibuja un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ec92-105">The [**glRectf**](glrectd.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ec92-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ec92-106">Syntax</span></span>


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a><span data-ttu-id="2ec92-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ec92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ec92-108">*x1*</span><span class="sxs-lookup"><span data-stu-id="2ec92-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="2ec92-109">Coordenada *x* del vértice de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ec92-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2ec92-110">*y1*</span><span class="sxs-lookup"><span data-stu-id="2ec92-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="2ec92-111">Coordenada *y* del vértice de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ec92-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2ec92-112">*RCA*</span><span class="sxs-lookup"><span data-stu-id="2ec92-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="2ec92-113">Coordenada *x* del vértice opuesto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ec92-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="2ec92-114">*a2*</span><span class="sxs-lookup"><span data-stu-id="2ec92-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="2ec92-115">Coordenada *y* del vértice opuesto del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="2ec92-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ec92-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ec92-116">Return value</span></span>

<span data-ttu-id="2ec92-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2ec92-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ec92-118">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2ec92-118">Error codes</span></span>

<span data-ttu-id="2ec92-119">La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="2ec92-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2ec92-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ec92-120">Name</span></span>                                                                                                  | <span data-ttu-id="2ec92-121">Significado</span><span class="sxs-lookup"><span data-stu-id="2ec92-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ec92-122"><dt>**\_operación no válida GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2ec92-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2ec92-123">Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2ec92-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2ec92-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ec92-124">Remarks</span></span>

<span data-ttu-id="2ec92-125">La función **glRectf** admite la especificación eficaz de rectángulos como dos puntos de vértice.</span><span class="sxs-lookup"><span data-stu-id="2ec92-125">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="2ec92-126">Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas (*x*, *y*), o como dos punteros a matrices, cada una con un par (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="2ec92-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="2ec92-127">El rectángulo resultante se define en el plano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="2ec92-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="2ec92-128">La función **glRectf**(*x1,* *Y1,* *x2,* *Y2*) es exactamente equivalente a la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="2ec92-128">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="2ec92-129">**glBegin**(GL, \_ polígono);</span><span class="sxs-lookup"><span data-stu-id="2ec92-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="2ec92-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="2ec92-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="2ec92-131">**glVertex2**( *x2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="2ec92-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="2ec92-132">**glVertex2**( *x2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="2ec92-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="2ec92-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="2ec92-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="2ec92-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="2ec92-134">**glEnd**( );</span></span>

<span data-ttu-id="2ec92-135">Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con un bobinado en sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="2ec92-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ec92-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ec92-136">Requirements</span></span>



| <span data-ttu-id="2ec92-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ec92-137">Requirement</span></span> | <span data-ttu-id="2ec92-138">Value</span><span class="sxs-lookup"><span data-stu-id="2ec92-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ec92-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ec92-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2ec92-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ec92-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2ec92-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ec92-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2ec92-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ec92-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ec92-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ec92-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ec92-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ec92-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2ec92-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ec92-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ec92-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ec92-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2ec92-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ec92-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ec92-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ec92-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ec92-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ec92-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ec92-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2ec92-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2ec92-151">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="2ec92-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2ec92-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="2ec92-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





