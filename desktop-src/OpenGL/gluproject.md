---
title: función gluProject (GLU. h)
description: La función gluProject asigna coordenadas de objeto a las coordenadas de la ventana.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject (función) OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491915"
---
# <a name="gluproject-function"></a><span data-ttu-id="aa3d9-104">gluProject función)</span><span class="sxs-lookup"><span data-stu-id="aa3d9-104">gluProject function</span></span>

<span data-ttu-id="aa3d9-105">La función **gluProject** asigna coordenadas de objeto a las coordenadas de la ventana.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-105">The **gluProject** function maps object coordinates to window coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa3d9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa3d9-106">Syntax</span></span>


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a><span data-ttu-id="aa3d9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa3d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa3d9-108">*objx*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-108">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-109">Coordenada x del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-109">The x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-110">*objy*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-110">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-111">Coordenada y del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-111">The y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-112">*objz*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-112">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-113">Coordenada z del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-113">The z object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-115">La matriz de MODELVIEW actual (a partir de una llamada a [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="aa3d9-115">The current modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-117">La matriz de proyección actual (a partir de una llamada a **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="aa3d9-117">The current projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-118">*encuadre*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-119">La ventanilla actual (a partir de una llamada a [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="aa3d9-119">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-120">*winx*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-120">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-121">Coordenada x calculada de la ventana.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-121">The computed x window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-122">*winy*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-122">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-123">Coordenada y de la ventana calculada.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-123">The computed y window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="aa3d9-124">*winz*</span><span class="sxs-lookup"><span data-stu-id="aa3d9-124">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="aa3d9-125">Coordenada de la ventana z calculada.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-125">The computed z window coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa3d9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa3d9-126">Return value</span></span>

<span data-ttu-id="aa3d9-127">Si la función se ejecuta correctamente, el valor devuelto es GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="aa3d9-128">Si se produce un error en la función, el valor devuelto es GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa3d9-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa3d9-129">Remarks</span></span>

<span data-ttu-id="aa3d9-130">La función **gluProject** transforma las coordenadas del objeto especificado en coordenadas de la ventana mediante *modelMatrix*, *projMatrix* y *viewport*.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-130">The **gluProject** function transforms the specified object coordinates into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="aa3d9-131">El resultado se almacena en *Winx*, *Winy* y *Winz*.</span><span class="sxs-lookup"><span data-stu-id="aa3d9-131">The result is stored in *winx*, *winy*, and *winz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa3d9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa3d9-132">Requirements</span></span>



| <span data-ttu-id="aa3d9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa3d9-133">Requirement</span></span> | <span data-ttu-id="aa3d9-134">Value</span><span class="sxs-lookup"><span data-stu-id="aa3d9-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa3d9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa3d9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aa3d9-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa3d9-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aa3d9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa3d9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aa3d9-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa3d9-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aa3d9-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa3d9-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa3d9-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa3d9-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="aa3d9-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa3d9-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa3d9-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa3d9-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa3d9-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa3d9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa3d9-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa3d9-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa3d9-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa3d9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa3d9-146">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="aa3d9-146">**glGetDoublev**</span></span>](glgetdoublev.md)
</dt> <dt>

[<span data-ttu-id="aa3d9-147">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="aa3d9-147">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="aa3d9-148">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="aa3d9-148">**gluUnProject**</span></span>](gluunproject.md)
</dt> </dl>

 

 





