---
title: función glVertex2fv (GL. h)
description: Especifica un vértice. | función glVertex2fv (GL. h)
ms.assetid: bae32d27-2a19-40d5-a3f7-0e7a41918034
keywords:
- glVertex2fv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd7a57aff2166f3605d7007cd194f5cff04784
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670155"
---
# <a name="glvertex2fv-function"></a><span data-ttu-id="bf241-105">glVertex2fv función)</span><span class="sxs-lookup"><span data-stu-id="bf241-105">glVertex2fv function</span></span>

<span data-ttu-id="bf241-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="bf241-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf241-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf241-107">Syntax</span></span>


```C++
void WINAPI glVertex2fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="bf241-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf241-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf241-109">*v*</span><span class="sxs-lookup"><span data-stu-id="bf241-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="bf241-110">Puntero a una matriz de dos elementos.</span><span class="sxs-lookup"><span data-stu-id="bf241-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="bf241-111">Los elementos son las coordenadas x e y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="bf241-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf241-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf241-112">Return value</span></span>

<span data-ttu-id="bf241-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bf241-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf241-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf241-114">Requirements</span></span>



| <span data-ttu-id="bf241-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf241-115">Requirement</span></span> | <span data-ttu-id="bf241-116">Value</span><span class="sxs-lookup"><span data-stu-id="bf241-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf241-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf241-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf241-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf241-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf241-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf241-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf241-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf241-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf241-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf241-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf241-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf241-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bf241-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf241-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf241-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf241-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf241-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf241-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf241-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf241-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf241-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf241-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf241-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bf241-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bf241-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="bf241-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="bf241-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="bf241-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="bf241-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bf241-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bf241-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="bf241-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="bf241-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="bf241-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="bf241-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="bf241-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="bf241-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="bf241-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





