---
title: función gluQuadricNormals (GLU. h)
description: La función gluQuadricNormals especifica qué tipo de normalización se usará para Quadrics.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- gluQuadricNormals (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491909"
---
# <a name="gluquadricnormals-function"></a><span data-ttu-id="bfbb4-104">gluQuadricNormals función)</span><span class="sxs-lookup"><span data-stu-id="bfbb4-104">gluQuadricNormals function</span></span>

<span data-ttu-id="bfbb4-105">La función **gluQuadricNormals** especifica qué tipo de normalización se usará para Quadrics.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-105">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfbb4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfbb4-106">Syntax</span></span>


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a><span data-ttu-id="bfbb4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bfbb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfbb4-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="bfbb4-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="bfbb4-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="bfbb4-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="bfbb4-110">*las normales*</span><span class="sxs-lookup"><span data-stu-id="bfbb4-110">*normals*</span></span> 
</dt> <dd>

<span data-ttu-id="bfbb4-111">Tipo deseado de normalización.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-111">The desired type of normals.</span></span> <span data-ttu-id="bfbb4-112">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-112">The following values are valid.</span></span>



| <span data-ttu-id="bfbb4-113">Value</span><span class="sxs-lookup"><span data-stu-id="bfbb4-113">Value</span></span>                                                                                                                                                | <span data-ttu-id="bfbb4-114">Significado</span><span class="sxs-lookup"><span data-stu-id="bfbb4-114">Meaning</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <span data-ttu-id="bfbb4-115"><dt>**GLU \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb4-115"><dt>**GLU\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="bfbb4-116">No se generan normales.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-116">No normals are generated.</span></span><br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <span data-ttu-id="bfbb4-117"><dt>**GLU \_ plano**</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb4-117"><dt>**GLU\_FLAT**</dt></span></span> </dl>       | <span data-ttu-id="bfbb4-118">Se genera una normal para cada faceta de un quadric.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-118">One normal is generated for every facet of a quadric.</span></span><br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <span data-ttu-id="bfbb4-119"><dt>**\_Smooth Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb4-119"><dt>**GLU\_SMOOTH**</dt></span></span> </dl> | <span data-ttu-id="bfbb4-120">Se genera una normal para cada vértice de un quadric.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-120">One normal is generated for every vertex of a quadric.</span></span> <span data-ttu-id="bfbb4-121">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-121">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfbb4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bfbb4-122">Return value</span></span>

<span data-ttu-id="bfbb4-123">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfbb4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfbb4-124">Remarks</span></span>

<span data-ttu-id="bfbb4-125">La función **gluQuadricNormals** especifica qué tipo de normalización se va a usar para Quadrics representada con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="bfbb4-125">The **gluQuadricNormals** function specifies what kind of normals are to be used for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfbb4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfbb4-126">Requirements</span></span>



| <span data-ttu-id="bfbb4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfbb4-127">Requirement</span></span> | <span data-ttu-id="bfbb4-128">Value</span><span class="sxs-lookup"><span data-stu-id="bfbb4-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbb4-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfbb4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bfbb4-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bfbb4-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="bfbb4-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfbb4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bfbb4-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfbb4-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfbb4-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfbb4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfbb4-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb4-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="bfbb4-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bfbb4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="bfbb4-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb4-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bfbb4-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfbb4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfbb4-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfbb4-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfbb4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfbb4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfbb4-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="bfbb4-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="bfbb4-141">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="bfbb4-141">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="bfbb4-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="bfbb4-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="bfbb4-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="bfbb4-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





