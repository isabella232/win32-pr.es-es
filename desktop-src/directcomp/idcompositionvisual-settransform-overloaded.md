---
title: Métodos IDCompositionVisual SetTransform (Dcomp. h)
description: Establece la propiedad de transformación de este visual. La propiedad transform especifica una transformación 2D utilizada para modificar el sistema de coordenadas de este visual. La propiedad puede especificar una matriz de transformación de 3 por 2 o un objeto de transformación.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
keywords:
- Métodos SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359831"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="cedc5-106">IDCompositionVisual:: SetTransform (métodos)</span><span class="sxs-lookup"><span data-stu-id="cedc5-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="cedc5-107">Establece la propiedad de transformación de este visual.</span><span class="sxs-lookup"><span data-stu-id="cedc5-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="cedc5-108">La propiedad transform especifica una transformación 2D utilizada para modificar el sistema de coordenadas de este visual.</span><span class="sxs-lookup"><span data-stu-id="cedc5-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="cedc5-109">La propiedad puede especificar una matriz de transformación de 3 por 2 o un objeto de transformación.</span><span class="sxs-lookup"><span data-stu-id="cedc5-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cedc5-110">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="cedc5-110">Overload list</span></span>



| <span data-ttu-id="cedc5-111">Método</span><span class="sxs-lookup"><span data-stu-id="cedc5-111">Method</span></span>                                                                                                    | <span data-ttu-id="cedc5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cedc5-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="cedc5-113">[**SetTransform (D2D \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="cedc5-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="cedc5-114">Establece la propiedad transform en la matriz de transformación especificada.</span><span class="sxs-lookup"><span data-stu-id="cedc5-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="cedc5-115">[**SetTransform (IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="cedc5-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="cedc5-116">Establece la propiedad de transformación en el objeto de transformación especificado.</span><span class="sxs-lookup"><span data-stu-id="cedc5-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cedc5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cedc5-117">Requirements</span></span>



| <span data-ttu-id="cedc5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cedc5-118">Requirement</span></span> | <span data-ttu-id="cedc5-119">Value</span><span class="sxs-lookup"><span data-stu-id="cedc5-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cedc5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cedc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cedc5-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cedc5-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cedc5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cedc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cedc5-123">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cedc5-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cedc5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cedc5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cedc5-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cedc5-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cedc5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cedc5-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="cedc5-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cedc5-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="cedc5-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cedc5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cedc5-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cedc5-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cedc5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cedc5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cedc5-131">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="cedc5-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="cedc5-132">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="cedc5-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="cedc5-133">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="cedc5-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="cedc5-134">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="cedc5-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="cedc5-135">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="cedc5-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="cedc5-136">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="cedc5-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="cedc5-137">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="cedc5-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="cedc5-138">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="cedc5-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="cedc5-139">**IDCompositionVisual::SetOffsetY**</span><span class="sxs-lookup"><span data-stu-id="cedc5-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="cedc5-140">�</span><span class="sxs-lookup"><span data-stu-id="cedc5-140">�</span></span>

<span data-ttu-id="cedc5-141">�</span><span class="sxs-lookup"><span data-stu-id="cedc5-141">�</span></span>
