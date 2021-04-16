---
title: función glVertex3sv (GL. h)
description: Especifica un vértice. | función glVertex3sv (GL. h)
ms.assetid: 8b819a95-f834-4c6e-b88a-a96ae9b36c71
keywords:
- glVertex3sv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex3sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa808f76beefa440c3fa4a93a2301cf8b40dfcb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689770"
---
# <a name="glvertex3sv-function"></a><span data-ttu-id="029aa-105">glVertex3sv función)</span><span class="sxs-lookup"><span data-stu-id="029aa-105">glVertex3sv function</span></span>

<span data-ttu-id="029aa-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="029aa-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="029aa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="029aa-107">Syntax</span></span>


```C++
void WINAPI glVertex3sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="029aa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="029aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029aa-109">*v*</span><span class="sxs-lookup"><span data-stu-id="029aa-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="029aa-110">Puntero a una matriz de tres elementos.</span><span class="sxs-lookup"><span data-stu-id="029aa-110">A pointer to an array of three elements.</span></span> <span data-ttu-id="029aa-111">Los elementos son las coordenadas x, y y z de un vértice.</span><span class="sxs-lookup"><span data-stu-id="029aa-111">The elements are the x, y, and z coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029aa-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="029aa-112">Return value</span></span>

<span data-ttu-id="029aa-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="029aa-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="029aa-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="029aa-114">Requirements</span></span>



| <span data-ttu-id="029aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="029aa-115">Requirement</span></span> | <span data-ttu-id="029aa-116">Value</span><span class="sxs-lookup"><span data-stu-id="029aa-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="029aa-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="029aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="029aa-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="029aa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="029aa-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="029aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="029aa-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="029aa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="029aa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="029aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="029aa-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="029aa-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="029aa-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="029aa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="029aa-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="029aa-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="029aa-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="029aa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="029aa-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="029aa-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029aa-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="029aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029aa-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="029aa-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="029aa-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="029aa-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="029aa-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="029aa-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="029aa-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="029aa-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="029aa-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="029aa-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="029aa-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="029aa-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="029aa-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="029aa-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="029aa-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="029aa-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





