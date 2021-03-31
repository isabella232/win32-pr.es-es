---
title: función gluDeleteNurbsRenderer (GLU. h)
description: La función gluDeleteNurbsRenderer destruye un objeto de curva B-spline racional (NURBS) no uniforme.
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gluDeleteNurbsRenderer (función) OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802215"
---
# <a name="gludeletenurbsrenderer-function"></a><span data-ttu-id="8254e-104">gluDeleteNurbsRenderer función)</span><span class="sxs-lookup"><span data-stu-id="8254e-104">gluDeleteNurbsRenderer function</span></span>

<span data-ttu-id="8254e-105">La función **gluDeleteNurbsRenderer** destruye un objeto de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.</span><span class="sxs-lookup"><span data-stu-id="8254e-105">The **gluDeleteNurbsRenderer** function destroys a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8254e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8254e-106">Syntax</span></span>


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="8254e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8254e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8254e-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="8254e-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="8254e-109">Objeto NURBS que se va a destruir (creado con **gluNewNurbsRenderer**).</span><span class="sxs-lookup"><span data-stu-id="8254e-109">The NURBS object to be destroyed (created with **gluNewNurbsRenderer**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8254e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8254e-110">Return value</span></span>

<span data-ttu-id="8254e-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8254e-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8254e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8254e-112">Remarks</span></span>

<span data-ttu-id="8254e-113">La función **gluDeleteNurbsRenderer** destruye el objeto NURBS y libera cualquier memoria que haya usado.</span><span class="sxs-lookup"><span data-stu-id="8254e-113">The **gluDeleteNurbsRenderer** function destroys the NURBS object and frees any memory that it used.</span></span> <span data-ttu-id="8254e-114">Después de llamar a **gluDeleteNurbsRenderer**, no puede volver a usar *nobj* .</span><span class="sxs-lookup"><span data-stu-id="8254e-114">After you have called **gluDeleteNurbsRenderer**, you cannot use *nobj* again.</span></span>

## <a name="requirements"></a><span data-ttu-id="8254e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8254e-115">Requirements</span></span>



| <span data-ttu-id="8254e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8254e-116">Requirement</span></span> | <span data-ttu-id="8254e-117">Value</span><span class="sxs-lookup"><span data-stu-id="8254e-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8254e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8254e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8254e-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8254e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8254e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8254e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8254e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8254e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8254e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8254e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8254e-123"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8254e-123"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8254e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8254e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="8254e-125"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8254e-125"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8254e-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8254e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8254e-127"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8254e-127"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8254e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8254e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8254e-129">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="8254e-129">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





