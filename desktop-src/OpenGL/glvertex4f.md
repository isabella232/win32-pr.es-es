---
title: función glVertex4f (GL. h)
description: Especifica un vértice. | función glVertex4f (GL. h)
ms.assetid: 877fce8c-095e-4ae4-8633-7c84659ee8a6
keywords:
- glVertex4f (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex4f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b07852c1199338917ca1f29c54923ba6a904f30f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003577"
---
# <a name="glvertex4f-function"></a><span data-ttu-id="e158b-105">glVertex4f función)</span><span class="sxs-lookup"><span data-stu-id="e158b-105">glVertex4f function</span></span>

<span data-ttu-id="e158b-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="e158b-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="e158b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e158b-107">Syntax</span></span>


```C++
void WINAPI glVertex4f(
   GLfloat x,
   GLfloat y,
   GLfloat z,
   GLfloat w
);
```



## <a name="parameters"></a><span data-ttu-id="e158b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e158b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e158b-109">*x*</span><span class="sxs-lookup"><span data-stu-id="e158b-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="e158b-110">Especifica la coordenada x de un vértice.</span><span class="sxs-lookup"><span data-stu-id="e158b-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="e158b-111">*y*</span><span class="sxs-lookup"><span data-stu-id="e158b-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="e158b-112">Especifica la coordenada y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="e158b-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="e158b-113">*z*</span><span class="sxs-lookup"><span data-stu-id="e158b-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="e158b-114">Especifica la coordenada z de un vértice.</span><span class="sxs-lookup"><span data-stu-id="e158b-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="e158b-115">*w*</span><span class="sxs-lookup"><span data-stu-id="e158b-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="e158b-116">Especifica la coordenada w de un vértice.</span><span class="sxs-lookup"><span data-stu-id="e158b-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e158b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e158b-117">Return value</span></span>

<span data-ttu-id="e158b-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e158b-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e158b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e158b-119">Remarks</span></span>

<span data-ttu-id="e158b-120">Los comandos de la función glVertex se usan en pares de [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de punto, línea y polígono.</span><span class="sxs-lookup"><span data-stu-id="e158b-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="e158b-121">Las coordenadas color, normal y Texture actuales están asociadas al vértice cuando se llama a glVertex.</span><span class="sxs-lookup"><span data-stu-id="e158b-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="e158b-122">Cuando solo se especifican *x* *e y,* *z* tiene como valor predeterminado 0,0 y *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="e158b-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="e158b-123">Cuando se especifican *x*, *y* y *z* , el valor predeterminado de *w* es 1,0.</span><span class="sxs-lookup"><span data-stu-id="e158b-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="e158b-124">La invocación de glVertex fuera de un par glEnd de **glBegin** /  produce un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="e158b-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="e158b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e158b-125">Requirements</span></span>



| <span data-ttu-id="e158b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e158b-126">Requirement</span></span> | <span data-ttu-id="e158b-127">Value</span><span class="sxs-lookup"><span data-stu-id="e158b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e158b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e158b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e158b-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e158b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e158b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e158b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e158b-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e158b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e158b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e158b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e158b-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e158b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e158b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e158b-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e158b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e158b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e158b-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e158b-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e158b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e158b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e158b-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e158b-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e158b-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="e158b-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="e158b-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="e158b-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="e158b-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-143">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e158b-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e158b-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="e158b-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="e158b-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="e158b-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="e158b-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="e158b-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="e158b-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="e158b-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





