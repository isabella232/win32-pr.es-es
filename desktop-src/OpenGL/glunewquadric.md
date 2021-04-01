---
title: función gluNewQuadric (GLU. h)
description: La función gluNewQuadric crea un objeto quadric.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- gluNewQuadric (función) OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996620"
---
# <a name="glunewquadric-function"></a><span data-ttu-id="28e68-104">gluNewQuadric función)</span><span class="sxs-lookup"><span data-stu-id="28e68-104">gluNewQuadric function</span></span>

<span data-ttu-id="28e68-105">La función **gluNewQuadric** crea un objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="28e68-105">The **gluNewQuadric** function creates a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e68-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28e68-106">Syntax</span></span>


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a><span data-ttu-id="28e68-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28e68-107">Parameters</span></span>

<span data-ttu-id="28e68-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28e68-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e68-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28e68-109">Remarks</span></span>

<span data-ttu-id="28e68-110">La función **gluNewQuadric** crea y devuelve un puntero a un nuevo objeto quadric.</span><span class="sxs-lookup"><span data-stu-id="28e68-110">The **gluNewQuadric** function creates and returns a pointer to a new quadric object.</span></span> <span data-ttu-id="28e68-111">Consulte este objeto al llamar a funciones de representación y control de quadric.</span><span class="sxs-lookup"><span data-stu-id="28e68-111">Refer to this object when calling quadric rendering and control functions.</span></span> <span data-ttu-id="28e68-112">Un valor devuelto de cero significa que no hay memoria suficiente para asignar al objeto.</span><span class="sxs-lookup"><span data-stu-id="28e68-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e68-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e68-113">Requirements</span></span>



| <span data-ttu-id="28e68-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e68-114">Requirement</span></span> | <span data-ttu-id="28e68-115">Value</span><span class="sxs-lookup"><span data-stu-id="28e68-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="28e68-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28e68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28e68-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28e68-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="28e68-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28e68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28e68-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28e68-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="28e68-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28e68-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e68-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e68-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="28e68-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28e68-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="28e68-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28e68-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="28e68-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28e68-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28e68-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28e68-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e68-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="28e68-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e68-127">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="28e68-127">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="28e68-128">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="28e68-128">**gluDeleteQuadric**</span></span>](gludeletequadric.md)
</dt> <dt>

[<span data-ttu-id="28e68-129">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="28e68-129">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="28e68-130">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="28e68-130">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="28e68-131">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="28e68-131">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="28e68-132">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="28e68-132">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="28e68-133">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="28e68-133">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="28e68-134">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="28e68-134">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="28e68-135">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="28e68-135">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="28e68-136">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="28e68-136">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





