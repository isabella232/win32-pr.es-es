---
title: función glVertex4sv (GL. h)
description: Especifica un vértice. | función glVertex4sv (GL. h)
ms.assetid: 969ecb41-7e72-4b95-9d84-2d995f60f2a3
keywords:
- glVertex4sv (función) OpenGL
topic_type:
- apiref
api_name:
- glVertex4sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0497fa55b43b22e4649e7ece3eb17f6f9e5339
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914681"
---
# <a name="glvertex4sv-function"></a><span data-ttu-id="70763-105">glVertex4sv función)</span><span class="sxs-lookup"><span data-stu-id="70763-105">glVertex4sv function</span></span>

<span data-ttu-id="70763-106">Especifica un vértice.</span><span class="sxs-lookup"><span data-stu-id="70763-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="70763-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70763-107">Syntax</span></span>


```C++
void WINAPI glVertex4sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="70763-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70763-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70763-109">*v*</span><span class="sxs-lookup"><span data-stu-id="70763-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="70763-110">Puntero a una matriz de cuatro elementos.</span><span class="sxs-lookup"><span data-stu-id="70763-110">A pointer to an array of four elements.</span></span> <span data-ttu-id="70763-111">Los elementos son las coordenadas x, y, z y w de un vértice.</span><span class="sxs-lookup"><span data-stu-id="70763-111">The elements are the x, y, z, and w coordinates of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70763-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70763-112">Return value</span></span>

<span data-ttu-id="70763-113">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="70763-113">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70763-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70763-114">Requirements</span></span>



| <span data-ttu-id="70763-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="70763-115">Requirement</span></span> | <span data-ttu-id="70763-116">Value</span><span class="sxs-lookup"><span data-stu-id="70763-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70763-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70763-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70763-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="70763-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="70763-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70763-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70763-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="70763-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70763-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70763-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="70763-122"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="70763-122"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="70763-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70763-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="70763-124"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70763-124"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="70763-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70763-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70763-126"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70763-126"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70763-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="70763-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70763-128">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="70763-128">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="70763-129">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="70763-129">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="70763-130">**glColor**</span><span class="sxs-lookup"><span data-stu-id="70763-130">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-131">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="70763-131">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-132">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="70763-132">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="70763-133">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="70763-133">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-134">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="70763-134">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-135">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="70763-135">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-136">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="70763-136">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-137">**glRect**</span><span class="sxs-lookup"><span data-stu-id="70763-137">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="70763-138">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="70763-138">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





