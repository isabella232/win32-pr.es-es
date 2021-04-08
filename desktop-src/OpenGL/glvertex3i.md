---
title: función glVertex3i (GL. h)
description: Especifica un vértice. | función glVertex3i (GL. h)
ms.assetid: 5f757065-cbe9-401a-855b-f0a9308ae204
keywords:
- glVertex3i (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4e216c35a354daead228d6043d2129f6d30d400
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003558"
---
# <a name="glvertex3i-function"></a><span data-ttu-id="aa490-105">glVertex3i función)</span><span class="sxs-lookup"><span data-stu-id="aa490-105">glVertex3i function</span></span>

<span data-ttu-id="aa490-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="aa490-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa490-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa490-107">Syntax</span></span>


```C++
void WINAPI glVertex3i(
   GLint x,
   GLint y,
   GLint z
);
```



## <a name="parameters"></a><span data-ttu-id="aa490-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa490-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa490-109">*x*</span><span class="sxs-lookup"><span data-stu-id="aa490-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="aa490-110">Especifica la coordenada x de un vértice.</span><span class="sxs-lookup"><span data-stu-id="aa490-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="aa490-111">*y*</span><span class="sxs-lookup"><span data-stu-id="aa490-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="aa490-112">Especifica la coordenada y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="aa490-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="aa490-113">*z*</span><span class="sxs-lookup"><span data-stu-id="aa490-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="aa490-114">Especifica la coordenada z de un vértice.</span><span class="sxs-lookup"><span data-stu-id="aa490-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa490-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa490-115">Return value</span></span>

<span data-ttu-id="aa490-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aa490-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa490-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa490-117">Remarks</span></span>

<span data-ttu-id="aa490-118">Los comandos de la función glVertex se usan en pares de [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="aa490-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="aa490-119">Las coordenadas color, normal y Texture actuales están asociadas al vértice cuando se llama a glVertex.</span><span class="sxs-lookup"><span data-stu-id="aa490-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="aa490-120">Cuando solo se especifican *x* *e y,* *z* tiene como valor predeterminado 0,0 y *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="aa490-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="aa490-121">Cuando se especifican *x*, *y* y *z* , el valor predeterminado de *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="aa490-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="aa490-122">La invocación de glVertex fuera de un par glEnd de **glBegin** /  produce un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="aa490-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa490-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa490-123">Requirements</span></span>



| <span data-ttu-id="aa490-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa490-124">Requirement</span></span> | <span data-ttu-id="aa490-125">Value</span><span class="sxs-lookup"><span data-stu-id="aa490-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa490-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa490-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aa490-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa490-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aa490-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa490-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aa490-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa490-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa490-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa490-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa490-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa490-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="aa490-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa490-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa490-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa490-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa490-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa490-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa490-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa490-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa490-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa490-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa490-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="aa490-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="aa490-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="aa490-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="aa490-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="aa490-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="aa490-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="aa490-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="aa490-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="aa490-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="aa490-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="aa490-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="aa490-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="aa490-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="aa490-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="aa490-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





