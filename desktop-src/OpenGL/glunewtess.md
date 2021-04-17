---
title: función gluNewTess (GLU. h)
description: La función gluNewTess crea un objeto de teselación.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- gluNewTess (función) OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665973"
---
# <a name="glunewtess-function"></a><span data-ttu-id="01a2d-104">gluNewTess función)</span><span class="sxs-lookup"><span data-stu-id="01a2d-104">gluNewTess function</span></span>

<span data-ttu-id="01a2d-105">La función **gluNewTess** crea un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="01a2d-105">The **gluNewTess** function creates a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01a2d-106">Syntax</span></span>


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a><span data-ttu-id="01a2d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01a2d-107">Parameters</span></span>

<span data-ttu-id="01a2d-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="01a2d-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a2d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01a2d-109">Remarks</span></span>

<span data-ttu-id="01a2d-110">La función **gluNewTess** crea y devuelve un puntero a un nuevo objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="01a2d-110">The **gluNewTess** function creates and returns a pointer to a new tessellation object.</span></span> <span data-ttu-id="01a2d-111">Haga referencia a este objeto al llamar a funciones de teselación.</span><span class="sxs-lookup"><span data-stu-id="01a2d-111">Refer to this object when calling tessellation functions.</span></span> <span data-ttu-id="01a2d-112">Un valor devuelto de cero significa que no hay memoria suficiente para asignar al objeto.</span><span class="sxs-lookup"><span data-stu-id="01a2d-112">A return value of zero means there is not enough memory to allocate to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a2d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01a2d-113">Requirements</span></span>



| <span data-ttu-id="01a2d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a2d-114">Requirement</span></span> | <span data-ttu-id="01a2d-115">Value</span><span class="sxs-lookup"><span data-stu-id="01a2d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="01a2d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01a2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01a2d-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="01a2d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="01a2d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01a2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01a2d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01a2d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="01a2d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01a2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a2d-121"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a2d-121"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="01a2d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01a2d-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="01a2d-123"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01a2d-123"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="01a2d-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01a2d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01a2d-125"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01a2d-125"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a2d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="01a2d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a2d-127">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="01a2d-127">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="01a2d-128">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="01a2d-128">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="01a2d-129">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="01a2d-129">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





