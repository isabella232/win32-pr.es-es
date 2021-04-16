---
title: función gluNurbsCallback (GLU. h)
description: La función gluNurbsCallback define una devolución de llamada para un objeto no uniforme B-spline racional (NURBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback (función) OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676655"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="3b706-104">gluNurbsCallback función)</span><span class="sxs-lookup"><span data-stu-id="3b706-104">gluNurbsCallback function</span></span>

<span data-ttu-id="3b706-105">La función **gluNurbsCallback** define una devolución de llamada para un objeto no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).</span><span class="sxs-lookup"><span data-stu-id="3b706-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b706-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b706-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="3b706-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b706-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b706-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="3b706-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="3b706-109">El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="3b706-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3b706-110">*cuales*</span><span class="sxs-lookup"><span data-stu-id="3b706-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="3b706-111">Devolución de llamada que se está definiendo.</span><span class="sxs-lookup"><span data-stu-id="3b706-111">The callback being defined.</span></span> <span data-ttu-id="3b706-112">El único valor válido es GLU \_ error.</span><span class="sxs-lookup"><span data-stu-id="3b706-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="3b706-113">El significado del \_ error Glu significa que se llama a la función de error cuando se produce un error.</span><span class="sxs-lookup"><span data-stu-id="3b706-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="3b706-114">Su único argumento es de tipo **GLenum** y indica el error específico que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="3b706-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="3b706-115">Hay 37 errores exclusivos de NURBS, denominados GLU \_ NURBS \_ ERROR1 a Glu \_ NURBS \_ ERROR37.</span><span class="sxs-lookup"><span data-stu-id="3b706-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="3b706-116">Las cadenas de caracteres que describen estos errores pueden recuperarse con [**gluErrorString**](gluerrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="3b706-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b706-117">*fn*</span><span class="sxs-lookup"><span data-stu-id="3b706-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="3b706-118">Puntero a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3b706-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b706-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b706-119">Return value</span></span>

<span data-ttu-id="3b706-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3b706-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b706-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b706-121">Remarks</span></span>

<span data-ttu-id="3b706-122">Use **gluNurbsCallback** para definir una devolución de llamada que se va a usar en un objeto NURBS.</span><span class="sxs-lookup"><span data-stu-id="3b706-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="3b706-123">Si la devolución de llamada especificada ya está definida, se reemplaza.</span><span class="sxs-lookup"><span data-stu-id="3b706-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="3b706-124">Si *FN* es **null**, se borrarán todas las devoluciones de llamada existentes.</span><span class="sxs-lookup"><span data-stu-id="3b706-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b706-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b706-125">Requirements</span></span>



| <span data-ttu-id="3b706-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b706-126">Requirement</span></span> | <span data-ttu-id="3b706-127">Value</span><span class="sxs-lookup"><span data-stu-id="3b706-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b706-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b706-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3b706-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3b706-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3b706-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b706-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3b706-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3b706-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3b706-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b706-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b706-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b706-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3b706-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b706-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b706-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b706-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3b706-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b706-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b706-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b706-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b706-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b706-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b706-139">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="3b706-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="3b706-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="3b706-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





