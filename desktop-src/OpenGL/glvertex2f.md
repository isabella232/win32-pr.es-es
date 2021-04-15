---
title: función glVertex2f (GL. h)
description: Especifica un vértice. | función glVertex2f (GL. h)
ms.assetid: d351cdc1-efaa-4c06-96d9-c4ef613c64df
keywords:
- glVertex2f (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b2610b4d0498a5a623372ba5f28ee4feea7b40d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689756"
---
# <a name="glvertex2f-function"></a><span data-ttu-id="28d4c-105">glVertex2f función)</span><span class="sxs-lookup"><span data-stu-id="28d4c-105">glVertex2f function</span></span>

<span data-ttu-id="28d4c-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="28d4c-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d4c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28d4c-107">Syntax</span></span>


```C++
void WINAPI glVertex2f(
   GLfloat x,
   GLfloat y
);
```



## <a name="parameters"></a><span data-ttu-id="28d4c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28d4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28d4c-109">*x*</span><span class="sxs-lookup"><span data-stu-id="28d4c-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="28d4c-110">Especifica la coordenada x de un vértice.</span><span class="sxs-lookup"><span data-stu-id="28d4c-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="28d4c-111">*y*</span><span class="sxs-lookup"><span data-stu-id="28d4c-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="28d4c-112">Especifica la coordenada y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="28d4c-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28d4c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28d4c-113">Return value</span></span>

<span data-ttu-id="28d4c-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="28d4c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d4c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28d4c-115">Remarks</span></span>

<span data-ttu-id="28d4c-116">Los comandos de la función glVertex se usan en pares de [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="28d4c-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="28d4c-117">Las coordenadas color, normal y Texture actuales están asociadas al vértice cuando se llama a glVertex.</span><span class="sxs-lookup"><span data-stu-id="28d4c-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="28d4c-118">Cuando solo se especifican *x* *e y,* *z* tiene como valor predeterminado 0,0 y *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="28d4c-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="28d4c-119">Cuando se especifican *x*, *y* y *z* , el valor predeterminado de *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="28d4c-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="28d4c-120">La invocación de glVertex fuera de un par glEnd de **glBegin** /  produce un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="28d4c-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d4c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d4c-121">Requirements</span></span>



| <span data-ttu-id="28d4c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d4c-122">Requirement</span></span> | <span data-ttu-id="28d4c-123">Value</span><span class="sxs-lookup"><span data-stu-id="28d4c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28d4c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28d4c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="28d4c-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28d4c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28d4c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28d4c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="28d4c-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28d4c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28d4c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28d4c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="28d4c-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="28d4c-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="28d4c-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28d4c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="28d4c-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28d4c-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="28d4c-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28d4c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28d4c-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28d4c-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28d4c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="28d4c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d4c-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="28d4c-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="28d4c-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="28d4c-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="28d4c-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="28d4c-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="28d4c-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="28d4c-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="28d4c-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="28d4c-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="28d4c-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="28d4c-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="28d4c-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="28d4c-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="28d4c-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="28d4c-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





