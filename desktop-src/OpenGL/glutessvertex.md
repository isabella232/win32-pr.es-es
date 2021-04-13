---
title: función gluTessVertex (GLU. h)
description: La función gluTessVertex especifica un vértice en un polígono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535242"
---
# <a name="glutessvertex-function"></a><span data-ttu-id="5217a-104">gluTessVertex función)</span><span class="sxs-lookup"><span data-stu-id="5217a-104">gluTessVertex function</span></span>

<span data-ttu-id="5217a-105">La función **gluTessVertex** especifica un vértice en un polígono.</span><span class="sxs-lookup"><span data-stu-id="5217a-105">The **gluTessVertex** function specifies a vertex on a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="5217a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5217a-106">Syntax</span></span>


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a><span data-ttu-id="5217a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5217a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5217a-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="5217a-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="5217a-109">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="5217a-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5217a-110">*coords*</span><span class="sxs-lookup"><span data-stu-id="5217a-110">*coords*</span></span> 
</dt> <dd>

<span data-ttu-id="5217a-111">Ubicación del vértice.</span><span class="sxs-lookup"><span data-stu-id="5217a-111">The location of the vertex.</span></span>

</dd> <dt>

<span data-ttu-id="5217a-112">*data*</span><span class="sxs-lookup"><span data-stu-id="5217a-112">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="5217a-113">Un puntero devuelto al programa con la devolución de llamada del vértice (tal y como se especifica en [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="5217a-113">An pointer passed back to the program with the vertex callback (as specified by [*gluTessCallback*](glutess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5217a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5217a-114">Return value</span></span>

<span data-ttu-id="5217a-115">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5217a-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5217a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5217a-116">Remarks</span></span>

<span data-ttu-id="5217a-117">La función **gluTessVertex** describe un vértice de un polígono que el usuario está definiendo.</span><span class="sxs-lookup"><span data-stu-id="5217a-117">The **gluTessVertex** function describes a vertex on a polygon that the user is defining.</span></span> <span data-ttu-id="5217a-118">Las llamadas sucesivas a **gluTessVertex** describen un contorno cerrado.</span><span class="sxs-lookup"><span data-stu-id="5217a-118">Successive **gluTessVertex** calls describe a closed contour.</span></span> <span data-ttu-id="5217a-119">Por ejemplo, para describir un cuadrangular, llame a **gluTessVertex** cuatro veces.</span><span class="sxs-lookup"><span data-stu-id="5217a-119">For example, to describe a quadrilateral, call **gluTessVertex** four times.</span></span> <span data-ttu-id="5217a-120">Solo se puede llamar a **gluTessVertex** entre [**gluTessBeginContour**](glutessbegincontour.md) y [**gluTessEndContour**](glutessendcontour.md).</span><span class="sxs-lookup"><span data-stu-id="5217a-120">You can only call **gluTessVertex** between [**gluTessBeginContour**](glutessbegincontour.md) and [**gluTessEndContour**](glutessendcontour.md).</span></span>

<span data-ttu-id="5217a-121">Normalmente, el parámetro *Data* apunta a una estructura que contiene la ubicación del vértice, así como a otros atributos por vértice como color y normal.</span><span class="sxs-lookup"><span data-stu-id="5217a-121">The *data* parameter normally points to a structure containing the vertex location, as well as other per-vertex attributes such as color and normal.</span></span> <span data-ttu-id="5217a-122">Este puntero se devuelve al programa a través de la devolución de llamada del vértice de GLU después de la \_ teselación (vea [*gluTessCallback*](glutess.md)).</span><span class="sxs-lookup"><span data-stu-id="5217a-122">This pointer is passed back to the program through the GLU\_VERTEX callback after tessellation (see [*gluTessCallback*](glutess.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="5217a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5217a-123">Requirements</span></span>



| <span data-ttu-id="5217a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5217a-124">Requirement</span></span> | <span data-ttu-id="5217a-125">Value</span><span class="sxs-lookup"><span data-stu-id="5217a-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5217a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5217a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5217a-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5217a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5217a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5217a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5217a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5217a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5217a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5217a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5217a-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5217a-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5217a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5217a-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5217a-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5217a-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5217a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5217a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5217a-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5217a-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5217a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5217a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5217a-137">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="5217a-137">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="5217a-138">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="5217a-138">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="5217a-139">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="5217a-139">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="5217a-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="5217a-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="5217a-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="5217a-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="5217a-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="5217a-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="5217a-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="5217a-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





