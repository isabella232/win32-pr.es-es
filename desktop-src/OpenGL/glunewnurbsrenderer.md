---
title: función gluNewNurbsRenderer (GLU. h)
description: La función gluNewNurbsRenderer crea un objeto de curva B-spline racional (NURBS) no uniforme.
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- gluNewNurbsRenderer (función) OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b6e35df5abd9fb9e7757dd79066fbbe7efe8680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996621"
---
# <a name="glunewnurbsrenderer-function"></a><span data-ttu-id="52746-104">gluNewNurbsRenderer función)</span><span class="sxs-lookup"><span data-stu-id="52746-104">gluNewNurbsRenderer function</span></span>

<span data-ttu-id="52746-105">La función **gluNewNurbsRenderer** crea un objeto de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.</span><span class="sxs-lookup"><span data-stu-id="52746-105">The **gluNewNurbsRenderer** function creates a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="52746-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52746-106">Syntax</span></span>


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a><span data-ttu-id="52746-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52746-107">Parameters</span></span>

<span data-ttu-id="52746-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="52746-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="52746-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52746-109">Remarks</span></span>

<span data-ttu-id="52746-110">La función **gluNewNurbsRenderer** crea y devuelve un puntero a un nuevo objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="52746-110">The **gluNewNurbsRenderer** function creates and returns a pointer to a new NURBS object.</span></span> <span data-ttu-id="52746-111">Consulte este objeto al llamar a funciones de representación y control de NURBS.</span><span class="sxs-lookup"><span data-stu-id="52746-111">Refer to this object when calling NURBS rendering and control functions.</span></span> <span data-ttu-id="52746-112">Un valor devuelto de cero significa que no hay memoria suficiente para asignar al objeto.</span><span class="sxs-lookup"><span data-stu-id="52746-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="52746-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52746-113">Requirements</span></span>



| <span data-ttu-id="52746-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="52746-114">Requirement</span></span> | <span data-ttu-id="52746-115">Value</span><span class="sxs-lookup"><span data-stu-id="52746-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52746-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52746-116">Minimum supported client</span></span><br/> | <span data-ttu-id="52746-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="52746-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52746-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52746-118">Minimum supported server</span></span><br/> | <span data-ttu-id="52746-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="52746-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52746-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52746-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="52746-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="52746-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="52746-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52746-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="52746-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52746-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="52746-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52746-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52746-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52746-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52746-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="52746-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52746-127">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="52746-127">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="52746-128">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="52746-128">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="52746-129">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="52746-129">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="52746-130">**gluDeleteNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="52746-130">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="52746-131">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="52746-131">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="52746-132">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="52746-132">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





