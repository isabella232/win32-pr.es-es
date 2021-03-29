---
title: función glVertex2dv (GL. h)
description: Especifica un vértice. | función glVertex2dv (GL. h)
ms.assetid: b685d0aa-2874-4ad9-a20c-86823e9ad00b
keywords:
- glVertex2dv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex2dv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4839fa650302a67c98a0aef3d227dfafa8ddb688
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003573"
---
# <a name="glvertex2dv-function"></a><span data-ttu-id="3af05-105">glVertex2dv función)</span><span class="sxs-lookup"><span data-stu-id="3af05-105">glVertex2dv function</span></span>

<span data-ttu-id="3af05-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="3af05-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="3af05-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3af05-107">Syntax</span></span>


```C++
void WINAPI glVertex2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="3af05-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3af05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3af05-109">*v*</span><span class="sxs-lookup"><span data-stu-id="3af05-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="3af05-110">Puntero a una matriz de dos elementos.</span><span class="sxs-lookup"><span data-stu-id="3af05-110">A pointer to an array of two elements.</span></span> <span data-ttu-id="3af05-111">Los elementos son las coordenadas x e y de un vértice.</span><span class="sxs-lookup"><span data-stu-id="3af05-111">The elements are the x and y coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3af05-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3af05-112">Return value</span></span>

<span data-ttu-id="3af05-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3af05-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3af05-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3af05-114">Requirements</span></span>



| <span data-ttu-id="3af05-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3af05-115">Requirement</span></span> | <span data-ttu-id="3af05-116">Value</span><span class="sxs-lookup"><span data-stu-id="3af05-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3af05-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3af05-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3af05-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3af05-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3af05-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3af05-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3af05-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3af05-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3af05-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3af05-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3af05-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3af05-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3af05-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3af05-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3af05-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3af05-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3af05-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3af05-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3af05-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3af05-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af05-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3af05-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af05-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3af05-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3af05-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="3af05-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="3af05-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="3af05-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="3af05-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="3af05-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3af05-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="3af05-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="3af05-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="3af05-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="3af05-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="3af05-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="3af05-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="3af05-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





