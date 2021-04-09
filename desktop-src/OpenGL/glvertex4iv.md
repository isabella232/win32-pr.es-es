---
title: función glVertex4iv (GL. h)
description: Especifica un vértice. | función glVertex4iv (GL. h)
ms.assetid: 7b56777a-f904-4a9d-8d3d-84a38cbf0b45
keywords:
- glVertex4iv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex4iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff55c5534245843d5caa8797b2b529c7cfe00f9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914682"
---
# <a name="glvertex4iv-function"></a><span data-ttu-id="bfd3c-105">glVertex4iv función)</span><span class="sxs-lookup"><span data-stu-id="bfd3c-105">glVertex4iv function</span></span>

<span data-ttu-id="bfd3c-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd3c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfd3c-107">Syntax</span></span>


```C++
void WINAPI glVertex4iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="bfd3c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfd3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd3c-109">*v*</span><span class="sxs-lookup"><span data-stu-id="bfd3c-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="bfd3c-110">Puntero a una matriz de cuatro elementos.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="bfd3c-111">Los elementos son las coordenadas x, y, z y w de un vértice.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd3c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfd3c-112">Return value</span></span>

<span data-ttu-id="bfd3c-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bfd3c-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd3c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfd3c-114">Requirements</span></span>



| <span data-ttu-id="bfd3c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd3c-115">Requirement</span></span> | <span data-ttu-id="bfd3c-116">Value</span><span class="sxs-lookup"><span data-stu-id="bfd3c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd3c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfd3c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd3c-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bfd3c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bfd3c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfd3c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd3c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfd3c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bfd3c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfd3c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd3c-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd3c-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bfd3c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfd3c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfd3c-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfd3c-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bfd3c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfd3c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfd3c-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd3c-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd3c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfd3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd3c-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="bfd3c-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="bfd3c-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





