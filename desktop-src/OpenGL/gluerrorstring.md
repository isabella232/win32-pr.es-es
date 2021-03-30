---
title: función gluErrorString (GLU. h)
description: La función gluErrorString genera una cadena de error a partir de un código de error OpenGL o GLU. La cadena de error es sólo ANSI.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString (función) OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801988"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="9b576-105">gluErrorString función)</span><span class="sxs-lookup"><span data-stu-id="9b576-105">gluErrorString function</span></span>

<span data-ttu-id="9b576-106">La función **gluErrorString** genera una cadena de error a partir de un código de error OpenGL o Glu.</span><span class="sxs-lookup"><span data-stu-id="9b576-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="9b576-107">La cadena de error es sólo ANSI.</span><span class="sxs-lookup"><span data-stu-id="9b576-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b576-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b576-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="9b576-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b576-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b576-110">*errCode*</span><span class="sxs-lookup"><span data-stu-id="9b576-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="9b576-111">Un código de error de OpenGL o GLU.</span><span class="sxs-lookup"><span data-stu-id="9b576-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b576-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b576-112">Remarks</span></span>

<span data-ttu-id="9b576-113">La función **gluErrorString** genera una cadena de error a partir de un código de error OpenGL o Glu.</span><span class="sxs-lookup"><span data-stu-id="9b576-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="9b576-114">La cadena tiene un formato ISO Latín 1.</span><span class="sxs-lookup"><span data-stu-id="9b576-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="9b576-115">Por ejemplo, **gluErrorString**(libro \_ \_ de memoria insuficiente \_ ) devuelve la cadena "memoria insuficiente".</span><span class="sxs-lookup"><span data-stu-id="9b576-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="9b576-116">Los códigos de error de GLU estándar son GLU \_ \_ enumeración no válida, Glu \_ valor no válido \_ y Glu \_ memoria insuficiente \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9b576-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="9b576-117">Algunas otras funciones GLU pueden devolver códigos de error especializados a través de las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="9b576-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="9b576-118">Para obtener la lista de códigos de error de OpenGL, vea [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="9b576-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="9b576-119">La función **gluErrorString** solo genera cadenas de error en ANSI.</span><span class="sxs-lookup"><span data-stu-id="9b576-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="9b576-120">Siempre que sea posible, use **gluErrorStringWIN**, que permite cadenas de error ANSI o Unicode.</span><span class="sxs-lookup"><span data-stu-id="9b576-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="9b576-121">De este modo, resulta más fácil localizar el programa para usarlo con otro lenguaje.</span><span class="sxs-lookup"><span data-stu-id="9b576-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b576-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b576-122">Requirements</span></span>



| <span data-ttu-id="9b576-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b576-123">Requirement</span></span> | <span data-ttu-id="9b576-124">Value</span><span class="sxs-lookup"><span data-stu-id="9b576-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b576-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b576-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b576-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9b576-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9b576-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b576-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b576-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9b576-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9b576-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b576-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b576-130"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b576-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9b576-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b576-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9b576-132"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b576-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9b576-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b576-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b576-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b576-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b576-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b576-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b576-136">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="9b576-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="9b576-137">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="9b576-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="9b576-138">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="9b576-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="9b576-139">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="9b576-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





