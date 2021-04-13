---
title: función gluGetTessProperty (GLU. h)
description: La función gluGetTessProperty obtiene una propiedad de objeto de teselación.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty (función) OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422213"
---
# <a name="glugettessproperty-function"></a><span data-ttu-id="b46aa-104">gluGetTessProperty función)</span><span class="sxs-lookup"><span data-stu-id="b46aa-104">gluGetTessProperty function</span></span>

<span data-ttu-id="b46aa-105">La función **gluGetTessProperty** obtiene una propiedad de objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="b46aa-105">The **gluGetTessProperty** function gets a tessellation object property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b46aa-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b46aa-106">Syntax</span></span>


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a><span data-ttu-id="b46aa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b46aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b46aa-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="b46aa-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="b46aa-109">Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="b46aa-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b46aa-110">*cuales*</span><span class="sxs-lookup"><span data-stu-id="b46aa-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="b46aa-111">Propiedad cuyo valor se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b46aa-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="b46aa-112">Los valores siguientes son válidos: \_ Glu \_ Tess \_ , Glu \_ Tess \_ BOUNDARY \_ y Glu \_ Tess \_ Tolerance.</span><span class="sxs-lookup"><span data-stu-id="b46aa-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>

</dd> <dt>

<span data-ttu-id="b46aa-113">*value*</span><span class="sxs-lookup"><span data-stu-id="b46aa-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="b46aa-114">Puntero a la ubicación donde se escribe el valor de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="b46aa-114">A pointer to the location where the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b46aa-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b46aa-115">Return value</span></span>

<span data-ttu-id="b46aa-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b46aa-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b46aa-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b46aa-117">Remarks</span></span>

<span data-ttu-id="b46aa-118">Use **gluGetTessProperty** para recuperar las propiedades almacenadas en un objeto de teselación.</span><span class="sxs-lookup"><span data-stu-id="b46aa-118">Use **gluGetTessProperty** to retrieve properties stored in a tessellation object.</span></span> <span data-ttu-id="b46aa-119">Estas propiedades afectan a la manera en que se interpretan y representan los objetos de teselación.</span><span class="sxs-lookup"><span data-stu-id="b46aa-119">These properties affect the way tessellation objects are interpreted and rendered.</span></span> <span data-ttu-id="b46aa-120">Para obtener información sobre qué son las propiedades y qué hacen, vea [**gluTessProperty**](glutessproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b46aa-120">For information about what the properties are and what they do, see [**gluTessProperty**](glutessproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b46aa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b46aa-121">Requirements</span></span>



| <span data-ttu-id="b46aa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b46aa-122">Requirement</span></span> | <span data-ttu-id="b46aa-123">Value</span><span class="sxs-lookup"><span data-stu-id="b46aa-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b46aa-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b46aa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b46aa-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b46aa-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b46aa-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b46aa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b46aa-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b46aa-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b46aa-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b46aa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b46aa-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b46aa-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b46aa-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b46aa-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b46aa-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b46aa-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b46aa-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b46aa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b46aa-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b46aa-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b46aa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b46aa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b46aa-135">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="b46aa-135">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="b46aa-136">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="b46aa-136">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> </dl>

 

 





