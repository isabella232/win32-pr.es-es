---
title: función glVertex3s (GL. h)
description: Especifica un vértice. | función glVertex3s (GL. h)
ms.assetid: ee970440-3eb3-46d6-80d2-e23649585510
keywords:
- glVertex3s (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex3s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a167ded1510c0c5d9b430e59fb81b1625d5c199f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083659"
---
# <a name="glvertex3s-function"></a><span data-ttu-id="45be1-105">glVertex3s función)</span><span class="sxs-lookup"><span data-stu-id="45be1-105">glVertex3s function</span></span>

<span data-ttu-id="45be1-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="45be1-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="45be1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45be1-107">Syntax</span></span>


```C++
void WINAPI glVertex3s(
   GLshort x,
   GLshort y,
   GLshort z
);
```



## <a name="parameters"></a><span data-ttu-id="45be1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45be1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45be1-109">*x*</span><span class="sxs-lookup"><span data-stu-id="45be1-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="45be1-110">Especifica la coordenada x de un vértice.</span><span class="sxs-lookup"><span data-stu-id="45be1-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="45be1-111">*y*</span><span class="sxs-lookup"><span data-stu-id="45be1-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="45be1-112">Especifica la coordenada y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="45be1-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="45be1-113">*z*</span><span class="sxs-lookup"><span data-stu-id="45be1-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="45be1-114">Especifica la coordenada z de un vértice.</span><span class="sxs-lookup"><span data-stu-id="45be1-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45be1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45be1-115">Return value</span></span>

<span data-ttu-id="45be1-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="45be1-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45be1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45be1-117">Remarks</span></span>

<span data-ttu-id="45be1-118">Los comandos de la función glVertex se usan en pares de [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="45be1-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="45be1-119">Las coordenadas color, normal y Texture actuales están asociadas al vértice cuando se llama a glVertex.</span><span class="sxs-lookup"><span data-stu-id="45be1-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="45be1-120">Cuando solo se especifican *x* *e y,* *z* tiene como valor predeterminado 0,0 y *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="45be1-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="45be1-121">Cuando se especifican *x*, *y* y *z* , el valor predeterminado de *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="45be1-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="45be1-122">La invocación de glVertex fuera de un par glEnd de **glBegin** /  produce un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="45be1-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="45be1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45be1-123">Requirements</span></span>



| <span data-ttu-id="45be1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="45be1-124">Requirement</span></span> | <span data-ttu-id="45be1-125">Value</span><span class="sxs-lookup"><span data-stu-id="45be1-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45be1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45be1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45be1-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="45be1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="45be1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45be1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45be1-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45be1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45be1-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45be1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="45be1-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="45be1-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="45be1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45be1-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="45be1-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45be1-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="45be1-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45be1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45be1-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45be1-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45be1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="45be1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45be1-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="45be1-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="45be1-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="45be1-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="45be1-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="45be1-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="45be1-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="45be1-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="45be1-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="45be1-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="45be1-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="45be1-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="45be1-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="45be1-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="45be1-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="45be1-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





