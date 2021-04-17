---
title: función glVertex2sv (GL. h)
description: Especifica un vértice. | función glVertex2sv (GL. h)
ms.assetid: 4e13356a-a74b-4fb6-a001-1fffc28dd7a1
keywords:
- glVertex2sv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex2sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e865ab8999e08f9c13ad46443ba039be1cda9e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689792"
---
# <a name="glvertex2sv-function"></a><span data-ttu-id="fa9d1-105">glVertex2sv función)</span><span class="sxs-lookup"><span data-stu-id="fa9d1-105">glVertex2sv function</span></span>

<span data-ttu-id="fa9d1-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="fa9d1-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa9d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa9d1-107">Syntax</span></span>


```C++
void WINAPI glVertex2sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="fa9d1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa9d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa9d1-109">*v*</span><span class="sxs-lookup"><span data-stu-id="fa9d1-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="fa9d1-110">Puntero a una matriz de dos elementos.</span><span class="sxs-lookup"><span data-stu-id="fa9d1-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="fa9d1-111">Los elementos son las coordenadas x e y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="fa9d1-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa9d1-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa9d1-112">Return value</span></span>

<span data-ttu-id="fa9d1-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fa9d1-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa9d1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa9d1-114">Requirements</span></span>



| <span data-ttu-id="fa9d1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa9d1-115">Requirement</span></span> | <span data-ttu-id="fa9d1-116">Value</span><span class="sxs-lookup"><span data-stu-id="fa9d1-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9d1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa9d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa9d1-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fa9d1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa9d1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa9d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa9d1-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fa9d1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa9d1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa9d1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa9d1-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa9d1-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fa9d1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa9d1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa9d1-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa9d1-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa9d1-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa9d1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa9d1-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa9d1-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa9d1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa9d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa9d1-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="fa9d1-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="fa9d1-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





