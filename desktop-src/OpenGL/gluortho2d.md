---
title: Función gluOrtho2D (Glu.h)
description: La función gluOrtho2D define una matriz de proyección ortográfica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- Función gluOrtho2D OpenGL
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
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153558"
---
# <a name="gluortho2d-function"></a><span data-ttu-id="14d62-104">Función gluOrtho2D</span><span class="sxs-lookup"><span data-stu-id="14d62-104">gluOrtho2D function</span></span>

<span data-ttu-id="14d62-105">La **función gluOrtho2D** define una matriz de proyección ortográfica 2D.</span><span class="sxs-lookup"><span data-stu-id="14d62-105">The **gluOrtho2D** function defines a 2-D orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d62-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14d62-106">Syntax</span></span>


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a><span data-ttu-id="14d62-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14d62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d62-108">*Izquierda*</span><span class="sxs-lookup"><span data-stu-id="14d62-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="14d62-109">Coordenada del plano de recorte vertical izquierdo.</span><span class="sxs-lookup"><span data-stu-id="14d62-109">The coordinate for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-110">*Correcto*</span><span class="sxs-lookup"><span data-stu-id="14d62-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="14d62-111">Coordenada del plano de recorte vertical derecho.</span><span class="sxs-lookup"><span data-stu-id="14d62-111">The coordinate for the right vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-112">*top*</span><span class="sxs-lookup"><span data-stu-id="14d62-112">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="14d62-113">Coordenada del plano de recorte horizontal superior.</span><span class="sxs-lookup"><span data-stu-id="14d62-113">The coordinate for the top horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="14d62-114">*Parte inferior*</span><span class="sxs-lookup"><span data-stu-id="14d62-114">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="14d62-115">Coordenada del plano de recorte horizontal inferior.</span><span class="sxs-lookup"><span data-stu-id="14d62-115">The coordinate for the bottom horizontal clipping plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d62-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14d62-116">Return value</span></span>

<span data-ttu-id="14d62-117">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="14d62-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14d62-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14d62-118">Remarks</span></span>

<span data-ttu-id="14d62-119">La **función gluOrtho2D** configura una región de visualización ortográfica bidimensional.</span><span class="sxs-lookup"><span data-stu-id="14d62-119">The **gluOrtho2D** function sets up a two-dimensional orthographic viewing region.</span></span> <span data-ttu-id="14d62-120">Esto equivale a llamar [**a glOrtho**](glortho.md) con zNear = -1 y zFar = 1.</span><span class="sxs-lookup"><span data-stu-id="14d62-120">This is equivalent to calling [**glOrtho**](glortho.md) with zNear = -1 and zFar = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d62-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d62-121">Requirements</span></span>



| <span data-ttu-id="14d62-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d62-122">Requirement</span></span> | <span data-ttu-id="14d62-123">Valor</span><span class="sxs-lookup"><span data-stu-id="14d62-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14d62-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d62-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14d62-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="14d62-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="14d62-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d62-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14d62-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14d62-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14d62-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14d62-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d62-129"><dt>Glu.h</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-129"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="14d62-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14d62-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="14d62-131"><dt>Glu32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-131"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="14d62-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14d62-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d62-133"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d62-133"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14d62-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14d62-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d62-135">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="14d62-135">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="14d62-136">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="14d62-136">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





