---
title: función glVertex2iv (GL. h)
description: Especifica un vértice. | función glVertex2iv (GL. h)
ms.assetid: 3b88bf7d-5743-4ac0-a79f-5f450b488bd2
keywords:
- glVertex2iv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex2iv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594c50ff1e30184d5a7292c5b639f16a48f0820b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083680"
---
# <a name="glvertex2iv-function"></a><span data-ttu-id="0ebdf-105">glVertex2iv función)</span><span class="sxs-lookup"><span data-stu-id="0ebdf-105">glVertex2iv function</span></span>

<span data-ttu-id="0ebdf-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="0ebdf-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebdf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ebdf-107">Syntax</span></span>


```C++
void WINAPI glVertex2iv(
   const GLint *v
);
```



## <a name="parameters"></a><span data-ttu-id="0ebdf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ebdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebdf-109">*v*</span><span class="sxs-lookup"><span data-stu-id="0ebdf-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebdf-110">Puntero a una matriz de dos elementos.</span><span class="sxs-lookup"><span data-stu-id="0ebdf-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="0ebdf-111">Los elementos son las coordenadas x e y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="0ebdf-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebdf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ebdf-112">Return value</span></span>

<span data-ttu-id="0ebdf-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0ebdf-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebdf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebdf-114">Requirements</span></span>



| <span data-ttu-id="0ebdf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebdf-115">Requirement</span></span> | <span data-ttu-id="0ebdf-116">Value</span><span class="sxs-lookup"><span data-stu-id="0ebdf-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebdf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ebdf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebdf-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0ebdf-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0ebdf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ebdf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebdf-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ebdf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0ebdf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ebdf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebdf-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebdf-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0ebdf-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ebdf-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ebdf-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ebdf-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0ebdf-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ebdf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ebdf-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ebdf-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebdf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ebdf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebdf-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="0ebdf-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0ebdf-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





