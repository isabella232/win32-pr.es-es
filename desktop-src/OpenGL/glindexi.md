---
title: función glIndexi (GL. h)
description: La función glIndexi establece el índice de color actual.
ms.assetid: c57d2316-4081-40d8-af50-ae0299597803
keywords:
- glIndexi (función) OpenGL
topic_type:
- apiref
api_name:
- glIndexi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b40d8d0d96aac17c852fb266b23dec23d26c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665946"
---
# <a name="glindexi-function"></a><span data-ttu-id="ac32c-104">glIndexi función)</span><span class="sxs-lookup"><span data-stu-id="ac32c-104">glIndexi function</span></span>

<span data-ttu-id="ac32c-105">La función **glIndexi** establece el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="ac32c-105">The **glIndexi** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac32c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac32c-106">Syntax</span></span>


```C++
void WINAPI glIndexi(
   GLint c
);
```



## <a name="parameters"></a><span data-ttu-id="ac32c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac32c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac32c-108">*c*</span><span class="sxs-lookup"><span data-stu-id="ac32c-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="ac32c-109">Nuevo valor para el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="ac32c-109">The new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac32c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac32c-110">Return value</span></span>

<span data-ttu-id="ac32c-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac32c-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac32c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac32c-112">Remarks</span></span>

<span data-ttu-id="ac32c-113">La función **glIndexi** actualiza el índice de color actual (de un solo valor).</span><span class="sxs-lookup"><span data-stu-id="ac32c-113">The **glIndexi** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="ac32c-114">Toma un argumento: el nuevo valor para el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="ac32c-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="ac32c-115">El índice actual se almacena como un valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="ac32c-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="ac32c-116">Los valores enteros se convierten directamente en valores de punto flotante, sin asignación especial.</span><span class="sxs-lookup"><span data-stu-id="ac32c-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="ac32c-117">Los valores de índice fuera del intervalo representable del búfer de índice de color no se fijan.</span><span class="sxs-lookup"><span data-stu-id="ac32c-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="ac32c-118">Sin embargo, antes de que un índice esté desactivado (si está habilitado) y escrito en el fotogramas, se convierte al formato de punto fijo.</span><span class="sxs-lookup"><span data-stu-id="ac32c-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="ac32c-119">Los bits de la parte entera del valor de punto fijo resultante que no se correspondan con bits del fotogramas se enmascaran.</span><span class="sxs-lookup"><span data-stu-id="ac32c-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="ac32c-120">El índice actual se puede actualizar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="ac32c-120">The current index can be updated at any time.</span></span> <span data-ttu-id="ac32c-121">En concreto, se puede llamar a **glIndexi** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ac32c-121">In particular, **glIndexi** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="ac32c-122">La siguiente función recupera información relacionada con **glIndexi**:</span><span class="sxs-lookup"><span data-stu-id="ac32c-122">The following function retrieves information related to **glIndexi**:</span></span>

<span data-ttu-id="ac32c-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ índice actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="ac32c-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="ac32c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac32c-124">Requirements</span></span>



| <span data-ttu-id="ac32c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac32c-125">Requirement</span></span> | <span data-ttu-id="ac32c-126">Value</span><span class="sxs-lookup"><span data-stu-id="ac32c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac32c-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac32c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac32c-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac32c-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac32c-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac32c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac32c-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac32c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac32c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac32c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac32c-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac32c-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ac32c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac32c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac32c-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac32c-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac32c-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac32c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac32c-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac32c-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac32c-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac32c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac32c-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ac32c-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ac32c-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ac32c-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ac32c-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="ac32c-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ac32c-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ac32c-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

