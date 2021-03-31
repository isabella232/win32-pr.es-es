---
title: función glIndexsv (GL. h)
description: La función glIndexsv establece el índice de color actual.
ms.assetid: 4b7f4edf-a7c8-4e81-8448-5181295d5174
keywords:
- glIndexsv (función) OpenGL
topic_type:
- apiref
api_name:
- glIndexsv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da4db5d760845fa6c05923c76459900dafcbdbfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995951"
---
# <a name="glindexsv-function"></a><span data-ttu-id="6e7ae-104">glIndexsv función)</span><span class="sxs-lookup"><span data-stu-id="6e7ae-104">glIndexsv function</span></span>

<span data-ttu-id="6e7ae-105">La función **glIndexsv** establece el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-105">The **glIndexsv** function sets the current color index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7ae-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e7ae-106">Syntax</span></span>


```C++
void WINAPI glIndexsv(
   const GLshort *c
);
```



## <a name="parameters"></a><span data-ttu-id="6e7ae-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e7ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e7ae-108">*c*</span><span class="sxs-lookup"><span data-stu-id="6e7ae-108">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="6e7ae-109">Puntero a una matriz de un elemento que contiene el nuevo valor para el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-109">A pointer to a one-element array that contains the new value for the current color index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e7ae-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e7ae-110">Return value</span></span>

<span data-ttu-id="6e7ae-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e7ae-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e7ae-112">Remarks</span></span>

<span data-ttu-id="6e7ae-113">La función **glIndexsv** actualiza el índice de color actual (de un solo valor).</span><span class="sxs-lookup"><span data-stu-id="6e7ae-113">The **glIndexsv** function updates the current (single-valued) color index.</span></span> <span data-ttu-id="6e7ae-114">Toma un argumento: el nuevo valor para el índice de color actual.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-114">It takes one argument: the new value for the current color index.</span></span>

<span data-ttu-id="6e7ae-115">El índice actual se almacena como un valor de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-115">The current index is stored as a floating-point value.</span></span> <span data-ttu-id="6e7ae-116">Los valores enteros se convierten directamente en valores de punto flotante, sin asignación especial.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-116">Integer values are converted directly to floating-point values, with no special mapping.</span></span>

<span data-ttu-id="6e7ae-117">Los valores de índice fuera del intervalo representable del búfer de índice de color no se fijan.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-117">Index values outside the representable range of the color-index buffer are not clamped.</span></span> <span data-ttu-id="6e7ae-118">Sin embargo, antes de que un índice esté desactivado (si está habilitado) y escrito en el fotogramas, se convierte al formato de punto fijo.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-118">However, before an index is dithered (if enabled) and written to the framebuffer, it is converted to fixed-point format.</span></span> <span data-ttu-id="6e7ae-119">Los bits de la parte entera del valor de punto fijo resultante que no se correspondan con bits del fotogramas se enmascaran.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-119">Any bits in the integer portion of the resulting fixed-point value that do not correspond to bits in the framebuffer are masked out.</span></span>

<span data-ttu-id="6e7ae-120">El índice actual se puede actualizar en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-120">The current index can be updated at any time.</span></span> <span data-ttu-id="6e7ae-121">En concreto, se puede llamar a **glIndexsv** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6e7ae-121">In particular, **glIndexsv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](glend.md).</span></span>

<span data-ttu-id="6e7ae-122">La siguiente función recupera información relacionada con **glIndexsv**:</span><span class="sxs-lookup"><span data-stu-id="6e7ae-122">The following function retrieves information related to **glIndexsv**:</span></span>

<span data-ttu-id="6e7ae-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ índice actual de GL \_</span><span class="sxs-lookup"><span data-stu-id="6e7ae-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_INDEX</span></span>

## <a name="requirements"></a><span data-ttu-id="6e7ae-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e7ae-124">Requirements</span></span>



| <span data-ttu-id="6e7ae-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e7ae-125">Requirement</span></span> | <span data-ttu-id="6e7ae-126">Value</span><span class="sxs-lookup"><span data-stu-id="6e7ae-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7ae-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e7ae-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7ae-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6e7ae-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6e7ae-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e7ae-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7ae-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e7ae-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e7ae-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e7ae-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7ae-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e7ae-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6e7ae-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e7ae-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e7ae-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e7ae-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e7ae-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e7ae-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e7ae-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e7ae-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e7ae-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e7ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e7ae-138">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-138">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6e7ae-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="6e7ae-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6e7ae-141">**glGet**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-141">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

