---
title: función gluUnProject (GLU. h)
description: La función gluUnProject asigna las coordenadas de la ventana a las coordenadas del objeto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluUnProject (función) OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686194"
---
# <a name="gluunproject-function"></a><span data-ttu-id="58f97-104">gluUnProject función)</span><span class="sxs-lookup"><span data-stu-id="58f97-104">gluUnProject function</span></span>

<span data-ttu-id="58f97-105">La función **gluUnProject** asigna las coordenadas de la ventana a las coordenadas del objeto.</span><span class="sxs-lookup"><span data-stu-id="58f97-105">The **gluUnProject** function maps window coordinates to object coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f97-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58f97-106">Syntax</span></span>


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a><span data-ttu-id="58f97-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58f97-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f97-108">*winx*</span><span class="sxs-lookup"><span data-stu-id="58f97-108">*winx*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-109">Coordenada x de la ventana que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="58f97-109">The x window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="58f97-110">*winy*</span><span class="sxs-lookup"><span data-stu-id="58f97-110">*winy*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-111">Coordenada de la ventana y que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="58f97-111">The y window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="58f97-112">*winz*</span><span class="sxs-lookup"><span data-stu-id="58f97-112">*winz*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-113">Coordenada de la ventana de z que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="58f97-113">The z window coordinate to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="58f97-114">*modelMatrix*</span><span class="sxs-lookup"><span data-stu-id="58f97-114">*modelMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-115">La matriz MODELVIEW (a partir de una llamada a [**glGetDoublev**](glgetdoublev.md) ).</span><span class="sxs-lookup"><span data-stu-id="58f97-115">The modelview matrix (as from a [**glGetDoublev**](glgetdoublev.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="58f97-116">*projMatrix*</span><span class="sxs-lookup"><span data-stu-id="58f97-116">*projMatrix*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-117">La matriz de proyección (a partir de una llamada a **glGetDoublev** ).</span><span class="sxs-lookup"><span data-stu-id="58f97-117">The projection matrix (as from a **glGetDoublev** call).</span></span>

</dd> <dt>

<span data-ttu-id="58f97-118">*encuadre*</span><span class="sxs-lookup"><span data-stu-id="58f97-118">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-119">La ventanilla (a partir de una llamada a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="58f97-119">The viewport (as from a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) call).</span></span>

</dd> <dt>

<span data-ttu-id="58f97-120">*objx*</span><span class="sxs-lookup"><span data-stu-id="58f97-120">*objx*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-121">Coordenada x del objeto calculado.</span><span class="sxs-lookup"><span data-stu-id="58f97-121">The computed x object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="58f97-122">*objy*</span><span class="sxs-lookup"><span data-stu-id="58f97-122">*objy*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-123">Coordenada y del objeto calculado.</span><span class="sxs-lookup"><span data-stu-id="58f97-123">The computed y object coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="58f97-124">*objz*</span><span class="sxs-lookup"><span data-stu-id="58f97-124">*objz*</span></span> 
</dt> <dd>

<span data-ttu-id="58f97-125">Coordenada z calculada del objeto.</span><span class="sxs-lookup"><span data-stu-id="58f97-125">The computed z object coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f97-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58f97-126">Return value</span></span>

<span data-ttu-id="58f97-127">Si la función se ejecuta correctamente, el valor devuelto es GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="58f97-127">If the function succeeds, the return value is GL\_TRUE.</span></span>

<span data-ttu-id="58f97-128">Si se produce un error en la función, el valor devuelto es GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="58f97-128">If the function fails, the return value is GL\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f97-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58f97-129">Remarks</span></span>

<span data-ttu-id="58f97-130">La función **gluUnProject** asigna las coordenadas de ventana especificadas a coordenadas de objeto mediante *modelMatrix*, *projMatrix* y *viewport*.</span><span class="sxs-lookup"><span data-stu-id="58f97-130">The **gluUnProject** function maps the specified window coordinates into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="58f97-131">El resultado se almacena en *objx*, *objy* y *objz*.</span><span class="sxs-lookup"><span data-stu-id="58f97-131">The result is stored in *objx*, *objy*, and *objz*.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f97-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58f97-132">Requirements</span></span>



| <span data-ttu-id="58f97-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f97-133">Requirement</span></span> | <span data-ttu-id="58f97-134">Value</span><span class="sxs-lookup"><span data-stu-id="58f97-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="58f97-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58f97-135">Minimum supported client</span></span><br/> | <span data-ttu-id="58f97-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="58f97-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="58f97-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58f97-137">Minimum supported server</span></span><br/> | <span data-ttu-id="58f97-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58f97-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="58f97-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58f97-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="58f97-140"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="58f97-140"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="58f97-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58f97-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="58f97-142"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58f97-142"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="58f97-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58f97-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f97-144"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58f97-144"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f97-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="58f97-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f97-146">**glGet**</span><span class="sxs-lookup"><span data-stu-id="58f97-146">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="58f97-147">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="58f97-147">**glGetDoublev**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="58f97-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="58f97-148">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="58f97-149">**gluProject**</span><span class="sxs-lookup"><span data-stu-id="58f97-149">**gluProject**</span></span>](gluproject.md)
</dt> </dl>

 

 





