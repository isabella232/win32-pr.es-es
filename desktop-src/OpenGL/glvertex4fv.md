---
title: función glVertex4fv (GL. h)
description: Especifica un vértice. | función glVertex4fv (GL. h)
ms.assetid: c2a766fd-3ad8-463b-8f09-36d0673e6716
keywords:
- glVertex4fv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex4fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e05551268b697ba4444c29d5f2b9bdfb0e832e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689763"
---
# <a name="glvertex4fv-function"></a><span data-ttu-id="63539-105">glVertex4fv función)</span><span class="sxs-lookup"><span data-stu-id="63539-105">glVertex4fv function</span></span>

<span data-ttu-id="63539-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="63539-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="63539-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63539-107">Syntax</span></span>


```C++
void WINAPI glVertex4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a><span data-ttu-id="63539-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63539-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63539-109">*v*</span><span class="sxs-lookup"><span data-stu-id="63539-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="63539-110">Puntero a una matriz de cuatro elementos.</span><span class="sxs-lookup"><span data-stu-id="63539-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="63539-111">Los elementos son las coordenadas x, y, z y w de un vértice.</span><span class="sxs-lookup"><span data-stu-id="63539-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63539-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63539-112">Return value</span></span>

<span data-ttu-id="63539-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="63539-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="63539-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63539-114">Requirements</span></span>



| <span data-ttu-id="63539-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63539-115">Requirement</span></span> | <span data-ttu-id="63539-116">Value</span><span class="sxs-lookup"><span data-stu-id="63539-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63539-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63539-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63539-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63539-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63539-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63539-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63539-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63539-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63539-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63539-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="63539-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="63539-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63539-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63539-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="63539-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63539-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63539-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63539-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63539-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63539-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63539-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="63539-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63539-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="63539-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="63539-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="63539-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="63539-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="63539-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="63539-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="63539-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="63539-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="63539-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="63539-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="63539-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="63539-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="63539-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="63539-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="63539-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





