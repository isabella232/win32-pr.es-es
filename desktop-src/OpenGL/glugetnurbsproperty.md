---
title: función gluGetNurbsProperty (GLU. h)
description: La función gluGetNurbsProperty obtiene una propiedad no uniforme B-spline racional (NURBS).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty (función) OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150166"
---
# <a name="glugetnurbsproperty-function"></a><span data-ttu-id="44ca0-104">gluGetNurbsProperty función)</span><span class="sxs-lookup"><span data-stu-id="44ca0-104">gluGetNurbsProperty function</span></span>

<span data-ttu-id="44ca0-105">La función **gluGetNurbsProperty** obtiene una propiedad no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="44ca0-105">The **gluGetNurbsProperty** function gets a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ca0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44ca0-106">Syntax</span></span>


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a><span data-ttu-id="44ca0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44ca0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44ca0-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="44ca0-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="44ca0-109">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="44ca0-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="44ca0-110">*property*</span><span class="sxs-lookup"><span data-stu-id="44ca0-110">*property*</span></span> 
</dt> <dd>

<span data-ttu-id="44ca0-111">Propiedad cuyo valor se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="44ca0-111">The property whose value is to be retrieved.</span></span> <span data-ttu-id="44ca0-112">Los valores siguientes son válidos: GLU, la tolerancia de muestreo, el \_ modo de presentación de Glu, la selección de Glu, la \_ matriz de \_ \_ \_ \_ \_ carga automática de Glu, la \_ \_ tolerancia paramétrica de Glu, el \_ \_ \_ método de muestreo Glu, el paso de Glu \_ U \_ y Glu \_ V \_ .</span><span class="sxs-lookup"><span data-stu-id="44ca0-112">The following values are valid: GLU\_SAMPLING\_TOLERANCE, GLU\_DISPLAY\_MODE, GLU\_CULLING, GLU\_AUTO\_LOAD\_MATRIX, GLU\_PARAMETRIC\_TOLERANCE, GLU\_SAMPLING\_METHOD, GLU\_U\_STEP, and GLU\_V\_STEP.</span></span>

</dd> <dt>

<span data-ttu-id="44ca0-113">*value*</span><span class="sxs-lookup"><span data-stu-id="44ca0-113">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="44ca0-114">Puntero a la ubicación en la que se escribe el valor de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="44ca0-114">A pointer to the location into which the value of the named property is written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44ca0-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44ca0-115">Return value</span></span>

<span data-ttu-id="44ca0-116">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="44ca0-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ca0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44ca0-117">Remarks</span></span>

<span data-ttu-id="44ca0-118">Use **gluGetNurbsProperty** para recuperar las propiedades almacenadas en un objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="44ca0-118">Use **gluGetNurbsProperty** to retrieve properties stored in a NURBS object.</span></span> <span data-ttu-id="44ca0-119">Estas propiedades afectan a la manera en que se representan las curvas y curvas de NURBS.</span><span class="sxs-lookup"><span data-stu-id="44ca0-119">These properties affect the way NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="44ca0-120">Para obtener información acerca de las propiedades de NURBS, vea [**gluNurbsProperty**](glunurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="44ca0-120">For information about NURBS properties, see [**gluNurbsProperty**](glunurbsproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44ca0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ca0-121">Requirements</span></span>



| <span data-ttu-id="44ca0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ca0-122">Requirement</span></span> | <span data-ttu-id="44ca0-123">Value</span><span class="sxs-lookup"><span data-stu-id="44ca0-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44ca0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ca0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="44ca0-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="44ca0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44ca0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44ca0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="44ca0-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44ca0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44ca0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44ca0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ca0-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ca0-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="44ca0-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44ca0-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="44ca0-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44ca0-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="44ca0-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44ca0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44ca0-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ca0-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ca0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="44ca0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ca0-135">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="44ca0-135">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="44ca0-136">**gluNurbsProperty**</span><span class="sxs-lookup"><span data-stu-id="44ca0-136">**gluNurbsProperty**</span></span>](glunurbsproperty.md)
</dt> </dl>

 

 





