---
title: función glVertex3f (GL. h)
description: Especifica un vértice. | función glVertex3f (GL. h)
ms.assetid: 9833ef82-1ac8-45d4-b3e0-9c06cb07862d
keywords:
- glVertex3f (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex3f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b891b4d982d41fa61fa2eccc341979d181635e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670121"
---
# <a name="glvertex3f-function"></a><span data-ttu-id="836ff-105">glVertex3f función)</span><span class="sxs-lookup"><span data-stu-id="836ff-105">glVertex3f function</span></span>

<span data-ttu-id="836ff-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="836ff-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="836ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="836ff-107">Syntax</span></span>


```C++
void WINAPI glVertex3f(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="836ff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="836ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836ff-109">*x*</span><span class="sxs-lookup"><span data-stu-id="836ff-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="836ff-110">Especifica la coordenada x de un vértice.</span><span class="sxs-lookup"><span data-stu-id="836ff-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="836ff-111">*y*</span><span class="sxs-lookup"><span data-stu-id="836ff-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="836ff-112">Especifica la coordenada y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="836ff-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="836ff-113">*z*</span><span class="sxs-lookup"><span data-stu-id="836ff-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="836ff-114">Especifica la coordenada z de un vértice.</span><span class="sxs-lookup"><span data-stu-id="836ff-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836ff-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="836ff-115">Return value</span></span>

<span data-ttu-id="836ff-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="836ff-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="836ff-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="836ff-117">Remarks</span></span>

<span data-ttu-id="836ff-118">Los comandos de la función glVertex se usan en pares de [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="836ff-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="836ff-119">Las coordenadas color, normal y Texture actuales están asociadas al vértice cuando se llama a glVertex.</span><span class="sxs-lookup"><span data-stu-id="836ff-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="836ff-120">Cuando solo se especifican *x* *e y,* *z* tiene como valor predeterminado 0,0 y *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="836ff-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="836ff-121">Cuando se especifican *x*, *y* y *z* , el valor predeterminado de *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="836ff-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="836ff-122">La invocación de glVertex fuera de un par glEnd de **glBegin** /  produce un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="836ff-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="836ff-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="836ff-123">Requirements</span></span>



| <span data-ttu-id="836ff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="836ff-124">Requirement</span></span> | <span data-ttu-id="836ff-125">Value</span><span class="sxs-lookup"><span data-stu-id="836ff-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="836ff-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="836ff-126">Minimum supported client</span></span><br/> | <span data-ttu-id="836ff-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="836ff-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="836ff-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="836ff-128">Minimum supported server</span></span><br/> | <span data-ttu-id="836ff-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="836ff-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="836ff-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="836ff-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="836ff-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="836ff-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="836ff-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="836ff-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="836ff-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="836ff-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="836ff-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="836ff-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="836ff-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="836ff-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836ff-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="836ff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836ff-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="836ff-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="836ff-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="836ff-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="836ff-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="836ff-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="836ff-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="836ff-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="836ff-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="836ff-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="836ff-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="836ff-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="836ff-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="836ff-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="836ff-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="836ff-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





