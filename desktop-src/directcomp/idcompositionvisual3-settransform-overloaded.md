---
title: Métodos IDCompositionVisual3 SetTransform (Dcomp. h)
description: Establece la propiedad de transformación de este visual. La propiedad transform especifica una transformación 3D utilizada para modificar el sistema de coordenadas de este visual. La propiedad puede especificar una matriz de transformación de 4 por 4 o un objeto de transformación.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
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
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714591"
---
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="f7960-106">IDCompositionVisual3:: SetTransform (métodos)</span><span class="sxs-lookup"><span data-stu-id="f7960-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="f7960-107">Establece la propiedad de transformación de este visual.</span><span class="sxs-lookup"><span data-stu-id="f7960-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="f7960-108">La propiedad transform especifica una transformación 3D utilizada para modificar el sistema de coordenadas de este visual.</span><span class="sxs-lookup"><span data-stu-id="f7960-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="f7960-109">La propiedad puede especificar una matriz de transformación de 4 por 4 o un objeto de transformación.</span><span class="sxs-lookup"><span data-stu-id="f7960-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f7960-110">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="f7960-110">Overload list</span></span>



| <span data-ttu-id="f7960-111">Método</span><span class="sxs-lookup"><span data-stu-id="f7960-111">Method</span></span>                                                                                  | <span data-ttu-id="f7960-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7960-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="f7960-113">[**SetTransform ( \_ matriz D2D \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="f7960-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="f7960-114">Establece la propiedad transform en la matriz de transformación especificada.</span><span class="sxs-lookup"><span data-stu-id="f7960-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="f7960-115">[**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="f7960-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="f7960-116">Establece la propiedad de transformación en el objeto de transformación especificado.</span><span class="sxs-lookup"><span data-stu-id="f7960-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f7960-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7960-117">Requirements</span></span>



| <span data-ttu-id="f7960-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7960-118">Requirement</span></span> | <span data-ttu-id="f7960-119">Value</span><span class="sxs-lookup"><span data-stu-id="f7960-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7960-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7960-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7960-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7960-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f7960-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7960-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7960-123">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7960-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f7960-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7960-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7960-125"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7960-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7960-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7960-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7960-127"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7960-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7960-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7960-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7960-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7960-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7960-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7960-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7960-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="f7960-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="f7960-132">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="f7960-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="f7960-133">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="f7960-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="f7960-134">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="f7960-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="f7960-135">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="f7960-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="f7960-136">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="f7960-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="f7960-137">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="f7960-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="f7960-138">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="f7960-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="f7960-139">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="f7960-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="f7960-140">**IDCompositionVisual::SetOffsetY**</span><span class="sxs-lookup"><span data-stu-id="f7960-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="f7960-141">�</span><span class="sxs-lookup"><span data-stu-id="f7960-141">�</span></span>

<span data-ttu-id="f7960-142">�</span><span class="sxs-lookup"><span data-stu-id="f7960-142">�</span></span>
