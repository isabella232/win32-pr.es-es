---
title: función glEdgeFlag (GL. h)
description: Marca los bordes como límite o no límite. | función glEdgeFlag (GL. h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- glEdgeFlag (función) OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599a0b539e32d0e457f92c256e2cb0b678b05b59
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689734"
---
# <a name="gledgeflag-function"></a><span data-ttu-id="5f544-105">glEdgeFlag función)</span><span class="sxs-lookup"><span data-stu-id="5f544-105">glEdgeFlag function</span></span>

<span data-ttu-id="5f544-106">Marca los bordes como límite o no límite.</span><span class="sxs-lookup"><span data-stu-id="5f544-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f544-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f544-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a><span data-ttu-id="5f544-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f544-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f544-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="5f544-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="5f544-110">Especifica el valor de marca perimetral actual, ya sea **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="5f544-110">Specifies the current edge flag value, either **TRUE** or **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f544-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f544-111">Return value</span></span>

<span data-ttu-id="5f544-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5f544-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f544-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f544-113">Remarks</span></span>

<span data-ttu-id="5f544-114">Cada vértice de un polígono, un triángulo independiente o cuadrangular independientes especificados entre [](/windows/desktop/OpenGL/glbegin)un / par de [**glEnd**](/windows/desktop/OpenGL/glend) de glBegin se marca como el inicio de un límite o de un borde no enlazado.</span><span class="sxs-lookup"><span data-stu-id="5f544-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="5f544-115">Si la marca de borde actual es **true** cuando se especifica el vértice, el vértice se marca como el inicio de un borde del límite.</span><span class="sxs-lookup"><span data-stu-id="5f544-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="5f544-116">Si la marca de borde actual es **false**, el vértice se marca como el inicio de un borde no enlazado.</span><span class="sxs-lookup"><span data-stu-id="5f544-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="5f544-117">La función **glEdgeFlag** establece la marca perimetral en **true** si la marca es distinto de cero; de lo contrario, devuelve **false** .</span><span class="sxs-lookup"><span data-stu-id="5f544-117">The **glEdgeFlag** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="5f544-118">Los vértices de los triángulos conectados y los quadrilaterals conectados siempre se marcan como límites, independientemente del valor de la marca de borde.</span><span class="sxs-lookup"><span data-stu-id="5f544-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="5f544-119">Los límites de límite y no límite en los vértices solo son significativos si el modo de polígono de contabilidad \_ \_ está establecido en el punto de contabilidad o en la \_ línea de contabilidad \_ .</span><span class="sxs-lookup"><span data-stu-id="5f544-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="5f544-120">Vea [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="5f544-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="5f544-121">Inicialmente, el bit de marca perimetral es **true**.</span><span class="sxs-lookup"><span data-stu-id="5f544-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="5f544-122">La marca perimetral actual se puede actualizar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="5f544-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="5f544-123">En concreto, se puede llamar a **glEdgeFlag** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente a [**glEnd**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="5f544-123">In particular, **glEdgeFlag** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="5f544-124">Las siguientes funciones recuperan información relacionada con **glEdgeFlag**:</span><span class="sxs-lookup"><span data-stu-id="5f544-124">The following functions retrieve information related to **glEdgeFlag**:</span></span>

<span data-ttu-id="5f544-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con marcador de contabilidad de margen de argumento \_ \_</span><span class="sxs-lookup"><span data-stu-id="5f544-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="5f544-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f544-126">Requirements</span></span>



| <span data-ttu-id="5f544-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f544-127">Requirement</span></span> | <span data-ttu-id="5f544-128">Value</span><span class="sxs-lookup"><span data-stu-id="5f544-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f544-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f544-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5f544-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f544-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f544-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f544-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5f544-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f544-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f544-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f544-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f544-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f544-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5f544-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f544-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f544-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f544-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f544-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f544-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f544-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f544-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

