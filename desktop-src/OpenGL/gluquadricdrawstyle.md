---
title: función gluQuadricDrawStyle (GLU. h)
description: La función gluQuadricDrawStyle especifica el estilo de dibujo deseado para Quadrics.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996773"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="dcf65-104">gluQuadricDrawStyle función)</span><span class="sxs-lookup"><span data-stu-id="dcf65-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="dcf65-105">La función **gluQuadricDrawStyle** especifica el estilo de dibujo deseado para Quadrics.</span><span class="sxs-lookup"><span data-stu-id="dcf65-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf65-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcf65-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="dcf65-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcf65-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf65-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="dcf65-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf65-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="dcf65-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="dcf65-110">*drawStyle*</span><span class="sxs-lookup"><span data-stu-id="dcf65-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf65-111">Estilo de dibujo deseado.</span><span class="sxs-lookup"><span data-stu-id="dcf65-111">The desired draw style.</span></span> <span data-ttu-id="dcf65-112">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="dcf65-112">The following values are valid.</span></span>



| <span data-ttu-id="dcf65-113">Value</span><span class="sxs-lookup"><span data-stu-id="dcf65-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="dcf65-114">Significado</span><span class="sxs-lookup"><span data-stu-id="dcf65-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="dcf65-115"><dt>**relleno de GLU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="dcf65-116">Quadrics se representan con primitivas de polígonos.</span><span class="sxs-lookup"><span data-stu-id="dcf65-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="dcf65-117">Los polígonos se dibujan en sentido contrario a las agujas del reloj con respecto a sus normales (como se define con [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="dcf65-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="dcf65-118"><dt>**\_línea Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="dcf65-119">Quadrics se representan como un conjunto de líneas.</span><span class="sxs-lookup"><span data-stu-id="dcf65-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="dcf65-120"><dt>**\_silueta Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="dcf65-121">Quadrics se representan como un conjunto de líneas, con la excepción de que los bordes que separan las caras coplanaras no se dibujarán.</span><span class="sxs-lookup"><span data-stu-id="dcf65-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="dcf65-122"><dt>**\_punto Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="dcf65-123">Quadrics se representan como un conjunto de puntos.</span><span class="sxs-lookup"><span data-stu-id="dcf65-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf65-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcf65-124">Return value</span></span>

<span data-ttu-id="dcf65-125">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dcf65-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf65-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcf65-126">Remarks</span></span>

<span data-ttu-id="dcf65-127">La función **gluQuadricDrawStyle** especifica el estilo de dibujo de Quadrics representado con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="dcf65-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf65-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf65-128">Requirements</span></span>



| <span data-ttu-id="dcf65-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf65-129">Requirement</span></span> | <span data-ttu-id="dcf65-130">Value</span><span class="sxs-lookup"><span data-stu-id="dcf65-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf65-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcf65-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf65-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dcf65-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dcf65-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcf65-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf65-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dcf65-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dcf65-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcf65-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcf65-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="dcf65-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcf65-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcf65-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="dcf65-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dcf65-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf65-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcf65-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf65-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcf65-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf65-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="dcf65-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="dcf65-143">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="dcf65-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="dcf65-144">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="dcf65-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="dcf65-145">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="dcf65-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





