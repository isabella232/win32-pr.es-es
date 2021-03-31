---
title: Métodos SetClip IDCompositionVisual (Dcomp. h)
description: Establece la propiedad clip de este objeto visual en la región rectangular o el objeto de clip especificados.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip (métodos) DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803709"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="d6e6c-104">IDCompositionVisual:: SetClip (métodos)</span><span class="sxs-lookup"><span data-stu-id="d6e6c-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="d6e6c-105">Establece la propiedad clip de este objeto visual en la región rectangular o el objeto de clip especificados.</span><span class="sxs-lookup"><span data-stu-id="d6e6c-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="d6e6c-106">La propiedad clip restringe la representación del subárbol visual que está en la raíz de este visual a una región rectangular.</span><span class="sxs-lookup"><span data-stu-id="d6e6c-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d6e6c-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="d6e6c-107">Overload list</span></span>



| <span data-ttu-id="d6e6c-108">Método</span><span class="sxs-lookup"><span data-stu-id="d6e6c-108">Method</span></span>                                                                                | <span data-ttu-id="d6e6c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6e6c-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="d6e6c-110">[**SetClip (const D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="d6e6c-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="d6e6c-111">Establece la propiedad clip en la región rectangular especificada.</span><span class="sxs-lookup"><span data-stu-id="d6e6c-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="d6e6c-112">[**SetClip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="d6e6c-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="d6e6c-113">Establece la propiedad clip en el objeto de clip especificado.</span><span class="sxs-lookup"><span data-stu-id="d6e6c-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="d6e6c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6e6c-114">Requirements</span></span>



| <span data-ttu-id="d6e6c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6e6c-115">Requirement</span></span> | <span data-ttu-id="d6e6c-116">Value</span><span class="sxs-lookup"><span data-stu-id="d6e6c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e6c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6e6c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6e6c-118">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6e6c-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d6e6c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6e6c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6e6c-120">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6e6c-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6e6c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6e6c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6e6c-122"><dt>Dcomp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6e6c-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d6e6c-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6e6c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6e6c-124"><dt>Dcomp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6e6c-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="d6e6c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6e6c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6e6c-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6e6c-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6e6c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6e6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e6c-128">Recorte</span><span class="sxs-lookup"><span data-stu-id="d6e6c-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="d6e6c-129">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="d6e6c-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="d6e6c-130">�</span><span class="sxs-lookup"><span data-stu-id="d6e6c-130">�</span></span>

<span data-ttu-id="d6e6c-131">�</span><span class="sxs-lookup"><span data-stu-id="d6e6c-131">�</span></span>
