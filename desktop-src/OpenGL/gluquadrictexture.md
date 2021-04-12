---
title: función gluQuadricTexture (GLU. h)
description: La función gluQuadricTexture especifica si se va a aplicar textura a Quadrics.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150702"
---
# <a name="gluquadrictexture-function"></a><span data-ttu-id="ec75a-104">gluQuadricTexture función)</span><span class="sxs-lookup"><span data-stu-id="ec75a-104">gluQuadricTexture function</span></span>

<span data-ttu-id="ec75a-105">La función **gluQuadricTexture** especifica si se va a aplicar textura a Quadrics.</span><span class="sxs-lookup"><span data-stu-id="ec75a-105">The **gluQuadricTexture** function specifies whether quadrics are to be textured.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec75a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec75a-106">Syntax</span></span>


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a><span data-ttu-id="ec75a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec75a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec75a-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="ec75a-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75a-109">El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="ec75a-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ec75a-110">*textureCoords*</span><span class="sxs-lookup"><span data-stu-id="ec75a-110">*textureCoords*</span></span> 
</dt> <dd>

<span data-ttu-id="ec75a-111">Marca que indica si se van a generar coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ec75a-111">A flag indicating whether texture coordinates are to be generated.</span></span> <span data-ttu-id="ec75a-112">Los valores siguientes son válidos.</span><span class="sxs-lookup"><span data-stu-id="ec75a-112">The following values are valid.</span></span>



| <span data-ttu-id="ec75a-113">Value</span><span class="sxs-lookup"><span data-stu-id="ec75a-113">Value</span></span>                                                                                                                                          | <span data-ttu-id="ec75a-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ec75a-114">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <span data-ttu-id="ec75a-115"><dt>**GL \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-115"><dt>**GL\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="ec75a-116">Generar coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ec75a-116">Generate texture coordinates.</span></span><br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <span data-ttu-id="ec75a-117"><dt>**CONTABILIDAD \_ falsa**</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-117"><dt>**GL\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ec75a-118">No genere coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="ec75a-118">Do not generate texture coordinates.</span></span> <span data-ttu-id="ec75a-119">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ec75a-119">This is the default value.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec75a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec75a-120">Return value</span></span>

<span data-ttu-id="ec75a-121">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec75a-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec75a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec75a-122">Remarks</span></span>

<span data-ttu-id="ec75a-123">La función **gluQuadricTexture** especifica si las coordenadas de textura se generarán para Quadrics representadas con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="ec75a-123">The **gluQuadricTexture** function specifies whether texture coordinates are to be generated for quadrics rendered with **quadObject**.</span></span>

<span data-ttu-id="ec75a-124">La forma en que se generan las coordenadas de textura depende de la quadric específica que se representa.</span><span class="sxs-lookup"><span data-stu-id="ec75a-124">The manner in which texture coordinates are generated depends upon the specific quadric rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec75a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec75a-125">Requirements</span></span>



| <span data-ttu-id="ec75a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec75a-126">Requirement</span></span> | <span data-ttu-id="ec75a-127">Value</span><span class="sxs-lookup"><span data-stu-id="ec75a-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ec75a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec75a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ec75a-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ec75a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ec75a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec75a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ec75a-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec75a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ec75a-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec75a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec75a-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ec75a-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec75a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec75a-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ec75a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec75a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec75a-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec75a-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec75a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec75a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec75a-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="ec75a-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="ec75a-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="ec75a-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="ec75a-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="ec75a-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> </dl>

 

 





