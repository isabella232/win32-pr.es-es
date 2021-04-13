---
title: función gluOrtho2D (GLU. h)
description: La función gluOrtho2D define una matriz de proyección ortográfica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D (función) OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421901"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="ce362-104">gluOrtho2D función)</span><span class="sxs-lookup"><span data-stu-id="ce362-104">gluOrtho2D function</span></span>

<span data-ttu-id="ce362-105">La función **gluOrtho2D** define una matriz de proyección ortográfica 2D.</span><span class="sxs-lookup"><span data-stu-id="ce362-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce362-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce362-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="ce362-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce362-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce362-108">*salido*</span><span class="sxs-lookup"><span data-stu-id="ce362-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="ce362-109">Coordenada del plano de recorte vertical izquierdo.</span><span class="sxs-lookup"><span data-stu-id="ce362-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="ce362-110">*correcta*</span><span class="sxs-lookup"><span data-stu-id="ce362-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="ce362-111">Coordenada del plano de recorte vertical derecho.</span><span class="sxs-lookup"><span data-stu-id="ce362-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="ce362-112">*top*</span><span class="sxs-lookup"><span data-stu-id="ce362-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="ce362-113">Coordenada del plano de recorte horizontal superior.</span><span class="sxs-lookup"><span data-stu-id="ce362-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="ce362-114">*descendente*</span><span class="sxs-lookup"><span data-stu-id="ce362-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="ce362-115">Coordenada del plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="ce362-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce362-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce362-116">Return value</span></span>

<span data-ttu-id="ce362-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ce362-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce362-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce362-118">Remarks</span></span>

<span data-ttu-id="ce362-119">La función **gluOrtho2D** configura una región de visualización ortográfica bidimensional.</span><span class="sxs-lookup"><span data-stu-id="ce362-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="ce362-120">Esto es equivalente a llamar a [**glOrtho**](glortho.md) con Near = 1 y Far = 1.</span><span class="sxs-lookup"><span data-stu-id="ce362-120">This is equivalent to calling [**glOrtho**](glortho.md) with near =  1 and far = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce362-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce362-121">Requirements</span></span>



| <span data-ttu-id="ce362-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce362-122">Requirement</span></span> | <span data-ttu-id="ce362-123">Value</span><span class="sxs-lookup"><span data-stu-id="ce362-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce362-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce362-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ce362-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ce362-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ce362-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce362-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ce362-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ce362-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ce362-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce362-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce362-129"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce362-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ce362-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce362-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce362-131"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce362-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce362-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ce362-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce362-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce362-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce362-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce362-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce362-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="ce362-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="ce362-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="ce362-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





