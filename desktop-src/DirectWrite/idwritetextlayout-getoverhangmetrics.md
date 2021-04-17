---
title: IDWriteTextLayout GetOverhangMetrics, método
description: Devuelve los sobrebloqueos (en DIP) del diseño y todos los objetos contenidos en él, incluidos los glifos de texto y los objetos insertados.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Método GetOverhangMetrics de escritura directa
- Método GetOverhangMetrics de escritura directa, interfaz IDWriteTextLayout
- Interfaz IDWriteTextLayout Direct Write, método GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670863"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="34e9a-106">IDWriteTextLayout:: GetOverhangMetrics (método)</span><span class="sxs-lookup"><span data-stu-id="34e9a-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="34e9a-107">Devuelve los sobrebloqueos (en DIP) del diseño y todos los objetos contenidos en él, incluidos los glifos de texto y los objetos insertados.</span><span class="sxs-lookup"><span data-stu-id="34e9a-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e9a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34e9a-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="34e9a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34e9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34e9a-110">*sobrebloqueos* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34e9a-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34e9a-111">Tipo: **[ **\_ \_ métricas salientes de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="34e9a-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="34e9a-112">Excesos de extensiones visibles (en DIP) fuera del diseño.</span><span class="sxs-lookup"><span data-stu-id="34e9a-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34e9a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34e9a-113">Return value</span></span>

<span data-ttu-id="34e9a-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="34e9a-114">Type: **HRESULT**</span></span>

<span data-ttu-id="34e9a-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="34e9a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="34e9a-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="34e9a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="34e9a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34e9a-117">Remarks</span></span>

<span data-ttu-id="34e9a-118">Los subrayados y los tachados no contribuyen a la determinación del cuadro negro, ya que el representador los dibuja realmente, lo que puede dibujarlos en cualquier variedad de estilos.</span><span class="sxs-lookup"><span data-stu-id="34e9a-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="34e9a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34e9a-119">Requirements</span></span>



| <span data-ttu-id="34e9a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e9a-120">Requirement</span></span> | <span data-ttu-id="34e9a-121">Value</span><span class="sxs-lookup"><span data-stu-id="34e9a-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34e9a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34e9a-122">Library</span></span><br/> | <dl> <span data-ttu-id="34e9a-123"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34e9a-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="34e9a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34e9a-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="34e9a-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34e9a-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e9a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="34e9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e9a-127">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="34e9a-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="34e9a-128">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="34e9a-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

