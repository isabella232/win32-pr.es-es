---
title: función glVertex4d (GL. h)
description: Especifica un vértice. | función glVertex4d (GL. h)
ms.assetid: d9203e4f-5ed2-41e7-b619-65cee3132ed9
keywords:
- glVertex4d (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex4d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a28a64c35ff30cc668839899dca4f3dc2958ff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670206"
---
# <a name="glvertex4d-function"></a><span data-ttu-id="33577-105">glVertex4d función)</span><span class="sxs-lookup"><span data-stu-id="33577-105">glVertex4d function</span></span>

<span data-ttu-id="33577-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="33577-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="33577-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33577-107">Syntax</span></span>


```C++
void WINAPI glVertex4d(
   GLdouble x,
   GLdouble y,
   GLdouble z,
   GLdouble w
);
```



## <a name="parameters"></a><span data-ttu-id="33577-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33577-109">*x*</span><span class="sxs-lookup"><span data-stu-id="33577-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="33577-110">Especifica la coordenada x de un vértice.</span><span class="sxs-lookup"><span data-stu-id="33577-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="33577-111">*y*</span><span class="sxs-lookup"><span data-stu-id="33577-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="33577-112">Especifica la coordenada y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="33577-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="33577-113">*z*</span><span class="sxs-lookup"><span data-stu-id="33577-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="33577-114">Especifica la coordenada z de un vértice.</span><span class="sxs-lookup"><span data-stu-id="33577-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="33577-115">*w*</span><span class="sxs-lookup"><span data-stu-id="33577-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="33577-116">Especifica la coordenada w de un vértice.</span><span class="sxs-lookup"><span data-stu-id="33577-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33577-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33577-117">Return value</span></span>

<span data-ttu-id="33577-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="33577-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33577-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33577-119">Remarks</span></span>

<span data-ttu-id="33577-120">Los comandos de la función glVertex se usan en pares de [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="33577-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="33577-121">Las coordenadas color, normal y Texture actuales están asociadas al vértice cuando se llama a glVertex.</span><span class="sxs-lookup"><span data-stu-id="33577-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="33577-122">Cuando solo se especifican *x* *e y,* *z* tiene como valor predeterminado 0,0 y *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="33577-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="33577-123">Cuando se especifican *x*, *y* y *z* , el valor predeterminado de *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="33577-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="33577-124">La invocación de glVertex fuera de un par glEnd de **glBegin** /  produce un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="33577-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="33577-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33577-125">Requirements</span></span>



| <span data-ttu-id="33577-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="33577-126">Requirement</span></span> | <span data-ttu-id="33577-127">Value</span><span class="sxs-lookup"><span data-stu-id="33577-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33577-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33577-128">Minimum supported client</span></span><br/> | <span data-ttu-id="33577-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="33577-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="33577-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33577-130">Minimum supported server</span></span><br/> | <span data-ttu-id="33577-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="33577-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33577-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="33577-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="33577-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="33577-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="33577-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33577-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="33577-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33577-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="33577-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33577-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33577-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33577-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33577-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="33577-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33577-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="33577-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="33577-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="33577-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="33577-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="33577-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="33577-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="33577-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="33577-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="33577-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="33577-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="33577-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="33577-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="33577-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="33577-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="33577-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





